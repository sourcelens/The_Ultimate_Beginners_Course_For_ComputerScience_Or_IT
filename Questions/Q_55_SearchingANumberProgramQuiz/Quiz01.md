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

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0022FB2C EIP = 003F13DE ESP = 0022FA60 EBP = 0022FB2C EFL = 00000204

Relevant memory is the following,

0x0022FA3C 772e041d  
0x0022FA40 0003a27a  
0x0022FA44 fffffffe  
0x0022FA48 772a36fa  
0x0022FA4C 772a32f2  
0x0022FA50 00428358  
0x0022FA54 00428360  
0x0022FA58 00000000  
0x0022FA5C 00000000  
0x0022FA60 00000000  
0x0022FA64 00000000  
0x0022FA68 7efde000  
0x0022FA6C cccccccc  
0x0022FA70 cccccccc  
0x0022FA74 cccccccc  

Disassembly is the following,   

<img src="" width="400"/>

What will be the value of ESP after the execution of the instruction sub esp, 20 in the above program?
