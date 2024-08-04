---
---

1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov eax, ebx
    }
    return 0;
}
```


Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003DF954 EIP = 002113DE ESP = 003DF888 EBP = 003DF954 EFL = 00000200   


Relevant memory is the following,

0x003DF888  00 00 00 00  
0x003DF88C  00 00 00 00  
0x003DF890  00 e0 fd 7e  
0x003DF894  cc cc cc cc  
0x003DF898  cc cc cc cc  
0x003DF89C  cc cc cc cc  
0x003DF8A0  cc cc cc cc  
0x003DF8A4  cc cc cc cc  
0x003DF8A8  cc cc cc cc  
0x003DF8AC  cc cc cc cc  
0x003DF8B0  cc cc cc cc  
0x003DF8B4  cc cc cc cc  

Which register/s will change after the execution of the line, mov eax, ebx in the above program?  

a) EAX  
b) EBX  
c) ESP  
d) ECX  

**Answer** a) 

**Description**

In the above program the value of ebx will move to eax. So eax will become ebx value. EBX, ESP &amp; ECX will have no change.

---
---


2 : 
