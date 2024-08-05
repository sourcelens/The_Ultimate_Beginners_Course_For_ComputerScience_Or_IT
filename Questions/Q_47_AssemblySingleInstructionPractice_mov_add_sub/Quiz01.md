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
