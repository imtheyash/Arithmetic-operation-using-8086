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
| 1200:12                            1204:24
  1201:34----------------------- | - 1205:68----------------------- |
| 1202:12                       |                          |
  1203:34
#### Manual Calculations
![WhatsApp Image 2025-08-26 at 13 03 20_72476653](https://github.com/user-attachments/assets/990a3d21-6b28-408c-8d7f-81af5562fb7e)

(Add your calculation here)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/9b28d177-c43b-4bec-b57e-2feee9761dfb" />
<img width="640" height="480" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/d02fa21d-9a4d-450c-81e4-88152c57bbd5" />



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
code segment
assume cs:code,ds:code
org 1000h 
mov si, 1200h 
mov ax, [si]
mov bx, [si+02h]  
mov cl,00h 
sub ax, bx 
jnc 11 
inc cl 
11:mov[si+04h], ax 
mov [si+06h],cl 
mov ah,4ch
int 21h 
code ends 
end



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| 1200:12----------------------- | 1204:00------------------------ |
| 1201:34                       |  1205:00                        |
  1202:12
  1203:34
   
#### Manual Calculations
![WhatsApp Image 2025-08-26 at 13 03 21_5cdaf738](https://github.com/user-attachments/assets/f6cddbb0-00fe-495d-90ea-2964fb6bb4ab)

(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (15)" src="https://github.com/user-attachments/assets/27f06838-30e6-44e5-be57-f3fb44da582f" />
<img width="640" height="480" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/c1ba9b51-17ae-4d98-945c-95a61ed82927" />



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
| -1200:12---------------------- | 1204:44------------------------ |
|  1201:34                      |  1205:51                       |
   1202:12                         1206:97
   1203:34                         1207:OA
#### Manual Calculations
![WhatsApp Image 2025-08-26 at 13 03 21_7d2dc15a](https://github.com/user-attachments/assets/d30575f2-f17d-41bb-ba4a-f16a1775f0fe)

(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/c13cd18f-06f0-4547-9be8-22ef531ab0f5" />
<img width="640" height="480" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/b4bf9b95-d4d0-4f89-945c-7b5e26588190" />



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
| -1200:12---------------------- | 1204:01------------------------ |
|  1201:34                       | 1205:00                         |
   1202:12                          1206:00
   1203:34                          1207:00 
#### Manual Calculations
![WhatsApp Image 2025-08-26 at 13 03 22_c956ba73](https://github.com/user-attachments/assets/97afe8ab-a245-48e9-96f6-37bb5a13cf91)

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/54390627-62b5-4df0-9e3d-28f3777f7c8a" />
<img width="640" height="480" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/d0b65b3c-4b46-4dd5-9660-f7631569c08c" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
