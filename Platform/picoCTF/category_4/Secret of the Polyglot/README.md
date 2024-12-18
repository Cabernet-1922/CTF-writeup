# Secret of the Polyglot [Easy] (by syreal) - picoCTF 2024
> The Network Operations Center (NOC) of your local institution picked up a
suspicious file, they're getting conflicting information on what type of file
it is. They've brought you in as an external expert to examine the file. Can
you extract all the information from this strange file?</p>
Download the suspicious file <a href='https://artifacts.picoctf.net/c_titan/96/flag2of2-final.pdf' download>here</a>.</p>

Open the pdf file we can see half part of the flag: `1n_pn9_&_pdf_90974127}`. Then we `binwalk flag2of2-final.pdf`:
```text
DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 50 x 50, 8-bit/color RGBA, non-interlaced
914           0x392           PDF document, version: "1.4"
1149          0x47D           Zlib compressed data, default compression
```
That means there is a hidden png, it gives another half part of the flag: `picoCTF{f1u3n7_`

flag: `picoCTF{f1u3n7_1n_pn9_&_pdf_90974127}`
