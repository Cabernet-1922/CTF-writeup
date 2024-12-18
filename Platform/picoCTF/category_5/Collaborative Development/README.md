# Collaborative Development [Easy] (by Jeffery John) - picoCTF 2024
> <p>My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?</p>
<p>You can download the challenge files here:</p>
<ul>
<li><a href='https://artifacts.picoctf.net/c_titan/179/challenge.zip' download>challenge.zip</a></li>
</ul>

We can use `git log` and `git checkout` to check the commits, however, there is only one commits in the log. \
Therefore, we need to find out all the commit hash in the `.git` folder: `grep -roP "[0-9a-f]{20,}"`. After that, appear some strange path name:
```text
.git/refs/heads/feature/part-1
.git/refs/heads/feature/part-2
.git/refs/heads/feature/part-3
```
Then, go checkout each of them. There part of flag form the complete flag:
`picoCTF{t3@mw0rk_`+`m@k3s_th3_dr3@m_`+`w0rk_798f9981}`

flag: `picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_798f9981}`