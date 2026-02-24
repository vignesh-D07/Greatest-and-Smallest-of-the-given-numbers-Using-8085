# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP:CMP M
JNC NEXT
MOV A,M
NEXT:INX H
DCR C
JNZ LOOP
STA 4300H
HLT
```

## Output:
<img width="1821" height="867" alt="image" src="https://github.com/user-attachments/assets/06895865-c157-4bdc-aefd-598217a027d8" />
<img width="1846" height="854" alt="image" src="https://github.com/user-attachments/assets/1d59ceb1-4eed-47ee-90e2-8a792beb8045" />


## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP:CMP M
JC NEXT
MOV A,M
NEXT:INX H
DCR C
JNZ LOOP
STA 4301H
HLT
```

## Output:
<img width="1806" height="784" alt="image" src="https://github.com/user-attachments/assets/ef62b564-b764-468a-9aaa-fa085693669e" />
<img width="1817" height="764" alt="image" src="https://github.com/user-attachments/assets/5f0f0ae6-1663-4b3a-a3ea-1b00d07016fa" />



## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
