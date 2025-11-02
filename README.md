
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
<img width="1037" height="205" alt="image" src="https://github.com/user-attachments/assets/e3d1fd36-8064-4798-850d-b3c3d1576a5a" />
<img width="1720" height="518" alt="image" src="https://github.com/user-attachments/assets/f3106065-af2f-488e-bc99-724424873409" />

After execution: D:0x40H:
<img width="1537" height="597" alt="image" src="https://github.com/user-attachments/assets/482d4aee-a7d8-4cb2-bacb-3a833d001b96" />



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
<img width="1497" height="457" alt="image" src="https://github.com/user-attachments/assets/5398d63c-303b-4c5c-b9c5-905b7205514b" />
<img width="902" height="142" alt="image" src="https://github.com/user-attachments/assets/b9f2c268-83b1-4b12-bb24-5185e390a331" />
After execution:
D:0x40H:
<img width="1420" height="538" alt="Screenshot 2025-11-02 183153" src="https://github.com/user-attachments/assets/fed74b21-d6a5-49c2-8c6a-2f0b5eab3e2d" />

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

