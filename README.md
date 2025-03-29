# HUFFMAN-SHANNON-FANO
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
## AIM:
To apply the Huffman and Shannon-Fano to this source with symbols and statistics {0.125,0.0625,0.25,0.0625,0.125,0.125,0.25} for its output
## TOOLS REQUIRED:
Python IDE with Numpy and Scipy
## PROGRAM:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
## CACULATION:
![WhatsApp Image 2025-03-29 at 09 36 35_e5d3e245](https://github.com/user-attachments/assets/ba419bc7-1f4c-4d0c-aaa4-cab0f583e9e3)
![WhatsApp Image 2025-03-29 at 09 33 11_10da1b9d](https://github.com/user-attachments/assets/d6a56e97-7e1b-444b-9f4b-27a5c510ea63)
## OUTPUT:
![WhatsApp Image 2025-03-29 at 08 34 03_300920c3](https://github.com/user-attachments/assets/ccf0b692-d161-4cf8-9d95-65f7cba57049)
## RESULT:
The Huffman and Shannon-Fano of the given statistics {0.125,0.0625,0.25,0.0625,0.125,0.125,0.25} using python are verified
