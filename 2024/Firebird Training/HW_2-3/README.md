# Challenge: Super Encryption 2.633 v3
This challenge was solved more than a month ago, so already forgot about the detail. The payload could be refined... I may pick up this when have time...
## Solution:
There are total 6 stages.
- Stage 0
Use the given PoW_solve function
- Stage 1
base64 decoding
-  Stage 2
hex
-  Stage 3
base32 decoding
-  Stage 3+
base32 decoding
- Stage 1,2,3+
base32 (need to upper case all the letter)
```
from pwn import *
import hashlib
import random
import string
import itertools, re
import base64
LENGTH = 6
hex_set = "0123456789abcdef"
letter_set = string.ascii_letters + string.digits


def PoW_solve(given: str, h: str) -> str:
    for ch in itertools.product(hex_set, repeat=LENGTH):
        ch = ''.join(ch)
        if h == hashlib.md5(f"SE2:{given}:{ch}".encode()).hexdigest():
            return ch


r = remote("chal.firebird.sh", 'xxxxx')
# r = remote("chal.firebird.sh", 'xxxxx',level="debug")
res = r.recvline_contains("md5").decode().strip()
given = str(re.findall(":.*:", res)[0]).strip(":")
h = str(re.findall("=.*",res)[0]).strip("=").lstrip(" ")
ch = PoW_solve(given=given,h=h).encode()
r.sendline(ch)
r.recvline()


code = r.recvline_contains("Vm").decode().strip()
r.recv()
while len(code) != 7:
    code += (4 - (len(code) % 4)) * "="
    code = base64.b64decode(code)
    code = code.decode()
code = code.encode()
r.sendline(code)
r.recvline()



# stage 2
code = ""
#for i in range(100):
newdata = r.recvline_contains("33").decode()
code += newdata
print("-----------------------------------")
while len(code) > 7:
    code = code.strip("=")
    if (len(code) % 2) != 0:
        code = "0"+code
    len(code)
    code = bytes.fromhex(code).decode('utf-8')

code = code.encode()
r.recv()
r.sendline(code)
r.recvline()
# stage 3
r.recvline()
code = r.recvline().decode().strip()
while len(code) > 7:
    try:
        code = base64.b32decode(code).decode()
    except Exception as e:
        if (8-(len(code)%8)) <= 4:
            code += (8-(len(code)%8)) *"="
        else:
            code= code[:-(len(code)%8)]
code = code.encode()
#print(code)
r.recv()
r.sendline(code)
r.recvline()
print(r.recvline())




# stage 3+
code = r.recvline_contains("J")
print(r.recvuntil(":"))
code = code.decode().strip()
while len(code) > 7:
   # print(code)
    try:
        code = base64.b32decode(code,casefold=True).decode()
    except Exception as e:
        if (8-(len(code)%8)) <= 4:
            code += (8-(len(code)%8)) *"="
        else:
            code= code[:-(len(code)%8)]
code = code.encode()

r.sendline(code)
print(r.recvline())
print(r.recvline())



# Stage 1,2,3+
code = r.recvline_contains("n")
print(r.recvuntil(":"))
code = code.decode().strip()
print(code)


while len(code) != 7:
    #print(code)
    try:
        code = base64.b32decode(code,casefold=True).decode()
    except Exception as e:
        if (8-(len(code)%8)) <= 4:
            code += (8-(len(code)%8)) *"="
        else:
            code= code[:-(len(code)%8)]



code = code.encode()

print(code)
r.sendline(code)
print(r.recvline())
print(r.recvline())
```
