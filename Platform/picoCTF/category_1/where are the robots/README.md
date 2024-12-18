# where are the robots [Easy] (by zaratec/Danny) - picoCTF 2019
> Can you find the robots? <code>https://jupiter.challenges.picoctf.org/problem/36474/</code> (<a href="https://jupiter.challenges.picoctf.org/problem/36474/">link</a>) or http://jupiter.challenges.picoctf.org:36474


Robots for a web challenge often refers to robots.txt file, so we access `/robots.txt` and found that: `User-agent: *
Disallow: /477ce.html`, this might be related to the flag we are finding.

flag: `picoCTF{ca1cu1at1ng_Mach1n3s_477ce}`