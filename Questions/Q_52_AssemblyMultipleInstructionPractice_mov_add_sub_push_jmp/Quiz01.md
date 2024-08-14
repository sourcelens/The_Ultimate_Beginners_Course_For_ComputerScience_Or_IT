---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly1.jpg" width="400"/>  
What will change after the execution of the first instruction push 0x12?    

a) ESP  
b) EIP  
c) Value of memory location 0x0043FB74  
d) All of the above  

**Answer** d)

**Description**

Push 0x12 instruction is effectively, sub esp, 4 and mov dword ptr[esp], 0x12. So ESP will change. EIP will be pointing to next instruction, so it will change. Also the value of the memory location 0x0043FB74 will become 0x12.  

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly2.jpg" width="400"/>  

What will be the value of ESP after the execution of the first instruction push 0x12?  

a) 0043FB78  
b) 0043FB74  
c) 0043FB70  
d) 0043FB7C  

**Answer** b)

**Description**

Push 0x12 instruction is effectively, sub esp, 4 and mov dword ptr[esp], 0x12. So ESP will get decremented and become 0043FB74.

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly3.jpg" width="400"/>  

What will be the value of EIP after the execution of the first instruction, push 0x12?  

a) 012713E0  
b) 012713E3  
c) 012713E5  
d) 012713E8  

**Answer** a)

**Description**

After the execution of the first instruction, push 0x12, EIP will be pointing to next instruction whose EIP is 012713E0, which is evident from the disassembly shown.   

---
---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00   
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly4.jpg" width="400"/>  

What will be the value of the memory location 0x0043FB74 after the execution of the first instruction, push 0x12?  

a) 00000000  
b) 00000012  
c) 012713E0  
d) None of the above  

**Answer** b)

**Description**

Push 0x12 instruction is effectively, sub esp, 4 and mov dword ptr[esp], 0x12. So the value of the memory location 0x0043FB74 will become 00000012.  

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly5.jpg" width="400"/>  

What will be the value of EAX after the execution of the second instruction, mov eax, dword ptr[esp]?  

a) 00000012  
b) 00000034  
c) 00000046  
d) None of the above  

**Answer** a)

**Description**

The second instruction mov eax, dword ptr[esp] will move the value of [esp] to eax which will then become 00000012.  

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly6.jpg" width="400"/>  

What will be the value of EIP after the execution of the second instruction, mov eax, dword ptr[esp]?  

a) 012713E0  
b) 012713E3  
c) 012713E5  
d) 012713E8  

**Answer** b)

**Description**

After the execution of the second instruction, mov eax, dword ptr[esp], EIP will be pointing to next instruction whose EIP is 012713E3, which is evident from the disassembly shown.  

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e   
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly7.jpg " width="400"/>  

What will change after the execution of the third instruction push 0x34?  

a) ESP  
b) EIP  
c) Value of memory location 0x0043FB70  
d) All of the above  

**Answer** d)

**Description**

Push 0x34 instruction is effectively, sub esp, 4 and mov dword ptr[esp], 0x34. So ESP will change. EIP will be pointing to next instruction, so it will change. Also the value of the memory location 0x0043FB70 will become 0x34.  

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly8.jpg" width="400"/>    

What will be the value of ESP after the execution of the third instruction, push 0x34?  

a) 0043FB78  
b) 0043FB74  
c) 0043FB70  
d) 0043FB7C  

**Answer** c)

**Description**

Push 0x34 instruction is effectively, sub esp, 4 and mov dword ptr[esp], 0x34. So ESP will change and become 0043FB70.  

---
---


9 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly9.jpg" width="400"/>    

What will be the value of EIP after the execution of the third instruction, push 0x34?  

a) 012713E0  
b) 012713E3  
c) 012713E5  
d) 012713E8  

**Answer** c)

**Description**

After the execution of the third instruction, push 0x34, EIP will be pointing to next instruction whose EIP is 012713E5, which is evident from the disassembly shown.   

---
---


10 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly10.jpg" width="400"/>  

What will be the value of the memory location 0x0043FB70 after the execution of the third instruction, push 0x34?  

a) 00000000  
b) 00000012  
c) 00000034  
d) None of the above  

**Answer** c)

**Description**

Push 0x34 instruction is effevtively, sub esp, 4 and mov dword ptr[esp], 0x34. So the value of the memory location 0x0043FB70 will become 00000034.

---
---


11 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly11.jpg" width="400"/>  

What will be the value of EBX after the execution of the instruction, mov ebx, dword ptr[esp]?  

a) 00000012  
b) 00000034  
c) 00000046  
d) None of the above  

**Answer** c)

**Description**

The fourth instruction mov ebx, dword ptr[esp] will move the value of [esp] to ebx, which will become 00000034.  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 0x12
        mov eax, dword ptr[esp]
        push 0x34
        mov ebx, dword ptr[esp]
        add eax, ebx
        add esp, 8
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FC44 EIP = 012713DE ESP = 0043FB78 EBP = 0043FC44 EFL = 00000204

Relevant memory is the following,

0x0043FB6C b8 7e 88 00  
0x0043FB70 00 00 00 00  
0x0043FB74 00 00 00 00  
0x0043FB78 00 00 00 00  
0x0043FB7C 00 00 00 00  
0x0043FB80 00 e0 fd 7e  
0x0043FB84 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly12.jpg" width="400"/>
  
What will be the value of EIP after the execution of the instruction, mov ebx, dword ptr[esp]?  

a) 012713E0  
b) 012713E3  
c) 012713E5  
d) 012713E8  

**Answer** d)

**Description**

After the execution of the instruction, mov ebx, dword ptr[esp], EIP will be pointing to next instruction whose EIP is 012713E8, which is evident from the disassembly shown.  

---
---


13 : 


