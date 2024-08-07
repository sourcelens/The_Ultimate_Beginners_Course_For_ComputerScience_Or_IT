---
---

1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0037F888 EIP = 00F213DE ESP = 0037F7BC EBP = 0037F888 EFL = 00000200 

Relevant memory is the following,

0x0037F7B0 b0 7e 3c 00  
0x0037F7B4 00 00 00 00  
0x0037F7B8 00 00 00 00  
0x0037F7BC 00 00 00 00  
0x0037F7C0 00 00 00 00  
0x0037F7C4 00 e0 fd 7e  
0x0037F7C8 cc cc cc cc  
0x0037F7CC cc cc cc cc  
0x0037F7D0 cc cc cc cc  
0x0037F7D4 cc cc cc cc  

What will change after the execution of the instruction, push 6 in the above program?  

a) Value of the memory location 0x0037F7B8  
b) ESP  
c) Value of the memory location 0x0037F7BC  
d) Both a & b  

**Answer** d) 

**Description**

push 6 instruction is effectively two instructions, that is sub esp, 4 &amp; mov dword ptr [esp], 6. So it is allocating memory and writing to that memory. So value of the memory location 0x0037F7B8 will change and ESP will be pointing to that memory location. So ESP will also change.

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0037F888 EIP = 00F213DE ESP = 0037F7BC EBP = 0037F888 EFL = 00000200 

Relevant memory is the following,

0x0037F7B0 b0 7e 3c 00  
0x0037F7B4 00 00 00 00  
0x0037F7B8 00 00 00 00  
0x0037F7BC 00 00 00 00  
0x0037F7C0 00 00 00 00  
0x0037F7C4 00 e0 fd 7e  
0x0037F7C8 cc cc cc cc  
0x0037F7CC cc cc cc cc  
0x0037F7D0 cc cc cc cc  
0x0037F7D4 cc cc cc cc  

What will be the value of the memory location 0x0037F7B8, after the execution of the instruction push 6 in the above program?  

a) 00000006  
b) 00000000  
c) CCCCCCCC  
d) None of the above  

**Answer** a) 

**Description**

push 6 instruction is effectively two instructions, that is sub esp, 4 &amp; mov dword ptr [esp], 6. So it is allocating memory and writing to that memory. So the value of the memory location 0x0037F7B8 will become 00000006.       

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0037F888 EIP = 00F213DE ESP = 0037F7BC EBP = 0037F888 EFL = 00000200 

Relevant memory is the following,

0x0037F7B0 b0 7e 3c 00  
0x0037F7B4 00 00 00 00  
0x0037F7B8 00 00 00 00  
0x0037F7BC 00 00 00 00   
0x0037F7C0 00 00 00 00  
0x0037F7C4 00 e0 fd 7e  
0x0037F7C8 cc cc cc cc  
0x0037F7CC cc cc cc cc  
0x0037F7D0 cc cc cc cc  
0x0037F7D4 cc cc cc cc   

What will be the value of ESP after the execution of the line push 6 in the above program?  

a) 00000006  
b) 0037F7B8  
c) 0037F7C0  
d) 0037F7BC  

**Answer** b) 

**Description**

push 6 instruction is effectively two instructions, that is sub esp, 4 & mov dword ptr [esp], 6. So it is allocating memory and writing to memory. So value of memory location 0x0037F7B8 will change and ESP will be pointing to that memory location. So ESP will become 0037F7B8.

---
---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0037F888 EIP = 00F213DE ESP = 0037F7BC EBP = 0037F888 EFL = 00000200 

Relevant memory is the following,

0x0037F7B0 b0 7e 3c 00  
0x0037F7B4 00 00 00 00  
0x0037F7B8 00 00 00 00  
0x0037F7BC 00 00 00 00  
0x0037F7C0 00 00 00 00  
0x0037F7C4 00 e0 fd 7e  
0x0037F7C8 cc cc cc cc  
0x0037F7CC cc cc cc cc  
0x0037F7D0 cc cc cc cc  
0x0037F7D4 cc cc cc cc  

What will be the value of the memory location 0x0037F7BC, after the execution of the instruction push 6 in the above program?  

a) 00000006  
b) 00000000  
c) CCCCCCCC  
d) None of the above  

**Answer** b) 

**Description**

push 6 instruction is effectively two instructions, that is sub esp, 4 & mov dword ptr [esp], 6. So the value of the memory location 0x0037F7B8 is changing. Value of the memory location 0x0037F7BC is retained and it will have no change.   

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0037F888 EIP = 00F213DE ESP = 0037F7BC EBP = 0037F888 EFL = 00000200 

Relevant memory is the following,

0x0037F7B0 b0 7e 3c 00  
0x0037F7B4 00 00 00 00  
0x0037F7B8 00 00 00 00  
0x0037F7BC 00 00 00 00  
0x0037F7C0 00 00 00 00  
0x0037F7C4 00 e0 fd 7e  
0x0037F7C8 cc cc cc cc  
0x0037F7CC cc cc cc cc  
0x0037F7D0 cc cc cc cc  
0x0037F7D4 cc cc cc cc  

What will be the fate of the above program?  

a) Program will execute normally  
b) Program will crash  
c) Nothing happen  
d) None of the above  

**Answer** b) 

**Description**

In the above program we are allocating 4 bytes of stack memory. So it must be deallocated. But we are not doing, add esp, 4 in the above program. So the program will crash. 

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002AFC40 EIP = 010713DE ESP = 002AFB74 EBP = 002AFC40 EFL = 00000200 

Relevant memory is the following,

0x002AFB68 b0 7e 4f 00  
0x002AFB6C 00 00 00 00  
0x002AFB70 00 00 00 00  
0x002AFB74 00 00 00 00  
0x002AFB78 00 00 00 00  
0x002AFB7C 00 e0 fd 7e    
0x002AFB80 cc cc cc cc    
0x002AFB84 cc cc cc cc  
0x002AFB88 cc cc cc cc  
0x002AFB8C cc cc cc cc  

What will change after the execution of the instruction, push eax in the above program?  

a) Value of the memory location 0x002AFB70  
b) ESP  
c) Value of the memory location 0x002AFB74  
d) Both a & b  

**Answer** d) 

**Description**

push eax instruction is effectively two instructions, that is sub esp, 4 & mov dword ptr [esp], eax. So it is allocating memory and writing to memory. So value of the memory location 0x002AFB70  will change and ESP will be pointing to that memory location. So ESP will also change.

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002AFC40 EIP = 010713DE ESP = 002AFB74 EBP = 002AFC40 EFL = 00000200 

Relevant memory is the following,

0x002AFB68 b0 7e 4f 00  
0x002AFB6C 00 00 00 00  
0x002AFB70 00 00 00 00  
0x002AFB74 00 00 00 00  
0x002AFB78 00 00 00 00  
0x002AFB7C 00 e0 fd 7e  
0x002AFB80 cc cc cc cc  
0x002AFB84 cc cc cc cc  
0x002AFB88 cc cc cc cc  
0x002AFB8C cc cc cc cc  

What will be the value of the memory location, 0x002AFB70 after the execution of the instruction push eax in the above program?  

a) 00000006  
b) 00000000  
c) CCCCCCCC  
d) None of the above  

**Answer** c) 

**Description**

push eax instruction is effectively two instructions, that is sub esp, 4 & mov dword ptr [esp], eax. So it is allocating memory and writing to memory. So the value of the memory location 0x002AFB70 will become the value of EAX, that is CCCCCCCC.         

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002AFC40 EIP = 010713DE ESP = 002AFB74 EBP = 002AFC40 EFL = 00000200 

Relevant memory is the following,

0x002AFB68 b0 7e 4f 00  
0x002AFB6C 00 00 00 00  
0x002AFB70 00 00 00 00  
0x002AFB74 00 00 00 00  
0x002AFB78 00 00 00 00  
0x002AFB7C 00 e0 fd 7e  
0x002AFB80 cc cc cc cc  
0x002AFB84 cc cc cc cc  
0x002AFB88 cc cc cc cc  
0x002AFB8C cc cc cc cc  

What will be the value of ESP after the execution of the line, push eax in the above program?  

a) CCCCCCCC  
b) 002AFB70  
c) 002AFB74  
d) 002AFB78  

**Answer** b) 

**Description**

push eax instruction is effectively two instructions, that is sub esp, 4 & mov dword ptr [esp], eax. So it is allocating memory and writing to memory. So value of the memory location 0x002AFB70 will change and ESP will be pointing to that memory location. So ESP will become 002AFB70.  

---
---


9 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002AFC40 EIP = 010713DE ESP = 002AFB74 EBP = 002AFC40 EFL = 00000200 

Relevant memory is the following,

0x002AFB68 b0 7e 4f 00  
0x002AFB6C 00 00 00 00  
0x002AFB70 00 00 00 00  
0x002AFB74 00 00 00 00  
0x002AFB78 00 00 00 00  
0x002AFB7C 00 e0 fd 7e  
0x002AFB80 cc cc cc cc  
0x002AFB84 cc cc cc cc  
0x002AFB88 cc cc cc cc  
0x002AFB8C cc cc cc cc  

What will be the fate of the above program?  

a) Program will execute normally  
b) Program will crash  
c) Nothing happen  
d) None of the above  

**Answer** b) 

**Description**

In the above program we are allocating 4 bytes of stack memory. So it must be deallocated. But we are not doing, add esp, 4 in the above program. So the program will crash.   

---
---


10 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push edx
        add esp, 4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0030FE88 EIP = 00E413DE ESP = 0030FDBC EBP = 0030FE88 EFL = 00000200 

Relevant memory is the following,

0x0030FDAC a8 7e 6b 00  
0x0030FDB0 b0 7e 6b 00  
0x0030FDB4 00 00 00 00  
0x0030FDB8 00 00 00 00  
0x0030FDBC 00 00 00 00  
0x0030FDC0 00 00 00 00  
0x0030FDC4 00 e0 fd 7e  
0x0030FDC8 cc cc cc cc  

What will change after the execution of the instruction, push edx in the above program?  

a) Value of the memory location 0x0030FDBC  
b) ESP  
c) Value of the memory location 0x0030FDB8  
d) Both b & c  

**Answer** d) 

**Description**

push edx instruction is effectively two instructions, that is sub esp, 4 & mov dword ptr [esp], edx. So it is allocating memory and writing to memory. So value of the memory location 0x0030FDB8   will change and ESP will be pointing to that memory location. So ESP will also change.

---
---


11 :







