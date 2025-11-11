
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**

**MEMORY WINDOW:**

Before execution: D:0x40H:
![WhatsApp Image 2025-10-26 at 21 20 04_5db0bb2a](https://github.com/user-attachments/assets/2797332d-3511-4030-a691-f7ce1fcd9177)

<BR>
<BR>
<BR>
After execution: D:0x40H:

![WhatsApp Image 2025-11-05 at 16 06 04_ae1deec3](https://github.com/user-attachments/assets/48a6dca3-4221-47a1-a638-97fffbc25ad3)



<BR>
<BR>
<BR>


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
![WhatsApp Image 2025-11-05 at 16 06 19_021f38a6](https://github.com/user-attachments/assets/2fb857dd-491e-4116-8d38-81051e8e4e47)

<BR>
<BR>
<BR>
<BR>
After execution:
D:0x40H:

![WhatsApp Image 2025-11-05 at 16 06 34_0fc8f19a](https://github.com/user-attachments/assets/e8060d6e-8ca1-4d00-aead-c466bd116438)

<BR>
<BR>
<BR>
**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

