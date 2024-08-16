---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {
        mov esi, 1
        cmp edx, esi
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0042FE04 EIP = 011B13E5 ESP = 0042FD2C EBP = 0042FE04 EFL = 00000210

Relevant memory is the following,

0x0042FD20 fa 36 97 77   
0x0042FD24 f2 32 97 77  
0x0042FD28 a8 7e 57 00  
0x0042FD2C 00 00 00 00  
0x0042FD30 00 00 00 00  
0x0042FD34 00 e0 fd 7e  
0x0042FD38 cc cc cc cc  
0x0042FD3C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_1.jpg" width="400"/>

What will be the value of ESI after the execution of the instruction mov esi, 1?  

a) CCCCCCCC  
b) 00000000  
c) 00000001  
d) None of the above  

**Answer** c) 

**Description**  

By the instruction mov esi, 1 we are moving the value 1 to ESI, so it will become 00000001.  

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {
        mov esi, 1
        cmp edx, esi
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0042FE04 EIP = 011B13E5 ESP = 0042FD2C EBP = 0042FE04 EFL = 00000210

Relevant memory is the following,

0x0042FD20 fa 36 97 77  
0x0042FD24 f2 32 97 77  
0x0042FD28 a8 7e 57 00  
0x0042FD2C 00 00 00 00  
0x0042FD30 00 00 00 00  
0x0042FD34 00 e0 fd 7e  
0x0042FD38 cc cc cc cc  
0x0042FD3C cc cc cc cc   

Disassembly is the following,  

<img src="" width="400"/>

What will be the value of EIP after the execution of the instruction mov esi, 1?
