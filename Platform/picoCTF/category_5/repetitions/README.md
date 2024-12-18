# repetitions [Easy] (by Theoneste Byagutangaza) - picoCTF 2023
> <p>Can you make sense of this file?</p>
> <p>Download the file <a href='https://artifacts.picoctf.net/c/475/enc_flag' download>here</a>.</p>

```bash
cat enc_flag | base64 --decode | base64 --decode | base64 --decode | base64 --decode | base64 --decode | base64 --decode
```
flag: `picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_492767d2}`