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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_49_AssemblySingleInstructionPractice_jmp_eflags_ret/Images/Q_49_Disassembly4.jpg" width="400"/>  

What will be the value of EIP after the instruction, jnz label1 in the above program?  

a) 003513E7  
b) 003513DE  
c) 003513E9  
d) 003513DC  

**Answer** b)

**Description**

In the above instruction the Zero flag is 0, (ZR = 0) not 1, which means that it is not set and the result of the previous operation is not zero. So it will jump to label1, whose EIP is  003513DE, which is evident from the disassembly. In the disassembly it is given jne. It is same as jnz, that is jump on non zero means both values are not equal.    

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub ecx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0026F9F8 EIP = 013713DE ESP = 0026F92C EBP = 0026F9F8 EFL = 00000200 

Relevant memory is the following,

0x0026F920 b0 7e 5f 00  
0x0026F924 00 00 00 00  
0x0026F928 00 00 00 00  
0x0026F92C 00 00 00 00  
0x0026F930 00 00 00 00  
0x0026F934 00 e0 fd 7e  
0x0026F938 cc cc cc cc  
0x0026F93C cc cc cc cc  
0x0026F940 cc cc cc cc  

Which register/s will change after the execution of the line, sub ecx, 1 in the above program?  

a) EIP  
b) ECX  
c) EFL  
d) All of the above  

**Answer** d)

**Description**

Here ECX will change as we are subtracting a value from it. EIP changes after every instruction. EFL will also change as the Sign flag & Carry flag got set.

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub ecx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0026F9F8 EIP = 013713DE ESP = 0026F92C EBP = 0026F9F8 EFL = 00000200 

Relevant memory is the following,

0x0026F920 b0 7e 5f 00  
0x0026F924 00 00 00 00  
0x0026F928 00 00 00 00  
0x0026F92C 00 00 00 00  
0x0026F930 00 00 00 00  
0x0026F934 00 e0 fd 7e  
0x0026F938 cc cc cc cc  
0x0026F93C cc cc cc cc  
0x0026F940 cc cc cc cc  

What is the value of ECX after the line, sub ecx, 1 in the above program?  

a) 00000001  
b) 00000002  
c) FFFFFFFF (00000000 - 1)  
d) CCCCCCCC  

**Answer** c)

**Description**

In the above program we are subtracting 1 from the value of ECX, which is 0. So it will become FFFFFFFF. It is a negative integer which is -1.  

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub ecx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0026F9F8 EIP = 013713DE ESP = 0026F92C EBP = 0026F9F8 EFL = 00000200 

Relevant memory is the following,

0x0026F920 b0 7e 5f 00  
0x0026F924 00 00 00 00  
0x0026F928 00 00 00 00  
0x0026F92C 00 00 00 00  
0x0026F930 00 00 00 00  
0x0026F934 00 e0 fd 7e  
0x0026F938 cc cc cc cc  
0x0026F93C cc cc cc cc  
0x0026F940 cc cc cc cc  

What is the value of EIP after the line, sub ecx, 1 in the above program?  

a) 013713DE  
b) Point to next instruction  
c) Junk value  
d) None of the above  

**Answer** b)

**Description**

EIP will always point to the next instruction to execute.  

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub ecx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0026F9F8 EIP = 013713DE ESP = 0026F92C EBP = 0026F9F8 EFL = 00000200 

Relevant memory is the following,

0x0026F920 b0 7e 5f 00  
0x0026F924 00 00 00 00  
0x0026F928 00 00 00 00  
0x0026F92C 00 00 00 00  
0x0026F930 00 00 00 00  
0x0026F934 00 e0 fd 7e  
0x0026F938 cc cc cc cc  
0x0026F93C cc cc cc cc  
0x0026F940 cc cc cc cc   

Which Flag/s will get set after the instruction, sub ecx, 1 in the above program?  

a) Overflow flag  
b) Carry flag  
c) Sign flag  
d) Both b & c  

**Answer** d)

**Description**

Here the value of ECX is 0. So when 1 is subtracted from it, it will become -1, which is FFFFFFFF and the entire register overflows. So the Carry flag is set. Here the sign of the value becomes negative andso the Sign flag is also set.

---
---


9 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub edx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0036F798 EIP = 013E13DE ESP = 0036F6CC EBP = 0036F798 EFL = 00000204 

Relevant memory is the following,

0x0036F6C0 b0 7e 63 00  
0x0036F6C4 00 00 00 00  
0x0036F6C8 00 00 00 00  
0x0036F6CC 00 00 00 00  
0x0036F6D0 00 00 00 00  
0x0036F6D4 00 e0 fd 7e  
0x0036F6D8 cc cc cc cc  
0x0036F6DC cc cc cc cc  
0x0036F6E0 cc cc cc cc  

Which register/s will change after the execution of the line, sub edx, 1 in the above program?  

a) EIP  
b) EDX  
c) EFL  
d) All of the above  

**Answer** d)

**Description**

Here EDX will change as we are subtracting a value from it. EIP changes after every instruction. EFL will also change as the Zero flag got set because the result of the previous operation is 0.

---
---


10 : We have the below program,

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub edx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0036F798 EIP = 013E13DE ESP = 0036F6CC EBP = 0036F798 EFL = 00000204

Relevant memory is the following,

0x0036F6C0 b0 7e 63 00  
0x0036F6C4 00 00 00 00  
0x0036F6C8 00 00 00 00  
0x0036F6CC 00 00 00 00  
0x0036F6D0 00 00 00 00  
0x0036F6D4 00 e0 fd 7e  
0x0036F6D8 cc cc cc cc  
0x0036F6DC cc cc cc cc  
0x0036F6E0 cc cc cc cc  

What is the value of EDX after the line, sub edx, 1 in the above program?   

a) 00000001  
b) 00000002  
c) 00000000  
d) CCCCCCCC  

**Answer** c)

**Description**

In the above program we are subtracting 1 from the value of EDX, which is 1. So it will become 00000000.   

---
---


11 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub edx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0036F798 EIP = 013E13DE ESP = 0036F6CC EBP = 0036F798 EFL = 00000204

Relevant memory is the following,

0x0036F6C0 b0 7e 63 00  
0x0036F6C4 00 00 00 00  
0x0036F6C8 00 00 00 00  
0x0036F6CC 00 00 00 00  
0x0036F6D0 00 00 00 00  
0x0036F6D4 00 e0 fd 7e  
0x0036F6D8 cc cc cc cc  
0x0036F6DC cc cc cc cc  
0x0036F6E0 cc cc cc cc  

What is the value of EIP after the line, sub edx, 1 in the above program?  

a) 013713DE  
b) Point to next instruction  
c) Junk value  
d) None of the above  

**Answer** b)

**Description**

EIP will always point to the next instruction.  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub edx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0036F798 EIP = 013E13DE ESP = 0036F6CC EBP = 0036F798 EFL = 00000204

Relevant memory is the following,

0x0036F6C0 b0 7e 63 00  
0x0036F6C4 00 00 00 00  
0x0036F6C8 00 00 00 00  
0x0036F6CC 00 00 00 00  
0x0036F6D0 00 00 00 00  
0x0036F6D4 00 e0 fd 7e  
0x0036F6D8 cc cc cc cc  
0x0036F6DC cc cc cc cc  
0x0036F6E0 cc cc cc cc  

Which Flag/s will get set after the instruction, sub edx, 1 in the above program?  

a) Zero flag  
b) Sign flag  
c) Overflow flag  
d) Carry flag  

**Answer** a)

**Description**

Here the value of EDX is 1. So if 1 is subtracted from it, it will become 0 and that’s why Zero flag will get set. Sign flag will not get set as sign does not change. As no overflow happens for signed operations Overflow flag will not get set. Carry flag also will not get set, because there is no overflow happens for the entire register.  

---
---


13 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        add edx, 0x7FFFFFFF	
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0014FB2C EIP = 010F13DE ESP = 0014FA60 EBP = 0014FB2C EFL = 00000204

Relevant memory is the following,

0x0014FA60 00 00 00 00  
0x0014FA64 00 00 00 00  
0x0014FA68 00 e0 fd 7e  
0x0014FA6C cc cc cc cc  
0x0014FA70 cc cc cc cc  
0x0014FA74 cc cc cc cc  
0x0014FA78 cc cc cc cc  

Which register/s will change after the execution of the line, add edx, 0x7FFFFFFF in the above program?  

a) EIP  
b) EDX  
c) EFL  
d) All of the above  

**Answer** d)

**Description**

Here EDX will change as we are adding a value to it. EIP changes after every instruction. EFL will also change as the Sign flag & Overflow flag get set.  

---
---


14 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        add edx, 0x7FFFFFFF	
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0014FB2C EIP = 010F13DE ESP = 0014FA60 EBP = 0014FB2C EFL = 00000204

Relevant memory is the following,

0x0014FA60 00 00 00 00  
0x0014FA64 00 00 00 00  
0x0014FA68 00 e0 fd 7e  
0x0014FA6C cc cc cc cc  
0x0014FA70 cc cc cc cc  
0x0014FA74 cc cc cc cc  
0x0014FA78 cc cc cc cc  

What is the value of EDX after the line, add edx, 0x7FFFFFFF in the above program?  

a) 00000001  
b) 7FFFFFFF  
c) 80000000 (7FFFFFFF+1)  
d) FFFFFFFF  

**Answer** c)

**Description**

Here EDX is 1. So when 0x7FFFFFFF is added to it, it becomes 80000000, which is a negative integer. 7FFFFFFF is the maximum positive integer possible.  

---
---


15 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        add edx, 0x7FFFFFFF	
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0014FB2C EIP = 010F13DE ESP = 0014FA60 EBP = 0014FB2C EFL = 00000204

Relevant memory is the following,

0x0014FA60 00 00 00 00  
0x0014FA64 00 00 00 00  
0x0014FA68 00 e0 fd 7e  
0x0014FA6C cc cc cc cc  
0x0014FA70 cc cc cc cc  
0x0014FA74 cc cc cc cc  
0x0014FA78 cc cc cc cc  

What is the value of EIP after the line, add edx, 0x7FFFFFFF in the above program?  

a) 010F13DE  
b) Point to next instruction  
c) Junk value  
d) None of the above  

**Answer** b)

**Description**

EIP will always point to the next instruction.  

---
---


16 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        add edx, 0x7FFFFFFF	
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0014FB2C EIP = 010F13DE ESP = 0014FA60 EBP = 0014FB2C EFL = 00000204

Relevant memory is the following,

0x0014FA60 00 00 00 00  
0x0014FA64 00 00 00 00  
0x0014FA68 00 e0 fd 7e  
0x0014FA6C cc cc cc cc  
0x0014FA70 cc cc cc cc  
0x0014FA74 cc cc cc cc  
0x0014FA78 cc cc cc cc  

Which Flag/s will get set after the instruction, add edx, 0x7FFFFFFF in the above program?   

a) Zero flag  
b) Sign flag  
c) Overflow flag  
d) Both b & c  

**Answer** d)

**Description**

Ox7FFFFFFF is the maximum positive integer, so when 1 is added to it, it becomes 80000000, which is a negative integer. So the sign flag will get set. Overflow flag will also get set as overflow happens for positive integer.  

---
---


17 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FDE4 EIP = 00FE13DE ESP = 0043FD18 EBP = 0043FDE4 EFL = 00000204

Relevant memory is the following,

0x0043FD0C b0 7e 4f 00  
0x0043FD10 00 00 00 00  
0x0043FD14 00 00 00 00  
0x0043FD18 00 00 00 00  
0x0043FD1C 00 00 00 00  
0x0043FD20 00 e0 fd 7e  
0x0043FD24 cc cc cc cc  
0x0043FD28 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_49_AssemblySingleInstructionPractice_jmp_eflags_ret/Images/Q_49_Disassembly16.jpg" width="400"/>

Which register/s will change after the execution of the instruction, mov eax, edx in the above program?  

a) EDI  
b) EDX  
c) EAX  
d) All of the above  

**Answer** c)

**Description**

In the above program the value of edx will move to eax. So eax will become edx value. EDX & EDI registers will have no change.  

---
---


18 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FDE4 EIP = 00FE13DE ESP = 0043FD18 EBP = 0043FDE4 EFL = 00000204

Relevant memory is the following,

0x0043FD0C b0 7e 4f 00  
0x0043FD10 00 00 00 00  
0x0043FD14 00 00 00 00  
0x0043FD18 00 00 00 00  
0x0043FD1C 00 00 00 00  
0x0043FD20 00 e0 fd 7e  
0x0043FD24 cc cc cc cc  
0x0043FD28 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_49_AssemblySingleInstructionPractice_jmp_eflags_ret/Images/Q_49_Disassembly18.jpg" width="400"/>  

What is the value of EAX after the line, mov eax, edx in the above program?  

a) CCCCCCCC  
b) 00000001  
c) 00000000  
d) None of the above  

**Answer** b)

**Description**

In the above program the value of EDX, that is 1 will move to EAX. So it will become 00000001.  

---
---


19 : We have the below program,

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FDE4 EIP = 00FE13DE ESP = 0043FD18 EBP = 0043FDE4 EFL = 00000204

Relevant memory is the following,

0x0043FD0C b0 7e 4f 00  
0x0043FD10 00 00 00 00  
0x0043FD14 00 00 00 00  
0x0043FD18 00 00 00 00  
0x0043FD1C 00 00 00 00  
0x0043FD20 00 e0 fd 7e  
0x0043FD24 cc cc cc cc  
0x0043FD28 cc cc cc cc  

Disassembly is the following,  
<img src="" width="400"/>

What is the value of EDX after the line, mov eax, edx in the above program?  

a) CCCCCCCC  
b) 00000001  
c) 00000000  
d) None of the above  

**Answer** b)

**Description**

The EDX will have the same value as before. After the instruction, both EDX & EAX will have the same value.  

---
---


20 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0043FDE4 EIP = 00FE13DE ESP = 0043FD18 EBP = 0043FDE4 EFL = 00000204

Relevant memory is the following,

0x0043FD0C b0 7e 4f 00  
0x0043FD10 00 00 00 00  
0x0043FD14 00 00 00 00  
0x0043FD18 00 00 00 00  
0x0043FD1C 00 00 00 00  
0x0043FD20 00 e0 fd 7e  
0x0043FD24 cc cc cc cc  
0x0043FD28 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_49_AssemblySingleInstructionPractice_jmp_eflags_ret/Images/Q_49_Disassembly20.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov eax, edx in the above program?









