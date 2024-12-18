# First Grep [Easy] (by Alex Fulton/Danny Tunitis) - picoCTF 2019
> Can you find the flag in <a href='//jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file'>file</a>? This would be really tedious to look through manually, something tells me there is a better way.


```bash
grep -roP "picoCTF{.*}"
```

flag: `picoCTF{grep_is_good_to_find_things_dba08a45}`