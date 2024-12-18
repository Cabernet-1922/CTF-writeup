# logon [Easy] (by bobson) - picoCTF 2019
> The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? <code>https://jupiter.challenges.picoctf.org/problem/44573/</code> (<a href="https://jupiter.challenges.picoctf.org/problem/44573/">link</a>) or http://jupiter.challenges.picoctf.org:44573

Use a random username and password to log into the site. Then we see `admin: False' in the cookie page, manually change it to True and refresh the page. The flag will now be displayed.

flag: `picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc}`
