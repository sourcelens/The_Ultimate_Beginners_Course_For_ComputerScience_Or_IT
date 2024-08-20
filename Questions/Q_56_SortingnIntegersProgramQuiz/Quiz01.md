---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    sub esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13DE ESP = 0133FA58 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_1.jpg" width="400"/>

What will be the value of ESP after the execution of the instruction sub esp, 20 in the above program?   

a) 0133FA58  
b) 0133FA54  
c) 0133FA48  
d) 0133FA44  

**Answer** d)

**Description** 

Sub esp, 20 means we are allocating 5 locations of stack memory 4 bytes each. So the value of ESP will be 0133FA44, which is evident from the stack memory locations given.  

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    sub esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13DE ESP = 0133FA58 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,

What will be the value of EIP after the execution of the instruction sub esp, 20 in the above program?
