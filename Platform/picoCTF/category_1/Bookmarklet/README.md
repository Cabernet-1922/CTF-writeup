# Bookmarklet [Easy] (by Jeffery John) - picoCTF 2024
> <p>Why search for the flag when I can make a bookmarklet to print it for me?</p>


Simply run the javascript, and it will print out the flag:
```javascript
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÒËÉ§©í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
```

flag: `picoCTF{p@g3_turn3r_6bbf8953}`