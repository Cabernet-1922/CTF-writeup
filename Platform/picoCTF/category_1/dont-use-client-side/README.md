# dont-use-client-side [Easy] (by Alex Fulton/Danny) - picoCTF 2019
> Can you break into this super secure portal? <code>https://jupiter.challenges.picoctf.org/problem/17682/</code> (<a href="https://jupiter.challenges.picoctf.org/problem/17682/">link</a>) or http://jupiter.challenges.picoctf.org:17682

```javascript
function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == '706c') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_b') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == '5}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
```

By viewing the source code of the page, we get a javascript. However, we do not need to understand the code, simple sort the if statement `split*`:
```text
0 -> pico
split -> CTF{
split*2 -> no_c
split*3 -> lien
split*4 -> ts_p
split*5 -> lz_b
split*6 -> 706c
split*7 -> 5}
```

flag: `picoCTF{no_clients_plz_b706c5}`