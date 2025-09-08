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
|      1200:12            | 1204:24                  |
|1201:34                  | 1205:68                  |
1202:12                   |  1206:00
1203:34                   |  1207:C4
#### Manual Calculations

![WhatsApp Image 2025-09-02 at 23 49 15_395ff71a](https://github.com/user-attachments/assets/a4fb3a5d-e3a2-4b8c-a18b-3a605cdd4b4b)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="633" height="431" alt="image" src="https://github.com/user-attachments/assets/cd654097-0290-4a13-a0b4-e0feb03e991b" />

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
MOV SI,2000H
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
|      1200:12                   |         1204:00   |
  1201:34        | 1205:00 
  1202:12        | 1206:00 
  1203:34        |1207:c4|

#### Manual Calculations
![WhatsApp Image 2025-09-02 at 23 55 25_ddfc1868](https://github.com/user-attachments/assets/d767725c-53b7-46bd-8b9e-9c42a081f9b8)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="940" height="627" alt="image" src="https://github.com/user-attachments/assets/6d03e332-ffc6-4699-a096-c7c2da802c56" />



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
| 1200:12              |     1204:44                     |
1201:34|1205:51 
1202:12 | 1206:97 
1203:34 |1207:0A
#### Manual Calculations
![WhatsApp Image 2025-09-03 at 00 44 12_dfe522c5](https://github.com/user-attachments/assets/57296cf3-659d-4826-be84-043e167429ac)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="940" height="626" alt="image" src="https://github.com/user-attachments/assets/a530a5cb-f02f-4c05-938d-857abc2968f4" />



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
| 1200:12                 | 1204:01       
1201:34                   |1205:00 
1202:12                   |1206:00 
1203:34                   |1207:00 |

#### Manual Calculations
![WhatsApp Image 2025-09-03 at 01 02 51_08fc5e17](https://github.com/user-attachments/assets/f133f5aa-49d1-4b7e-bb8f-c88d33d7ca0d)


---
## OUTPUT FROM MASM SOFTWARE
<img width="940" height="627" alt="image" src="https://github.com/user-attachments/assets/5aec6c19-44bb-4210-86b8-d944e44630d8" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
