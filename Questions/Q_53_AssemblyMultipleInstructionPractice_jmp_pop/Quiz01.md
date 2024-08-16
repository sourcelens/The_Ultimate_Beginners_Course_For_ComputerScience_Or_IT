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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_2.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov esi, 1?  

a) 011B13DE  
b) 011B13E5  
c) 011B13EA  
d) 011B13EC  

**Answer** c) 

**Description**

After the instruction mov esi, 1 the EIP will be pointing to next instruction, which is 011B13EA  and it is evident from the disassembly.  

---
---


3 : We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_3.jpg" width="400"/>

Which Flag/s will get set after the instruction cmp edx, esi in the above program?  

a) Sign flag  
b) Carry flag  
c) Zero flag  
d) Both a & b  

**Answer** c) 

**Description**

cmp edx, esi is subtracting esi from edx, so 1 – 1, which is 0. So the Zero flag will become 1.   

---


4 : We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q-53_4.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, cmp edx, esi in the above program?  

a) 011B13DE  
b) 011B13E5  
c) 011B13EA  
d) 011B13EC  

**Answer** d) 

**Description**

After the instruction, cmp edx, esi the EIP will be pointing to next instruction which is 011B13EC  and it is evident from the disassembly. Je (jump equal to) shown in the disassembly is same as jz in the program, as jump on zero means both values are equal.  

---
---


5 : We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_5.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz label1 in the above program?  

a) 011B13DE  
b) 011B13E5  
c) 011B13EA  
d) 011B13EE  

**Answer** a) 

**Description**

Here after the instruction, jz label1, it will jump as Zero flag is 1 and the value of the comparison is 0. So EIP will be pointing to label1, not to next instruction, which is 011B13DE.  Je (jump equal to) shown in the disassembly is same as jz in the program, as jump on zero means both values are equal.

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov esi, 3
        cmp edx, esi
        jnz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003AFEAC EIP = 009D13E5 ESP = 003AFDD4 EBP = 003AFEAC EFL = 00000200

Relevant memory is the following,

0x003AFDC8 fa 36 97 77  
0x003AFDCC f2 32 97 77  
0x003AFDD0 a8 7e 79 00  
0x003AFDD4 00 00 00 00  
0x003AFDD8 00 00 00 00  
0x003AFDDC 00 e0 fd 7e  
0x003AFDE0 cc cc cc cc  
0x003AFDE4 cc cc cc cc  

Disassembly is the following,  

<img src="" width="400"/>

What will be the value of ESI after the execution of the instruction mov esi, 3?
