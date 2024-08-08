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
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0016FB9C EIP = 00B513E5 ESP = 0016FAC4 EBP = 0016FB9C EFL = 00000200 

Flags are the following,

OV = 0 UP = 0 EI = 1 PL = 0 ZR = 0 AC = 0 PE = 0 CY = 0

Relevant memory is the following,

0x0016FAB8 fa 36 00 77  
0x0016FABC f2 32 00 77  
0x0016FAC4 00 00 00 00  
0x0016FAC8 00 00 00 00  
0x0016FACC 00 e0 fd 7e  
0x0016FAD0 cc cc cc cc  
0x0016FAD4 cc cc cc cc  
0x0016FAD8 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_49_AssemblySingleInstructionPractice_jmp_eflags_ret/Images/Q_49_Disassembly1.jpg" width="400"/>  

What will happen in the above program after the execution of the instruction, jz label1?  

a) Jump to label1  
b) Will not jump to label1, execute next instruction  
c) ESP will change  
d) Not enough information to answer  

**Answer** b)

**Description**

In the above instruction the Zero flag is 0, (ZR = 0) not 1, which means that it is not set and the result of the previous operation is not zero. So it will not jump to label1, but execute the next instruction. In the disassembly it is given je. It is same as jz, that is jump on zero means both values are equal.

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
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0016FB9C EIP = 00B513E5 ESP = 0016FAC4 EBP = 0016FB9C EFL = 00000200 

Flags are the following,

OV = 0 UP = 0 EI = 1 PL = 0 ZR = 0 AC = 0 PE = 0 CY = 0 

Relevant memory is the following,

0x0016FAB8 fa 36 00 77  
0x0016FABC f2 32 00 77  
0x0016FAC0 28 7f 5b 00  
0x0016FAC4 00 00 00 00  
0x0016FAC8 00 00 00 00  
0x0016FACC 00 e0 fd 7e  
0x0016FAD0 cc cc cc cc  
0x0016FAD4 cc cc cc cc  
0x0016FAD8 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_49_AssemblySingleInstructionPractice_jmp_eflags_ret/Images/Q_49_Disassembly2.jpg" width="400"/>  

What will be the value of EIP after the instruction, jz label1 in the above program?  

a) 00B513E7  
b) 00B513DE  
c) 00B513E5  
d) 00B513E9  

**Answer** a)

**Description**

In the above instruction the Zero flag is 0, (ZR = 0) not 1, which means that it is not set and the result of the previous operation is not zero. So it will not jump to label1, but execute the next instruction. So the EIP will be that of the next instruction which is 00B513E7, which is evident from the disassembly. In the disassembly it is given je. It is same as jz, that is jump on zero means both values are equal. 

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
        jnz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 004DF840 EIP = 003513E5 ESP = 004DF768 EBP = 004DF840 EFL = 00000214 

Flags are the following,

OV = 0 UP = 0 EI = 1 PL = 0 ZR = 0 AC = 1 PE = 1 CY = 0 

Relevant memory is the following,

0x004DF75C fa 36 03 77  
0x004DF760 f2 32 03 77  
0x004DF764 28 7f 80 00  
0x004DF768 00 00 00 00  
0x004DF76C 00 00 00 00  
0x004DF770 00 e0 fd 7e  
0x004DF774 cc cc cc cc  
0x004DF778 cc cc cc cc  
0x004DF77C cc cc cc cc   

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_49_AssemblySingleInstructionPractice_jmp_eflags_ret/Images/Q_49_Disassembly3.jpg" width="400"/>  

What will happen in the above program after the execution of the instruction, jnz label1?  

a) Jump to label1  
b) Will not jump to label1, execute next instruction  
c) ESP will change  
d) Not enough information to answer  

**Answer** a)

**Description**

In the above instruction the Zero flag is 0, (ZR = 0) not 1, which means that it is not set and the result of the previous operation is not zero. So it will jump to label1, because it is jump non-zero (jnz). In the disassembly it is given jne. It is same as jnz, that is jump on non zero means both values are not equal.    

---
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
        jnz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 004DF840 EIP = 003513E5 ESP = 004DF768 EBP = 004DF840 EFL = 00000214 

Flags are the following,

OV = 0 UP = 0 EI = 1 PL = 0 ZR = 0 AC = 1 PE = 1 CY = 0 

Relevant memory is the following,

0x004DF75C fa 36 03 77  
0x004DF760 f2 32 03 77  
0x004DF764 28 7f 80 00  
0x004DF768 00 00 00 00  
0x004DF76C 00 00 00 00  
0x004DF770 00 e0 fd 7e  
0x004DF774 cc cc cc cc  
0x004DF778 cc cc cc cc  
0x004DF77C cc cc cc cc   

Disassembly is the following,  
<img src="" width="400"/>

What will be the value of EIP after the instruction, jnz label1 in the above program?


