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
<img src="" width="400"/>

What will happen in the above program after the execution of the instruction, jz label1?
