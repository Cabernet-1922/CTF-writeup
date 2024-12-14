# Exercise 3-B Trojan Horse [100 points] (41 solves)
Basically make the server think it is coming from a local address:
```bash
curl -X POST http://chal.firebird.sh:35016 -sH "X-Forwarded-For: 127.0.0.1" | grep -oP "flag{.*}"
```