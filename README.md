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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

<img width="899" height="811" alt="image" src="https://github.com/user-attachments/assets/9067e98b-38fe-49a6-a074-974b341075de" />
<img width="1360" height="818" alt="image" src="https://github.com/user-attachments/assets/db4682c0-68f3-418c-b405-71fb00b59e94" />


#### Manual Calculations

<img width="1014" height="758" alt="image" src="https://github.com/user-attachments/assets/484f1911-9e8e-4ca6-acda-c97365499a54" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="1168" height="775" alt="image" src="https://github.com/user-attachments/assets/5548d85e-d25d-426e-8215-f33ba040873b" />


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

<img width="1091" height="771" alt="image" src="https://github.com/user-attachments/assets/18f631a2-4ddf-41e4-ab02-d1d01add85e4" />


#### Manual Calculations

<img width="1251" height="797" alt="image" src="https://github.com/user-attachments/assets/db1cd145-6050-4524-a478-972fd852716a" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="1196" height="813" alt="image" src="https://github.com/user-attachments/assets/f1b0c020-ccfa-4722-8d60-b6e51ef03506" />


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

<img width="1082" height="769" alt="image" src="https://github.com/user-attachments/assets/802fd3a8-856e-4c31-9e02-26ecfd901ae9" />


#### Manual Calculations

<img width="1034" height="795" alt="image" src="https://github.com/user-attachments/assets/88810a25-ec63-4f0a-bb4f-9bb96106ebf0" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="1224" height="807" alt="image" src="https://github.com/user-attachments/assets/e8966173-db01-421c-b90b-0fcd871d9068" />


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

<img width="1011" height="743" alt="image" src="https://github.com/user-attachments/assets/a537dad2-cd09-49e6-9bec-9e112c51a9cf" />


#### Manual Calculations

<img width="1248" height="669" alt="image" src="https://github.com/user-attachments/assets/80b39c4b-cb47-441b-a563-da36e6b5d345" />


---
## OUTPUT FROM MASM SOFTWARE

<img width="1208" height="798" alt="image" src="https://github.com/user-attachments/assets/53f31cfa-3f8f-4294-9918-9f59ccfd4d0f" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

