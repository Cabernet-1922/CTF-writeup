# Python Wrangling [Easy] (by syreal) - picoCTF 2021
> Python scripts are invoked kind of like programs in the Terminal... Can you run <a href='//mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py'>this Python script</a> using <a href='//mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt'>this password</a> to get <a href='//mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en'>the flag</a>?


We have a password: `67c6cc9667c6cc9667c6cc9667c6cc96`, a python file and encrypted file.
```bash
python ende.py -d flag.txt.en
Please enter the password:67c6cc9667c6cc9667c6cc9667c6cc96
```
flag: `picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}`