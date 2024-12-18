# Scavenger Hunt [Easy] (by madStacks) - picoCTF 2021
> There is some interesting information hidden around this site <a href="http://mercury.picoctf.net:27278/">http://mercury.picoctf.net:27278/</a>. Can you find it?


The flag in this challenge is divided into five parts, the first two parts use the same technique as [Insp3ct0r](../Insp3ct0r/README.md).\
For the third part, when we access `myjs.js`, there is a comment that caught our attention: `How can I keep Google from indexing my website?` This could refer to the `robots.txt` that specifies the indexing rule. The `robots.txt` shows the third part of the flag: `t_0f_pl4c`.
For the fourth part it says `I think this is an apache server... can you Access the next flag?`. The Apache server allows directory level configuration, which means that there is a `.htaccess` configuration. So we get the fourth part of the flag: `3s_2_lO0k`.\
For the last part: `I love making websites on my Mac, I can Store a lot of information there.`, this implies the `.DS_Store` file specifically related to macOS. Then access that to get the last part of the flag: `_a69684fd}`


first part: `picoCTF{t` \
second part: `h4ts_4_l0`\
third part: `t_0f_pl4c` \
fourth part: `3s_2_lO0k` \
last part: `_a69684fd}` \
flag: `picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_a69684fd}`

