---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x5
        add dword ptr[esp], 0x4
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FBA0 EIP = 008313DE ESP = 0038FAD4 EBP = 0038FBA0 EFL = 00000200

Relevant memory is the following,

0x0038FAC8 b0 7e 3f 00  
0x0038FACC 00 00 00 00  
0x0038FAD0 00 00 00 00  
0x0038FAD4 00 00 00 00  
0x0038FAD8 00 00 00 00  
0x0038FADC 00 e0 fd 7e  
0x0038FAE0 cc cc cc cc  

Disassembly is the following,  
<img src="" width="400"/>

What will change after the execution of the instruction, push 0x5 in the above program?
