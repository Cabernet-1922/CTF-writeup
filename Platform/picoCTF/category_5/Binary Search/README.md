# Binary Search [Easy] (by Jeffery John) - picoCTF 2024
> <p>Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.</p>
<p>Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!</p>
<p>You can download the challenge files here:</p>
<ul>
<li><a href='https://artifacts.picoctf.net/c_atlas/5/challenge.zip' download>challenge.zip</a></li>
</ul>

As the challenge name states, we need to do the binary search manually.\
Example:
```text
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 250
Lower! Try again.
Enter your guess: 125
Higher! Try again.
Enter your guess: 187
Higher! Try again.
Enter your guess: 218
Higher! Try again.
Enter your guess: 234
Lower! Try again.
Enter your guess: 226
Lower! Try again.
Enter your guess: 222
Lower! Try again.
Enter your guess: 220
Higher! Try again.
Enter your guess: 221
Congratulations! You guessed the correct number: 221
Here's your flag: picoCTF{g00d_gu355_3af33d18}
```

flag: `picoCTF{g00d_gu355_3af33d18}`