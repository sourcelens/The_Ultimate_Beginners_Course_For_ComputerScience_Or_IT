---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov edi, 0
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 00D3C000 ECX = 00000000 EDX = 00000001 ESI = 00211640 EDI = 00BAFAEC EIP = 0021101E ESP = 00BAFA20 EBP = 00BAFAEC EFL = 00000200

Relevant memory is the following,

0x00BAFA14 00e60000  
0x00BAFA18 00baf9f8  
0x00BAFA1C 00bafa3c  
0x00BAFA20 00211640  
0x00BAFA24 00211640  
0x00BAFA28 00d3c000  
0x00BAFA2C cccccccc  
0x00BAFA30 cccccccc  
0x00BAFA34 cccccccc  
0x00BAFA38 cccccccc  
0x00BAFA3C cccccccc  

What will be the value of EDI register after the execution of the instruction mov edi, 0?  

a) 00000000  
b) 00000001  
c) 00BAFAEC  
d) 00BAFA20  

**Answer** a) 

**Description**

Here we are moving the value 0 to EDI register by the instruction mov edi, 0, so it will become 00000000.  

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov esi, 7000000
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 00D3C000 ECX = 00000000 EDX = 00000001 ESI = 00211640 EDI = 00BAFAEC EIP = 0021101E ESP = 00BAFA20 EBP = 00BAFAEC EFL = 00000200

Relevant memory is the following,

0x00BAFA14 00e60000  
0x00BAFA18 00baf9f8  
0x00BAFA1C 00bafa3c  
0x00BAFA20 00211640  
0x00BAFA24 00211640  
0x00BAFA28 00d3c000  
0x00BAFA2C cccccccc  
0x00BAFA30 cccccccc  
0x00BAFA34 cccccccc  
0x00BAFA38 cccccccc  
0x00BAFA3C cccccccc  

What will be the value of ESI register after the execution of the instruction mov esi, 7000000?  

a) 00000000  
b) 006ACFC0 (Hex value of 7000000)  
c) 00211640  
d) 00000007  

**Answer** b) 

**Description**  

Here we are moving the value 7000000 (Hex value is 006ACFC0) to ESI register by the instruction mov esi, 7000000, so it will become 006ACFC0.  

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov eax, edi
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 00D3C000 ECX = 00000000 EDX = 00000001 ESI = 00211640 EDI = 00000000 EIP = 0021101E ESP = 00BAFA20 EBP = 00BAFAEC EFL = 00000200

Relevant memory is the following,

0x00BAFA14 00e60000  
0x00BAFA18 00baf9f8  
0x00BAFA1C 00bafa3c  
0x00BAFA20 00211640  
0x00BAFA24 00211640  
0x00BAFA28 00d3c000  
0x00BAFA2C cccccccc  
0x00BAFA30 cccccccc  
0x00BAFA34 cccccccc  
0x00BAFA38 cccccccc  
0x00BAFA3C cccccccc  

What will be the value of EAX register after the execution of the instruction mov eax, edi ?  

a) CCCCCCCC  
b) 00000001  
c) 00000000  
d) 00BAFA20  

**Answer** c) 

**Description**

Here we are moving the value in EDI register to EAX. EDI register has the value 0, as seen from the register values shown, so EAX register will become 00000000.   

---
---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov ebx, 3
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 00D3C000 ECX = 00000000 EDX = 00000001 ESI = 00211640 EDI = 00000000 EIP = 0021101E ESP = 00BAFA20 EBP = 00BAFAEC EFL = 00000200

Relevant memory is the following,

0x00BAFA14 00e60000  
0x00BAFA18 00baf9f8  
0x00BAFA1C 00bafa3c  
0x00BAFA20 00211640  
0x00BAFA24 00211640  
0x00BAFA28 00d3c000  
0x00BAFA2C cccccccc  
0x00BAFA30 cccccccc  
0x00BAFA34 cccccccc  
0x00BAFA38 cccccccc  
0x00BAFA3C cccccccc  

What will be the value of EBX register after the execution of the instruction mov ebx, 3?  

a) CCCCCCCC  
b) 00000003  
c) 00000000  
d) 00BAFA20  

**Answer** b) 

**Description**

Here we are moving the value 3 to EBX register by the instruction mov ebx, 3, so it will become 00000003.  

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov edi, 0

    mainloopStart:

        mov esi, 7000000
        mov eax, edi
        mov ebx, 3
        call nTimesMultiplyM

    nTimesMultiplyM :

        mov ecx, eax
    }
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 00000003 ECX = 00000000 EDX = 00000001 ESI = 006ACFC0 EDI = 00000000 EIP = 00E8102F ESP = 0053F77C EBP = 0053F848 EFL = 00000204

Relevant memory is the following,

0x0053F770 0101f7cc  
0x0053F774 00810000  
0x0053F778 785e9d20  
0x0053F77C 00e81640  
0x0053F780 00e81640  
0x0053F784 002ff000  
0x0053F788 cccccccc  
0x0053F78C cccccccc  
0x0053F790 cccccccc  

Disassembly is the following,  

<img src="Images/Q_57_5.jpg" width="400"/>

What will be the value of EIP register after the execution of the instruction mov edi, 0, in the above program?  

a) 00E81023  
b) 00E81028  
c) 00E8102A  
d) 00E8102F  

**Answer** a) 

**Description**

Value of EIP register will always be the EIP of the next instruction to execute which here is mov esi, 7000000 (Hex value is 006ACFC0), whose EIP is 00E81023 and it is evident from the disassembly shown.   

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov edi, 0

    mainloopStart:

        mov esi, 7000000
        mov eax, edi
        mov ebx, 3
        call nTimesMultiplyM

    nTimesMultiplyM :

        mov ecx, eax
    }
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 00000003 ECX = 00000000 EDX = 00000001 ESI = 006ACFC0 EDI = 00000000 EIP = 00E8102F ESP = 0053F77C EBP = 0053F848 EFL = 00000204

Relevant memory is the following,

0x0053F770 0101f7cc  
0x0053F774 00810000  
0x0053F778 785e9d20  
0x0053F77C 00e81640  
0x0053F780 00e81640  
0x0053F784 002ff000  
0x0053F788 cccccccc  
0x0053F78C cccccccc  
0x0053F790 cccccccc  

Disassembly is the following,  

<img src="Images/Q_57_6.jpg" width="400"/>

What will be the value of EIP register after the execution of the instruction mov esi, 7000000, in the above program?  

a) 00E81023  
b) 00E81028  
c) 00E8102A  
d) 00E8102F  

**Answer** b) 

**Description**

Value of EIP register will always be the EIP of the next instruction to execute, which here is mov eax, edi, whose EIP is 00E81028 and it is evident from the disassembly shown.   

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov edi, 0

    mainloopStart:

        mov esi, 7000000
        mov eax, edi
        mov ebx, 3
        call nTimesMultiplyM

    nTimesMultiplyM :

        mov ecx, eax
    }
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 00000003 ECX = 00000000 EDX = 00000001 ESI = 006ACFC0 EDI = 00000000 EIP = 00E8102F ESP = 0053F77C EBP = 0053F848 EFL = 00000204

Relevant memory is the following,

0x0053F770 0101f7cc  
0x0053F774 00810000  
0x0053F778 785e9d20  
0x0053F77C 00e81640  
0x0053F780 00e81640  
0x0053F784 002ff000  
0x0053F788 cccccccc  
0x0053F78C cccccccc  
0x0053F790 cccccccc  

Disassembly is the following,

What will be the value of EIP register after the execution of the instruction mov eax, edi, in the above program?




