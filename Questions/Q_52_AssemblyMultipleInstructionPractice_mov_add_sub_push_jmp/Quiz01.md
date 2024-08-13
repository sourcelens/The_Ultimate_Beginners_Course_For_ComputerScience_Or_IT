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
<img src="" width="400"/>  

What will be the value of ESP after the execution of the first instruction push 0x12?
