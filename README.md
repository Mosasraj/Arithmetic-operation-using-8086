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
| 2000:12                 | 2004:24                  |
| 2001:34                 | 2005:68                  |
| 2002:12                 | 2006:00                  |
| 2003:34                 | 2007:D6                  |


#### Manual Calculations

![WhatsApp Image 2025-09-01 at 19 42 42_d89da4f6](https://github.com/user-attachments/assets/ab13fdcf-78bd-4188-b35f-3d429c145552)



---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="642" height="393" alt="image" src="https://github.com/user-attachments/assets/35f93cbb-d8fa-4e1a-b91f-ccbe3aec6670" />


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
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
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
| 1200 : 12               | 1204 : 00                |
| 1201 : 34               | 1205 : 00                |
| 1202 : 12               | 1206 : 00                |
| 1203 : 34               | 1207 : C4                |


#### Manual Calculations

![WhatsApp Image 2025-09-01 at 19 34 31_b4af468d](https://github.com/user-attachments/assets/65e98b09-0d83-44e0-b130-8d2711a4eead)


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="635" height="377" alt="image" src="https://github.com/user-attachments/assets/b523a7a0-45b4-499e-bdc3-34e6379e5a9d" />


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
MOV SI,1200H
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
| 1200 : 12               | 1204 : 44                |
| 1201 : 34               | 1205 : 51                |
| 1202 : 12               | 1206 : 97                |
| 1203 : 34               | 1207 : 0A                |

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 19 34 54_c462c8f8](https://github.com/user-attachments/assets/10ed97c7-3f43-4ce5-ba0c-7fc34c5e34b8)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="630" height="396" alt="image" src="https://github.com/user-attachments/assets/dd14902b-023d-4354-8963-4b5aa0b124ad" />

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
MOV SI,1200H
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
| 1200 : 12               | 1204 : 01                |
| 1201 : 34               | 1205 : 00                |
| 1202 : 12               | 1206 : 00                |
| 1203 : 34               | 1207 : 00                |

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 19 35 14_73338c11](https://github.com/user-attachments/assets/d41463d9-e7c8-4438-8f67-46a14ac6f667)


---
## OUTPUT FROM MASM SOFTWARE

<img width="626" height="381" alt="image" src="https://github.com/user-attachments/assets/029a7271-9bea-45d9-952a-e5057c30d63f" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
