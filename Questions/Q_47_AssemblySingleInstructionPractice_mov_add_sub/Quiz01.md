---
---

1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        add dword ptr[esp], 0x7
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001FFE40 EIP = 011E13DE ESP = 001FFD74 EBP = 001FFE40 EFL = 00000200 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

Which will change after the instruction, add dword ptr[esp], 0x7 in the above program?  

a) ESP  
b) Value of the memory location 0x001FFD74  
c) No change  
d) Value of the memory location 0x001FFD78  

**Answer** b) 

**Description**  

Here we are adding 0x7 to the value of the memory location [esp], that is 0x001FFD74. So it will change. ESP will have no change because we are changing the value inside the memory location which is pointed by ESP which is equal to 0x001FFD74 and not the value of ESP. Value of the memory location 0x001FFD78 will not change as it is next memory location which is [esp + 4].

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        add dword ptr[esp], 0x7
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001FFE40 EIP = 011E13DE ESP = 001FFD74 EBP = 001FFE40 EFL = 00000200 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc   
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

What will be the value of the memory location 0x001FFD74 after the instruction, add dword ptr[esp], 0x7 In the above program?  

a) 0000000  
b) 001FFD74 + 0x7  
c) 00000007  
d) None of the above   

**Answer** c) 

**Description** 

Here we are adding 0x7 to the value of the memory location [esp], that is 0x001FFD74. So it will get added (0 + 7) and become 00000007.

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        add dword ptr[esp], 0x7
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001FFE40 EIP = 011E13DE ESP = 001FFD74 EBP = 001FFE40 EFL = 00000200 

Relevant memory is the following,

0x001FFD74  00 00 00 00     
0x001FFD78  00 00 00 00    
0x001FFD7C  00 e0 fd 7e    
0x001FFD80  cc cc cc cc    
0x001FFD84  cc cc cc cc    
0x001FFD88  cc cc cc cc    
0x001FFD8C  cc cc cc cc    
0x001FFD90  cc cc cc cc    
0x001FFD94  cc cc cc cc    
0x001FFD98  cc cc cc cc    
0x001FFD9C  cc cc cc cc    
0x001FFDA0  cc cc cc cc  


What will be the value of the memory location 0x001FFD78 after the instruction, add dword ptr[esp], 0x7 In the above program?  

a) 00000000  
b) 001FFD78 + 0x7  
c) 00000007  
d) None of the above  

**Answer** a) 

**Description**

Here the mentioned memory location is [esp + 4]. Its value will be the same as before because we are not touching that memory location in the above instruction, so it will be 00000000.  

---
---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov edx, dword ptr[esp + 0Ch]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0031FC94 EIP = 009F13DE ESP = 001FFD74 EBP = 0031FC94 EFL = 00000204 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

Which will change after the instruction, mov edx, dword ptr[esp + 0Ch] in the above program?  

a) Value of the memory location 0x001FFD80  
b) EDX  
c) No change  
d) Value of the Memory location 0x001FFD7C  

**Answer** b) 

**Description**

Here EDX will change as we are moving the value from the memory location [esp + 0Ch], to EDX.

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov edx, dword ptr[esp + 0Ch]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0031FC94 EIP = 009F13DE ESP = 001FFD74 EBP = 0031FC94 EFL = 00000204 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

What will be the value of EDX after the instruction, mov edx, dword ptr[esp + 0Ch], in the above program?  

a) 00000001  
b) CCCCCCCC  
c) 00e0fd7e  
d) 00000000  

**Answer** b) 

**Description**

The value in the memory location [esp + 0Ch] which is CCCCCCCC will get moved to EDX. So EDX will become CCCCCCCC.  

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub dword ptr[esp], 0x2
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0018F8A8 EIP = 00CC13DE ESP = 001FFD74 EBP = 0018F8A8 EFL = 00000204 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

What all will change after the instruction, sub dword ptr[esp], 0x2 in the above program?  

a) ESP  
b) Value in the memory location 0x001FFD74  
c) EIP  
d) Both b & c  

**Answer** d) 

**Description**

Here we are subtracting 0x2 from the value of the memory location 0x001FFD74, so it will change. EIP will change with every instruction.  

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub dword ptr[esp], 0x2
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0018F8A8 EIP = 00CC13DE ESP = 001FFD74 EBP = 0018F8A8 EFL = 00000204 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

What will be the value in the memory location 0x001FFD74 after the line, sub dword ptr[esp], 0x2 in the above program?  

a) 00000000-2=FFFFFFFE  
b) 001FFD74-2=001FFD72  
c) CCCCCCCC-2=CCCCCCCA  
d) None of the above  

**Answer** a) 

**Description**

Here we are subtracting 0x2 from the value of the memory location 0x001FFD74, that is from 00000000. So the result will be 00000000-2=FFFFFFFE.    

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov dword ptr[esp + 8], edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001DFA8C EIP = 00E813DE ESP = 001FFD74 EBP = 001DFA8C EFL = 00000204 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

What will change after the instruction, mov dword ptr[esp + 8], edx in the above program?  

a) Value of the memory location 0x001FFD7C  
b) EDX  
c) EIP  
d) Both a & c  

**Answer** d) 

**Description**

Here we are moving the value in edx to the value of the memory location, [esp + 8], that is 0x001FFD7C. So its value will change. EIP changes with every instruction.   

---
---


9 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov dword ptr[esp + 8], edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001DFA8C EIP = 00E813DE ESP = 001FFD74 EBP = 001DFA8C EFL = 00000204 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

What will be the value of the memory location, 0x001FFD7C after the instruction, mov dword ptr[esp + 8], edx in the above program?  

a) 00000000  
b) 00000001  
c) CCCCCCCC  
d) None of the above  

**Answer** b) 

**Description**

Here we are moving the value in edx to the value of the memory location, [esp + 8], that is 0x001FFD7C. So it will become 00000001.

---
---


10 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov edi, 9
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0044FB0C EIP = 00EB13DE ESP = 001FFD74 EBP = 0044FB0C EFL = 00000200 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

Which register/s will change after the execution of the line, mov edi, 9 in the above program?  

a) EDI  
b) EIP  
c) EAX  
d) Both a & b  

**Answer** d) 

**Description**

Here we are moving a value 9 to EDI register, so it will change. EIP will change  after every instruction. EAX register will not change as we are not touching it.

---
---


11 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov edi, 9
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0044FB0C EIP = 00EB13DE ESP = 001FFD74 EBP = 0044FB0C EFL = 00000200 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

What will be the value of EDI register after the execution of the line, mov edi, 9 in the above program?  

a) 0044FB0C  
b) 00000009  
c) 00000000  
d) None of the above  

**Answer** b) 

**Description**

Here we are moving a value 9 to EDI register, so it will change to 00000009.  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov eip, eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0044FB0C EIP = 00EB13DE ESP = 001FFD74 EBP = 0044FB0C EFL = 00000200 

Relevant memory is the following,

0x001FFD74 00 00 00 00  
0x001FFD78 00 00 00 00  
0x001FFD7C 00 e0 fd 7e  
0x001FFD80 cc cc cc cc  
0x001FFD84 cc cc cc cc  
0x001FFD88 cc cc cc cc  
0x001FFD8C cc cc cc cc  
0x001FFD90 cc cc cc cc  
0x001FFD94 cc cc cc cc  
0x001FFD98 cc cc cc cc  
0x001FFD9C cc cc cc cc  
0x001FFDA0 cc cc cc cc  

What will be the value of EIP register after the execution of the line, mov eip, eax in the above program?  

a) CCCCCCCC  
b) 00EB13DE  
c) 00000000  
d) Illegal instruction  

**Answer** d) 

**Description**

EIP register is a strictly special purpose register which is always pointing to the next instruction. We cannot use it for other purposes, so this will not work and it is an illegal instruction.  

---
---


13 : 














