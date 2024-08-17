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

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003BF920 EIP = 00F413DE ESP = 003BF854 EBP = 003BF920 EFL = 00000204

Relevant memory is the following,

0x003BF83C 779436fa  
0x003BF840 779432f2  
0x003BF844 00668398  
0x003BF848 006683a0  
0x003BF84C 00000000  
0x003BF850 00000000  
0x003BF854 00000000  
0x003BF858 00000000  
0x003BF85C 7efde000  
0x003BF860 cccccccc  

What will be the value of ESP after the execution of the instruction sub esp, 20?  

a) 003BF850  
b) 003BF84C  
c) 003BF848  
d) 003BF840  

**Answer** d) 

**Description**  

Sub esp, 20 means we are allocating 5 locations of stack memory 4 bytes each. So the value of ESP will be 003BF840 which is evident from the stack memory locations given.  

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp], 77
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003BF920 EIP = 00F413DE ESP = 003BF840 EBP = 003BF920 EFL = 00000204

Relevant memory is the following,

0x003BF83C 779436fa  
0x003BF840 779432f2  
0x003BF844 00668398  
0x003BF848 006683a0  
0x003BF84C 00000000  
0x003BF850 00000000  
0x003BF854 00000000  
0x003BF858 00000000  
0x003BF85C 7efde000  
0x003BF860 cccccccc  

Disassembly is the following,  

<img src="" width="400"/>

What will be the value of the memory location 003BF840, after the execution of the instruction mov dword ptr[esp], 77?
