# binhexa [Easy] (by Nana Ama Atombo-Sackey) - picoCTF 2024
> <p>How well can you perfom basic binary operations?</p>

Connect the server, get two binary number.
Suppose Binary Number 1: `01000001` and Binary Number 2: `11000001`, follow the instruction and compute the answer.
\
\
Question 1/6:
Operation 1: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: `100000010`

Question 2/6:
Operation 2: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: `11000001`

Question 3/6:
Operation 3: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: `1100000`
Correct!


Question 4/6:
Operation 4: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: `1000001`
Correct!

Question 5/6:
Operation 5: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: `10000010`

Question 6/6:
Operation 6: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: `11000100000001`

Enter the results of the last operation in hexadecimal: `3101`
```python
bin(0b01000001+0b11000001).lstrip("0b") # question 1
bin(0b01000001|0b11000001).lstrip("0b") # question 2
bin(0b11000001>>1)                      # question 3
bin(0b01000001&0b11000001).lstrip("0b") # question 4
bin(0b01000001<<1)                      # question 5
bin(0b01000001*0b11000001)              # question 6
hex(int(bin(0b01000001*0b11000001),2))  # Last
```


flag: `picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}`