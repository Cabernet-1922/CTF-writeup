# IntroToBurp [Easy] (by Nana Ama Atombo-Sackey & Sabine Gisagara) - picoCTF 2024

After we randomly input something as registration, the page require us to submit a `OTP` for authentication. By pressing `F12` and go to cookies tab, we get the cookie `session: .eJw9jN0KQiEQhN9lr7sQk_T0MrK7rhSdo-IPEdG7ZyDN1cw3zLyB7_0FV0A4Abcafc8PSRNoMsxKb4QuGOU2tkGjVULnGEguKNpoFPfbxbHvPuEh6yf3Mp2Zsm7Ggq09cw2rLbecxKdxkNSFRpP633--DFctCA.Z2JWAg.XEhF0JBOpFdbKeSflHL8mac5yIg`, we can try to decode this with [flask-unsign](https://github.com/Paradoxis/Flask-Unsign):
```bash
flask-unsign -d --cookie .eJw9jN0KQiEQhN9lr7sQk_T0MrK7rhSdo-IPEdG7ZyDN1cw3zLyB7_0FV0A4Abcafc8PSRNoMsxKb4QuGOU2tkGjVULnGEguKNpoFPfbxbHvPuEh6yf3Mp2Zsm7Ggq09cw2rLbecxKdxkNSFRpP633--DFctCA.Z2JWAg.XEhF0JBOpFdbKeSflHL8mac5yIg
```
Then, we get `{'city': 'a', 'csrf_token': '2b4cc029ba8d4089c7d2a70eb3fdbe6ae242ae8a', 'full_name': 'a', 'otp': '444478', 'password': 'a', 'phone_number': 'a', 'username': 'a'}`, enter the `otp` to get the flag.


flag: `picoCTF{#0TP_Bypvss_SuCc3$S_b3fa4f1a}`