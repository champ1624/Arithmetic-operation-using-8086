# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200h	1204h
1201h	1205h
1202h	1206h
1203h	-                    |                          |

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-08 at 22 17 17_84e8ed2d](https://github.com/user-attachments/assets/2f3f66a6-4cb6-4069-893a-f8313c378715)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-08 at 21 23 43_1f09ed5b](https://github.com/user-attachments/assets/2f824618-1c36-464c-b422-819990354b57)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200h	1204h
1201h	1205h
1202h	1206h
1203h	-              

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-08 at 22 17 17_7e1928b3](https://github.com/user-attachments/assets/b359a974-87f5-451a-bf4c-82e374ee1fe9)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-08 at 21 25 40_7827f7a9](https://github.com/user-attachments/assets/aee3de9a-cdcd-4c8c-8e65-ce89e74c916f)

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200h	1204h
1201h	1205h
1202h	1206h
1203h	1207h

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-08 at 22 17 16_9a264b33](https://github.com/user-attachments/assets/b01c1fcf-89d4-4dc9-822d-72f1d60958fa)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-08 at 21 27 31_49c5a2a8](https://github.com/user-attachments/assets/a062d2f3-e849-403a-a597-f1eeff0ab35f)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   1200h	1204h
1201h	1205h
1202h	1206h
1203h	1207h                      |                          |

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-08 at 22 17 16_393240ac](https://github.com/user-attachments/assets/57183eb4-2fe1-443d-9547-8599644367a9)

---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-08 at 21 31 20_6b327c3b](https://github.com/user-attachments/assets/8d9e9647-3b28-4c13-a612-f811ed4d952d)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
