# information [Easy] (by susie) - picoCTF 2021
> Files can always be changed in a secret way. Can you find the flag? <a href='//mercury.picoctf.net/static/a614a27d4cb251d04c7d2f3f3f76a965/cat.jpg'>cat.jpg</a>

```bash
exiftool cat.jpg
```
Then we found `cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9` strange, use base64 decode the message, we will get the flag.

flag: `picoCTF{the_m3tadata_1s_modified}`