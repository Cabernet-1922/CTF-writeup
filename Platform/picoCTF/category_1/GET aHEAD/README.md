# GET aHEAD [Easy] (by madStacks) - picoCTF 2021
> Find the flag being held on this server to get ahead of the competition <a href="http://mercury.picoctf.net:47967/">http://mercury.picoctf.net:47967/</a>

By looking at the source of the page, we found that it uses the `GET` method when choosing red and the `POST` method when choosing blue. \
With Burpsuite, we can use `POST` method to request red or `GET` method to request blue. However, both not work. \
So far we can check the title of this challenge, it actually mentioned two request methods `GET` and `HEAD`. Then we can also try the HEAD method to request the page.
```bash
curl http://mercury.picoctf.net:47967/index.php --HEAD
```

flag: `picoCTF{r3j3ct_th3_du4l1ty_cca66bd3}`



reference: https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD