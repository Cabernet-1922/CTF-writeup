# strings it [Easy] (by Sanjay C/Danny Tunitis) - picoCTF 2019
> Can you find the flag in <a href='//jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings'>file</a> without running it?


```bash
strings strings | grep -oP "picoCTF{.*}"
```


flag: `picoCTF{5tRIng5_1T_827aee91}`