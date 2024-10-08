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


13 : We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly13.jpg" width="400"/>

What will be the value of EAX after the execution of the instruction, add eax, ebx?  

a) 00000012  
b) 00000034  
c) 00000046  
d) CCCCCCCC  

**Answer** c)

**Description**

After the execution of the instruction add eax, ebx, the value of ebx will get added to eax and it will become 00000046. (12 + 34)  

---
---


14 :We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly14.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, add eax, ebx?  

a) 012713EA  
b) 012713E3  
c) 012713E5  
d) 012713E8  

**Answer** a)

**Description**

After the execution of the instruction, add eax, ebx, EIP will be pointing to next instruction whose EIP is 012713EA, which is evident from the disassembly shown.  

---
---


15 : We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly15.jpg" width="400"/>

What will be the value of ESP after the execution of the instruction, add esp, 8?  

a) 0043FB78  
b) 0043FB74  
c) 0043FB70  
d) 0043FB7C  

**Answer** a)

**Description**

By the instruction add esp, 8  we are deallocating the stack memory we allocated by the two push instructions at the beginning. So the value of ESP becomes 0043FB78.

---
---


16 : We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly16.jpg" width="400"/>  

What will be the fate of the above program?  

a) Program will crash  
b) Program will not crash  
c) Nothing will happen  
d) None of the above  

**Answer** b)

**Description**

The above program will not crash as we are deallocating (add esp, 8) the stack memory back after we have used it andso it is a legal program.

---
---


17 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov ecx, 4
        cmp edx, ecx
        jge label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002FFE60 EIP = 00D713E5 ESP = 002FFD88 EBP = 002FFE60 EFL = 00000210

Relevant memory is the following,

0x002FFD7C fa 36 2d 77  
0x002FFD80 f2 32 2d 77  
0x002FFD84 a8 7e 76 00  
0x002FFD88 00 00 00 00  
0x002FFD8C 00 00 00 00  
0x002FFD90 00 e0 fd 7e  
0x002FFD94 cc cc cc cc  
0x002FFD98 cc cc cc cc   
0x002FFD9C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly17.jpg" width="400"/>  

What will be the value of ECX after the execution of the instruction mov ecx, 4?  

a) CCCCCCCC  
b) 00000000  
c) 00000004  
d) None of the above  

**Answer** b)

**Description**

By the instruction mov ecx, 4 we are moving the value 4 to ECX, so it will become 00000004.  

---
---


18 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov ecx, 4
        cmp edx, ecx
        jge label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002FFE60 EIP = 00D713E5 ESP = 002FFD88 EBP = 002FFE60 EFL = 00000210

Relevant memory is the following,

0x002FFD7C fa 36 2d 77  
0x002FFD80 f2 32 2d 77  
0x002FFD84 a8 7e 76 00  
0x002FFD88 00 00 00 00  
0x002FFD8C 00 00 00 00  
0x002FFD90 00 e0 fd 7e  
0x002FFD94 cc cc cc cc  
0x002FFD98 cc cc cc cc  
0x002FFD9C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly18.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction mov ecx, 4?  

a) 00D713E5  
b) 00D713EA  
c) 00D713EC  
d) 00D713EE  

**Answer** b)

**Description**

After the instruction mov ecx, 4 the EIP will be pointing to next instruction which is 00D713EA and it is evident from the disassembly.  

---
---


19 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov ecx, 4
        cmp edx, ecx
        jge label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002FFE60 EIP = 00D713E5 ESP = 002FFD88 EBP = 002FFE60 EFL = 00000210

Relevant memory is the following,

0x002FFD7C fa 36 2d 77  
0x002FFD80 f2 32 2d 77  
0x002FFD84 a8 7e 76 00  
0x002FFD88 00 00 00 00  
0x002FFD8C 00 00 00 00  
0x002FFD90 00 e0 fd 7e  
0x002FFD94 cc cc cc cc  
0x002FFD98 cc cc cc cc  
0x002FFD9C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly19.jpg" width="400"/>  

Which Flag/s will get set after the instruction cmp edx, ecx in the above program?  

a) Sign flag  
b) Carry flag  
c) Zero flag  
d) Both a & b  

**Answer** d)

**Description**

cmp edx, ecx is subtracting ecx from edx, so 1 – 4, which is a negative value. So the Sign flag will become 1. Also the entire register will overflow and Carry flag will also get set. Jge checks the condition Sign flag = Overflow flag.  

---
---


20 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov ecx, 4
        cmp edx, ecx
        jge label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002FFE60 EIP = 00D713E5 ESP = 002FFD88 EBP = 002FFE60 EFL = 00000210

Relevant memory is the following,

0x002FFD7C fa 36 2d 77  
0x002FFD80 f2 32 2d 77  
0x002FFD84 a8 7e 76 00  
0x002FFD88 00 00 00 00  
0x002FFD8C 00 00 00 00  
0x002FFD90 00 e0 fd 7e  
0x002FFD94 cc cc cc cc  
0x002FFD98 cc cc cc cc  
0x002FFD9C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly20.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, cmp edx, ecx in the above program?  

a) 00D713E5  
b) 00D713EA  
c) 00D713EC  
d) 00D713EE  

**Answer** c)

**Description**

After the instruction, cmp edx, ecx the EIP will be pointing to next instruction which is 00D713EC and it is evident from the disassembly.  

---
---


21 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov ecx, 4
        cmp edx, ecx
        jge label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002FFE60 EIP = 00D713E5 ESP = 002FFD88 EBP = 002FFE60 EFL = 00000210

Relevant memory is the following,

0x002FFD7C fa 36 2d 77  
0x002FFD80 f2 32 2d 77  
0x002FFD84 a8 7e 76 00  
0x002FFD88 00 00 00 00  
0x002FFD8C 00 00 00 00  
0x002FFD90 00 e0 fd 7e  
0x002FFD94 cc cc cc cc  
0x002FFD98 cc cc cc cc  
0x002FFD9C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly21.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, jge label1 in the above program?  

a) 00D713E5  
b) 00D713EA  
c) 00D713EC  
d) 00D713EE  

**Answer** d)

**Description**

Here after the instruction, jge label1, it will not jump as the value of edx is not greater than or equal to the value of ecx. So EIP will be pointing to next instruction whose EIP is 00D713EE, not to label1.   

---
---


22 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov ecx, 6
        cmp edx, ecx
        jle label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001AF8EC EIP = 011C13E5 ESP = 001AF814 EBP = 001AF8EC EFL = 00000200

Relevant memory is the following,

0x001AF808 fa 36 97 77  
0x001AF80C f2 32 97 77  
0x001AF810 a8 7e 36 00  
0x001AF814 00 00 00 00  
0x001AF818 00 00 00 00  
0x001AF81C 00 e0 fd 7e  
0x001AF820 cc cc cc cc  
0x001AF824 cc cc cc cc  
0x001AF828 cc cc cc cc  
0x001AF82C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly22.jpg" width="400"/>  

What will be the value of ECX after the execution of the instruction mov ecx, 6?  

a) CCCCCCCC  
b) 00000000  
c) 00000006  
d) None of the above  

**Answer** c)

**Description**

By the instruction mov ecx, 6 we are moving the value 6 to ECX, so it will become 00000006.  

---
---


23 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov ecx, 6
        cmp edx, ecx
        jle label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001AF8EC EIP = 011C13E5 ESP = 001AF814 EBP = 001AF8EC EFL = 00000200

Relevant memory is the following,

0x001AF808 fa 36 97 77  
0x001AF80C f2 32 97 77  
0x001AF810 a8 7e 36 00  
0x001AF814 00 00 00 00  
0x001AF818 00 00 00 00  
0x001AF81C 00 e0 fd 7e   
0x001AF820 cc cc cc cc  
0x001AF824 cc cc cc cc  
0x001AF828 cc cc cc cc  
0x001AF82C cc cc cc cc  


Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly23.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov ecx, 6?  

a) 011C13DE  
b) 011C13E5  
c) 011C13EA  
d) 011C13EC  

**Answer** c)

**Description**

After the instruction mov ecx, 6 the EIP will be pointing to next instruction, which is 011C13EA  and it is evident from the disassembly.  

---
---


24 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov ecx, 6
        cmp edx, ecx
        jle label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001AF8EC EIP = 011C13E5 ESP = 001AF814 EBP = 001AF8EC EFL = 00000200

Relevant memory is the following,

0x001AF808 fa 36 97 77    
0x001AF80C f2 32 97 77  
0x001AF810 a8 7e 36 00  
0x001AF814 00 00 00 00  
0x001AF818 00 00 00 00  
0x001AF81C 00 e0 fd 7e  
0x001AF820 cc cc cc cc    
0x001AF824 cc cc cc cc    
0x001AF828 cc cc cc cc  
0x001AF82C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly24.jpg" width="400"/>

 Which Flag/s will get set after the instruction cmp edx, ecx in the above program?  

 a) Sign flag  
 b) Carry flag  
 c) Zero flag  
 d) Both a & b  

 **Answer** d)

**Description**

cmp edx, ecx is subtracting ecx from edx, so 1 – 6, which is a negative value. So the Sign flag will become 1. Also the entire register will overflow and Carry flag will also get set.  

---
---


25 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov ecx, 6
        cmp edx, ecx
        jle label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001AF8EC EIP = 011C13E5 ESP = 001AF814 EBP = 001AF8EC EFL = 00000200

Relevant memory is the following,

0x001AF808 fa 36 97 77  
0x001AF80C f2 32 97 77  
0x001AF810 a8 7e 36 00  
0x001AF814 00 00 00 00  
0x001AF818 00 00 00 00  
0x001AF81C 00 e0 fd 7e  
0x001AF820 cc cc cc cc  
0x001AF824 cc cc cc cc  
0x001AF828 cc cc cc cc  
0x001AF82C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly25.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, cmp edx, ecx in the above program?  

a) 011C13DE  
b) 011C13E5  
c) 011C13EA  
d) 011C13EC  

 **Answer** d)

**Description**

After the instruction, cmp edx, ecx the EIP will be pointing to next instruction which is 011C13EC  and it is evident from the disassembly.  

---
---


26 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov ecx, 6
        cmp edx, ecx
        jle label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001AF8EC EIP = 011C13E5 ESP = 001AF814 EBP = 001AF8EC EFL = 00000200

Relevant memory is the following,

0x001AF808 fa 36 97 77  
0x001AF80C f2 32 97 77  
0x001AF810 a8 7e 36 00  
0x001AF814 00 00 00 00  
0x001AF818 00 00 00 00  
0x001AF81C 00 e0 fd 7e  
0x001AF820 cc cc cc cc  
0x001AF824 cc cc cc cc  
0x001AF828 cc cc cc cc  
0x001AF82C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_52_AssemblyMultipleInstructionPractice_mov_add_sub_push_jmp/Images/Q_52_Disassembly26.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jle label1 in the above program?  

a) 011C13DE  
b) 011C13E5  
c) 011C13EA  
d) 011C13EE  

 **Answer** a)

**Description**

Here after the instruction, jle label1, it will jump as the value of edx is less than or equal to the value of ecx. So EIP will be pointing to label1, not to next instruction. 

---
---





