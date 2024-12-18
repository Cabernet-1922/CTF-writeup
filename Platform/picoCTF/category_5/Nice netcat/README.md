# Nice netcat... [Easy] (by syreal) - picoCTF 2021
> There is a nice program that you can talk to by using this command in a shell: <code>$ nc mercury.picoctf.net 22902</code>, but it doesn't speak English...


After connect the remote server, it prints out: `112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 100 51 100 102 100 54 100 102 125 10`
It's obviously an ascii sequence, we can change it to readable characters:
```python
a = "112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 100 51 100 102 100 54 100 102 125 10"
"".join([chr(int(i)) for i in a.split(" ")])
```

flag: `picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}`
