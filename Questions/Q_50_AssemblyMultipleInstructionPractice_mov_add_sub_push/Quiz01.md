---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, 3
        add eax, 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0034FCE4 EIP = 00D513DE ESP = 0034FC18 EBP = 0034FCE4 EFL = 00000204

Relevant memory is the following,

0x0034FC18 00 00 00 00  
0x0034FC1C 00 00 00 00  
0x0034FC20 00 e0 fd 7e  
0x0034FC24 cc cc cc cc  
0x0034FC28 cc cc cc cc  
0x0034FC2C cc cc cc cc  
0x0034FC30 cc cc cc cc  

Disassembly is the following,  
<img src="" width="400"/>

Which register/s will change after the execution of the first instruction, mov eax, 3 in the above program?
