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


11 : We have the below program,  

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

What will be the value of the memory location, 0x0030FDB8 after the execution of the instruction push edx in the above program?  

a) CCCCCCCC  
b) 0000000  
c) 00000001  
d) None of the above  

**Answer** c) 

**Description**

push eax instruction is effectively two instructions, that is sub esp, 4 & mov dword ptr [esp], edx. So it is allocating memory and writing to memory. So value of the memory location 0x0030FDB8 will become the value of EDX, that is 00000001.           

---
---


12 : We have the below program,  

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

What will be the value of ESP after the execution of the line, push edx in the above program?  

a) CCCCCCCC  
b) 0030FDC0  
c) 0030FDBC  
d) 0030FDB8  

**Answer** d) 

**Description**

push eax instruction is effectively two instructions, that is sub esp, 4 & mov dword ptr [esp], edx. So it is allocating memory and writing to memory. So value of the memory location 0x0030FDB8  will change and ESP will be pointing to that memory location. So ESP will become 0030FDB8.

---
---


13 : We have the below program,  

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

What will be the fate of the above program?  

a) Program will crash  
b) Program will not crash  
c) Nothing happen  
d) None of the above  

**Answer** b) 

**Description**

In the above program we are allocating 4 bytes of stack memory. So it must be deallocated. We are deallocating it by add esp, 4. So the program won’t crash.

---
---


14 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0030FD84 EIP = 00F013DE ESP = 0030FCB8 EBP = 0030FD84 EFL = 00000200 

Relevant memory is the following,

0x0030FCAC b0 7e 37 00  
0x0030FCB0 00 00 00 00  
0x0030FCB4 00 00 00 00  
0x0030FCB8 00 00 00 00  
0x0030FCBC 00 00 00 00  
0x0030FCC0 00 e0 fd 7e  
0x0030FCC4 cc cc cc cc  
0x0030FCC8 cc cc cc cc  
0x0030FCCC cc cc cc cc  
0x0030FCD0 cc cc cc cc  

What will change after the execution of the instruction, pop eax in the above program?  

a) Value of the memory location 0x0030FCB8  
b) ESP  
c) EAX  
d) Both b & c  

**Answer** d) 

**Description**

pop eax instruction is effectively two instructions, that is mov eax, dword ptr[esp] & add esp, 4. So it is reading from memory, moving it to EAX and deallocating memory. So EAX will change and ESP will be pointing to next memory location. So ESP will also change.

---
---


15 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0030FD84 EIP = 00F013DE ESP = 0030FCB8 EBP = 0030FD84 EFL = 00000200 

Relevant memory is the following,

0x0030FCAC b0 7e 37 00  
0x0030FCB0 00 00 00 00  
0x0030FCB4 00 00 00 00  
0x0030FCB8 00 00 00 00  
0x0030FCBC 00 00 00 00  
0x0030FCC0 00 e0 fd 7e  
0x0030FCC4 cc cc cc cc  
0x0030FCC8 cc cc cc cc  
0x0030FCCC cc cc cc cc  
0x0030FCD0 cc cc cc cc  

What will be the value of EAX after the execution of the instruction, pop eax in the above program?  

a) CCCCCCCC  
b) 00000000  
c) 0030FCB8  
d) Not enough information to answer this  

**Answer** b) 

**Description**

pop eax instruction is effectively two instructions, that is mov eax, dword ptr[esp] & add esp, 4. So it is reading from memory, moving it to EAX and deallocating memory. So EAX will change and will become the value of the memory location 0x0030FCB8, that is 00000000.

---
---


16 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0030FD84 EIP = 00F013DE ESP = 0030FCB8 EBP = 0030FD84 EFL = 00000200 

Relevant memory is the following,

0x0030FCAC b0 7e 37 00  
0x0030FCB0 00 00 00 00  
0x0030FCB4 00 00 00 00  
0x0030FCB8 00 00 00 00  
0x0030FCBC 00 00 00 00  
0x0030FCC0 00 e0 fd 7e  
0x0030FCC4 cc cc cc cc  
0x0030FCC8 cc cc cc cc  
0x0030FCCC cc cc cc cc  
0x0030FCD0 cc cc cc cc  

What will be the value of ESP after the execution of the line, pop eax in the above program?  

a) 0030FCB8  
b) 00000000  
c) CCCCCCCC  
d) 0030FCBC  

**Answer** d) 

**Description**

pop eax instruction is effectively two instructions, that is mov eax, dword ptr[esp] & add esp, 4. So it is reading from memory, moving it to EAX and deallocating memory. So ESP will be pointing to next memory location that is 0030FCBC.

---
---


17 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0030FD84 EIP = 00F013DE ESP = 0030FCB8 EBP = 0030FD84 EFL = 00000200 

Relevant memory is the following,

0x0030FCAC b0 7e 37 00  
0x0030FCB0 00 00 00 00  
0x0030FCB4 00 00 00 00  
0x0030FCB8 00 00 00 00  
0x0030FCBC 00 00 00 00  
0x0030FCC0 00 e0 fd 7e  
0x0030FCC4 cc cc cc cc  
0x0030FCC8 cc cc cc cc  
0x0030FCCC cc cc cc cc  
0x0030FCD0 cc cc cc cc  

What will be the fate of the above program?  

a) Program will crash  
b) Program will not crash  
c) Not enough information to answer this  
d) None of the above  

**Answer** a) 

**Description**

In the above program we are deallocating memory at the end, but we are not allocating memory at the beginning. For a function/a set of instructions ESP must be the same before and after the execution of it. So as we are not allocating stack memory at the beginning, the program will crash.   

---
---


18 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        pop edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0044F80C EIP = 000F13DE ESP = 0044F740 EBP = 0044F80C EFL = 00000200 

Relevant memory is the following,

0x0044F734 b0 7e 71 00  
0x0044F738 00 00 00 00  
0x0044F73C 00 00 00 00  
0x0044F740 00 00 00 00  
0x0044F744 00 00 00 00  
0x0044F748 00 e0 fd 7e  
0x0044F74C cc cc cc cc  
0x0044F750 cc cc cc cc  
0x0044F754 cc cc cc cc  
0x0044F758 cc cc cc cc  

What will change after the execution of the instruction, pop edx in the above program?  

a) Value of the memory location 0x0044F73C  
b) EIP  
c) EDX  
d) Both b & c  

**Answer** d) 

**Description**

pop edx instruction is effectively two instructions, that is mov edx, dword ptr[esp] & add esp, 4. So it is reading from memory, moving it to EDX and deallocating memory. So EDX will change and become the value of the memory location 0x0044F73C. EIP will change after every instruction.        

---
---


19 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        pop edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0044F80C EIP = 000F13DE ESP = 0044F740 EBP = 0044F80C EFL = 00000200 

Relevant memory is the following,

0x0044F734 b0 7e 71 00  
0x0044F738 00 00 00 00  
0x0044F73C 00 00 00 00   
0x0044F740 00 00 00 00  
0x0044F744 00 00 00 00  
0x0044F748 00 e0 fd 7e  
0x0044F74C cc cc cc cc  
0x0044F750 cc cc cc cc  
0x0044F754 cc cc cc cc  
0x0044F758 cc cc cc cc  

What will be the value of EDX after the execution of the instruction, pop edx in the above program?  

a) CCCCCCCC  
b) 00000000  
c) 0044F740  
d) None of the above  

**Answer** b) 

**Description**

pop edx instruction is effectively two instructions, that is mov edx, dword ptr[esp] & add esp, 4. So it is reading from memory, moving it to EDX and deallocating memory. So EDX will change and will become the value of the memory location 0x0044F73C, that is 00000000.  

---
---


20 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        pop edx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0044F80C EIP = 000F13DE ESP = 0044F740 EBP = 0044F80C EFL = 00000200 

Relevant memory is the following,

0x0044F734 b0 7e 71 00  
0x0044F738 00 00 00 00  
0x0044F73C 00 00 00 00  
0x0044F740 00 00 00 00  
0x0044F744 00 00 00 00  
0x0044F748 00 e0 fd 7e  
0x0044F74C cc cc cc cc  
0x0044F750 cc cc cc cc  
0x0044F754 cc cc cc cc  
0x0044F758 cc cc cc cc  

What will be the fate of the above program?  

a) Program will crash  
b) Program will not crash  
c) Not enough information to answer this  
d) None of the above  

**Answer** b) 

**Description**

pop edx instruction is effectively two instructions, that is mov edx, dword ptr[esp] & add esp, 4. So it is reading from memory, moving it to EDX and deallocating memory. In the program firstly we are allocating memory by sub esp, 4. So the stack memory we are deallocating is the memory we allocated at the beginning. ESP will be the same before and after the function/set of instructions. So the program will not crash.

---
---


21 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
label1:
    int a = 20;
    __asm
    {
        call label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0035FB8C EIP = 010613E5 ESP = 0035FAB4 EBP = 0035FB8C EFL = 00000204 

Relevant memory is the following,

0x0035FAA8 fa 36 00 77  
0x0035FAAC f2 32 00 77  
0x0035FAB0 28 7f 44 00  
0x0035FAB4 00 00 00 00  
0x0035FAB8 00 00 00 00  
0x0035FABC 00 e0 fd 7e  
0x0035FAC0 cc cc cc cc  
0x0035FAC4 cc cc cc cc  
0x0035FAC8 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_48_AssemblySingleInstructionPractice_push_pop_call_ret/Images/Q_48_Disassembly.png" width="400"/>  

What will change after executing the instruction, call label1 in the above program?  

a) ESP  
b) EIP  
c) Value of the memory location 0x0035FAB0  
d) All of the above  

**Answer** d) 

**Description**

Call Label1 is effectively a combination of three instructions. First one is sub esp, 4, that is allocating stack memory. So ESP will change. Second one is mov dword ptr[esp], eip, that is moving the value of EIP to that memory location. So value of that memory location will change. Third one is mov eip, address of Label1. So EIP will also change.

---
---


22 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
label1:
    int a = 20;
    __asm
    {
        call label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0035FB8C EIP = 010613E5 ESP = 0035FAB4 EBP = 0035FB8C EFL = 00000204

Relevant memory is the following,

0x0035FAA8 fa 36 00 77  
0x0035FAAC f2 32 00 77  
0x0035FAB0 28 7f 44 00  
0x0035FAB4 00 00 00 00  
0x0035FAB8 00 00 00 00  
0x0035FABC 00 e0 fd 7e  
0x0035FAC0 cc cc cc cc  
0x0035FAC4 cc cc cc cc  
0x0035FAC8 cc cc cc cc  

 
Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_48_AssemblySingleInstructionPractice_push_pop_call_ret/Images/Q_48_Disassembly22.png" width="400"/>  

What will be the value of EIP after the instruction, call label1 in the above program?  

a) 010613DE  
b) 010613EA  
c) 010613E5  
d) 0035FAB0  

**Answer** a) 

**Description**

The EIP after executing call Label1, will be pointing to the address of Label1. So from the disassembly we get the address of Label1 and that is 010613DE.  

---
---


23 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
label1:
    int a = 20;
    __asm
    {
        call label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0035FB8C EIP = 010613E5 ESP = 0035FAB4 EBP = 0035FB8C EFL = 00000204 

Relevant memory is the following,

0x0035FAA8 fa 36 00 77  
0x0035FAAC f2 32 00 77  
0x0035FAB0 28 7f 44 00  
0x0035FAB4 00 00 00 00  
0x0035FAB8 00 00 00 00  
0x0035FABC 00 e0 fd 7e  
0x0035FAC0 cc cc cc cc  
0x0035FAC4 cc cc cc cc  
0x0035FAC8 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_48_AssemblySingleInstructionPractice_push_pop_call_ret/Images/Q_48_Disassembly23.png" width="400"/>  

What will be the value of ESP after the instruction, call label1 in the above program?  

a) 0035FAB4  
b) 0035FAB0  
c) 0035FAB8  
d) 0035FAAC  

**Answer** b) 

**Description**

What is call instruction doing first is allocating 4 bytes of stack memory, that is sub esp, 4. So ESP will become 0035FAB0.  

---
---


24 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
label1:
    int a = 20;
    __asm
    {
        call label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0035FB8C EIP = 010613E5 ESP = 0035FAB4 EBP = 0035FB8C EFL = 00000204 

Relevant memory is the following,

0x0035FAA8 fa 36 00 77  
0x0035FAAC f2 32 00 77  
0x0035FAB0 28 7f 44 00  
0x0035FAB4 00 00 00 00  
0x0035FAB8 00 00 00 00  
0x0035FABC 00 e0 fd 7e  
0x0035FAC0 cc cc cc cc  
0x0035FAC4 cc cc cc cc  
0x0035FAC8 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_48_AssemblySingleInstructionPractice_push_pop_call_ret/Images/Q_48_Disassembly24.png" width="400"/>  

What will be the value of the memory location 0x0035FAB0 after the execution of the instruction, call label1 in the above program?  

a) 010613E5  
b) 010613DE  
c) 010613EA  
d) 0035FAB0  

**Answer** c) 

**Description**

Call instruction is doing mov dword ptr[esp], eip. That is it is moving the value of EIP to the value of the memory location [esp]. So it will become 010613EA.  

---
---


25 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
label1:
    int a = 20;
    __asm
    {
        jmp label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0041FD54 EIP = 001D13E5 ESP = 0041FC7C EBP = 0041FD54 EFL = 00000214 

Relevant memory is the following,

0x0041FC70 fa 36 00 77    
0x0041FC74 f2 32 00 77  
0x0041FC78 28 7f 78 00  
0x0041FC7C 00 00 00 00  
0x0041FC80 00 00 00 00  
0x0041FC84 00 e0 fd 7e  
0x0041FC88 cc cc cc cc  
0x0041FC8C cc cc cc cc  
0x0041FC90 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_48_AssemblySingleInstructionPractice_push_pop_call_ret/Images/Q_48_Disassembly25.jpg" width="400"/>  

What will change after executing the instruction, jmp label1 in the above program?  

a) ESP  
b) EIP  
c) EAX  
d) All of the above  

**Answer** b) 

**Description**

jmp label1 is an unconditional jump. So it will jump to label1. So the value of EIP after the instruction will be the address of label1. So EIP will change. Jmp here is effectively, mov eip, label1. ESP will not change as we are not touching stack memory, similarly EAX will also have no change.

---
--- 


26 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
label1:
    int a = 20;
    __asm
    {
        jmp label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0041FD54 EIP = 001D13E5 ESP = 0041FC7C EBP = 0041FD54 EFL = 00000214 

Relevant memory is the following,

0x0041FC70 fa 36 00 77  
0x0041FC74 f2 32 00 77  
0x0041FC78 28 7f 78 00  
0x0041FC7C 00 00 00 00  
0x0041FC80 00 00 00 00  
0x0041FC84 00 e0 fd 7e  
0x0041FC88 cc cc cc cc  
0x0041FC8C cc cc cc cc  
0x0041FC90 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_48_AssemblySingleInstructionPractice_push_pop_call_ret/Images/Q_48_Disassembly26.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, jmp label1 in the above program?   

a) 001D13E5  
b) 001D13E7  
c) 001D13DE  
d) 001D13E9  

**Answer** c) 

**Description**

jmp label1 is an unconditional jump. So it will jump to label1. So the value of EIP after the instruction will be the address of label1. So EIP will change to 001D13DE.   

---
---


27 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push dword ptr[esp + 8]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0047FE98 EIP = 001E13DE ESP = 0047FDCC EBP = 0047FE98 EFL = 00000204 

Relevant memory is the following,

x0047FDC0 00808340  
0x0047FDC4 00000000  
0x0047FDC8 00000000  
0x0047FDCC 00000000   
0x0047FDD0 00000000  
0x0047FDD4 00e0fd7e  
0x0047FDD8 cccccccc  
0x0047FDDC cccccccc  
0x0047FDE0 cccccccc  
0x0047FDE4 cccccccc  
0x0047FDE8 cccccccc  

What will change after the execution of the instruction push dword ptr[esp + 8] in the above program?  

a) ESP  
b) EIP  
c) Value of the memory location 0x0047FDC8  
d) All of the above  

**Answer** d) 

**Description**

Here after the above instruction ESP will be subtracted by 4, that is it will be pointing to 0x0047FDC8 and also the value of the memory location [esp + 8] (0x0047FDD4) will move to the value of the memory location 0x0047FDC8. So ESP and value of the memory location 0x0047FDC8 will change. EIP will change after every instruction.  

---
---


28 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push dword ptr[esp + 8]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0047FE98 EIP = 001E13DE ESP = 0047FDCC EBP = 0047FE98 EFL = 00000204 

Relevant memory is the following,

0x0047FDC0 00808340  
0x0047FDC4 00000000  
0x0047FDC8 00000000  
0x0047FDCC 00000000  
0x0047FDD0 00000000  
0x0047FDD4 00e0fd7e  
0x0047FDD8 cccccccc  
0x0047FDDC cccccccc  
0x0047FDE0 cccccccc  
0x0047FDE4 cccccccc  
0x0047FDE8 cccccccc  

What will be the value of the memory location 0x0047FDC8 after the execution of the instruction push dword ptr[esp + 8] in the above program?  

a) 00000000  
b) 7EFDE000  
c) CCCCCCCC  
d) None of the above  

**Answer** b) 

**Description**

Here after the above instruction ESP will be subtracted by 4, that is it will be pointing to 0x0047FDC8 and also the value of the memory location [esp + 8] (0x0047FDD4) will move to the value of the memory location 0x0047FDC8. So the value of the memory location 0x0047FDC8 will be 00E0FD7E.

---
---


29 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        push dword ptr[esp + 8]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0047FE98 EIP = 001E13DE ESP = 0047FDCC EBP = 0047FE98 EFL = 00000204 

Relevant memory is the following,

0x0047FDC0 00808340  
0x0047FDC4 00000000  
0x0047FDC8 00000000  
0x0047FDCC 00000000  
0x0047FDD0 00000000  
0x0047FDD4 00e0fd7e  
0x0047FDD8 cccccccc  
0x0047FDDC cccccccc  
0x0047FDE0 cccccccc  
0x0047FDE4 cccccccc  
0x0047FDE8 cccccccc  

What will be the value of the memory location 0x0047FDD4 after the execution of the instruction push dword ptr[esp + 8] in the above program?  

a) 00000000  
b) 00E0FD7E  
c) CCCCCCCC  
d) Not enough information to answer  

**Answer** b) 

**Description**

After the above instruction the value of the memory location [esp + 8] (0x0047FDD4) will move to the value of the memory location 0x0047FDC8. The value of the memory location [esp + 8] (0x0047FDD4) is retained which is 00E0FD7E.  

---
---

























