# voiceCipher
### _a script using music21 Python Library_ 
This repository contains a Python script called voiceCipher that takes a music21 Score object as input and creates a notation in each Part (instrument part) wich ciphers the armonic movements (interval and type of motion) between each part and its contigious part. 
##### About Musc21
music21 -- A Toolkit for Computer-Aided Musical Analysis and Computational Musicology
https://github.com/cuthbertLab/music21
### Purpose
This script was created for pedagogical purposes, particularly for the practice, teaching and development of counterpoint. It can be a useful tool for checking students work.
# Example
Here is an example on Bach BWV 66.6: 
![voiceCipher example on Bach BWV 66.6](/bwv666-example.png "Bach BWV 66.6 - voiceCipher").

The cipher reflects harmonic intervals within voices and a symbol that matches each voice motion with a particular symbol:
- Oblique motion uses no symbol.
- Parallel motion uses "**=**".
- Contrary motion uses "**<**" and "**>**" for outward and inward, respectively.
- Direct motion uses "**↗**" if ascending and "**↘**" for descending movement.

In the example above the notation on the Soprano refers to the relation between Soprano and Alto; At alto part, the cipher corresponds to the relation Alto-Tenor and so on. Finally, Bass part cipher reflects Soprano-Bass relation.

# How to 
To use the script, import music21 and the voiceCipher function from the script. Then, call the voiceCipher function with a music score as its argument,
```
from music21 import *

score = corpus.parse('bwv66.6')
vcScore = voiceCipher(score)
vcScore.show()
```
for adding a system layout every 2 bars 
```
 vcScore = voiceCipher(score, measureBreak=2)
 ```