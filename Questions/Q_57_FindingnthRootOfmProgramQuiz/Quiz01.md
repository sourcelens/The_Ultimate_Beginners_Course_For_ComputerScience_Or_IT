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

<img src="Images/Q_57_7.jpg" width="400"/>

What will be the value of EIP register after the execution of the instruction mov eax, edi, in the above program?  

a) 00E81023  
b) 00E81028  
c) 00E8102A  
d) 00E8102F  

**Answer** c) 

**Description**

Value of EIP register will always be the EIP of the next instruction to execute, which here is mov ebx, 3 whose EIP is 00E8102A and it is evident from the disassembly shown.   

---
---


8 : We have the below program,  

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

<img src="Images/Q_57_8.jpg" width="400"/>

What will be the value of EIP register after the execution of the instruction mov ebx, 3, in the above program?  

a) 00E81023  
b) 00E81028  
c) 00E8102A  
d) 00E8102F  

**Answer** d) 

**Description**

Value of EIP register will always be the EIP of the next instruction to execute, which here is call nTimesMultiplyM, whose EIP is 00E8102F and it is evident from the disassembly shown.   

---
---


9 : We have the below program,  

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

<img src="Images/Q_57_9.jpg" width="400"/>

What will be the value of ESP register after the execution of the instruction call nTimesMultiplyM, in the above program?  

a) 0053F77C  
b) 0053F780  
c) 0053F778  
d) 0053F774  

**Answer** c) 

**Description**

Call nTimesMultiplyM is effectively a combination of three instructions. First one is sub esp, 4, that is allocating stack memory. So here ESP will change and become 0053F778. Second one is mov dword ptr[esp], eip, that is moving the value of EIP of next instruction to that memory location. So value of that memory location will change. Third one is mov eip, address of nTimesMultiplyM. So EIP will also change.  

---
---


10 : We have the below program,  

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

<img src="Images/Q_57_10.jpg" width="400"/>

What will be the value of the memory location [esp] after the execution of the instruction call nTimesMultiplyM, in the above program if the value of ESP now is 0053F778?  

a) 00E8102F  
b) 00E81034  
c) 00E8103D  
d) 00E8102A  

**Answer** b) 

**Description**

Call nTimesMultiplyM is effectively a combination of three instructions. First one is sub esp, 4, that is allocating stack memory. So here ESP will change and become 0053F778. Second one is mov dword ptr[esp], eip, that is moving the value of EIP of next instruction (00E81034) to that memory location (0053F778). So value of that memory location will change. Third one is mov eip, address of nTimesMultiplyM. So EIP will also change.  

---
---


11 : We have the below program,  

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

<img src="Images/Q_57_11.jpg" width="400"/>

What will be the value of EIP register after the execution of the instruction call nTimesMultiplyM, in the above program?   

a) 00E8102F  
b) 00E81034  
c) 00E81036  
d) 00E8103D  

**Answer** d) 

**Description**

Call nTimesMultiplyM is effectively a combination of three instructions. First one is sub esp, 4, that is allocating stack memory. So here ESP will change and become 0053F778. Second one is mov dword ptr[esp], eip, that is moving the value of EIP of next instruction (00E81034) to that memory location (0053F778). So value of that memory location will change. Third one is mov eip, address of nTimesMultiplyM. So EIP will change and become 00E8103D which is evident from the disassembly shown.  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
    nTimesMultiplyM :

        mov ecx, eax

    labelLoopStart :
        cmp ebx, 1
        jz labelEnd

        dec ebx
        imul eax, ecx
        jmp labelLoopStart

    labelEnd :
        ret
    }
    return 0;
}
```

Register values are the following,

EAX = 00000002 EBX = 00000003 ECX = 00000000 EDX = 00000001 ESI = 006ACFC0 EDI = 00000000 EIP = 0078103D ESP = 0135F764 EBP = 0135F834 EFL = 00000204

Relevant memory is the following,

0x0135F75C 014c0000  
0x0135F760 0135f740  
0x0135F764 00781034  
0x0135F768 00781640  
0x0135F76C 00781640   
0x0135F770 0119a000  
0x0135F774 cccccccc  
0x0135F778 cccccccc  
0x0135F77C cccccccc   
0x0135F780 cccccccc   

Disassembly is the following,  

<img src="Images/Q_57_12.jpg" width="400"/>

 What will be the value of ECX register after the execution of the instruction, mov ecx, eax, in the above program?  

 a) 00000000  
 b) 00000002  
 c) 00000003  
 d) 00000004  

 **Answer** b) 

**Description**  

By the instruction mov ecx, eax, we are moving the value of EAX register to ECX register. The value of EAX register here is 2 which is evident from the register values shown above. So it will move to ECX register and will become 00000002.   

---
---


13 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
    nTimesMultiplyM :

        mov ecx, eax

    labelLoopStart :
        cmp ebx, 1
        jz labelEnd

        dec ebx
        imul eax, ecx
        jmp labelLoopStart

    labelEnd :
        ret
    }
    return 0;
}
```

Register values are the following,

EAX = 00000002 EBX = 00000003 ECX = 00000000 EDX = 00000001 ESI = 006ACFC0 EDI = 00000000 EIP = 0078103D ESP = 0135F764 EBP = 0135F834 EFL = 00000204

Relevant memory is the following,

0x0135F75C 014c0000  
0x0135F760 0135f740   
0x0135F764 00781034  
0x0135F768 00781640  
0x0135F76C 00781640  
0x0135F770 0119a000  
0x0135F774 cccccccc  
0x0135F778 cccccccc  
0x0135F77C cccccccc  
0x0135F780 cccccccc  

Disassembly is the following,  

<img src="Images/Q_57_13.jpg" width="400"/>

 What will be the value of EIP register after the execution of the instruction, mov ecx, eax, in the above program?  

 a) 0078103D  
 b) 0078103F  
 c) 00781042  
 d) 00781044  

 **Answer** b) 

 **Description**   

 EIP register will always point to the next instruction which here is, cmp ebx, 1 whose EIP is 0078103F and it is evident from the disassembly shown.  

 ---
 ---


 14 : We have the below program,  

 ```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
    nTimesMultiplyM :

        mov ecx, eax

    labelLoopStart :
        cmp ebx, 1
        jz labelEnd

        dec ebx
        imul eax, ecx
        jmp labelLoopStart

    labelEnd :
        ret
    }
    return 0;
}
```

Register values are the following,

EAX = 00000002 EBX = 00000003 ECX = 00000000 EDX = 00000001 ESI = 006ACFC0 EDI = 00000000 EIP = 0078103D ESP = 0135F764 EBP = 0135F834 EFL = 00000204

Relevant memory is the following,

0x0135F75C 014c0000  
0x0135F760 0135f740  
0x0135F764 00781034  
0x0135F768 00781640  
0x0135F76C 00781640  
0x0135F770 0119a000  
0x0135F774 cccccccc  
0x0135F778 cccccccc  
0x0135F77C cccccccc  
0x0135F780 cccccccc  

Disassembly is the following,  

<img src="Images/Q_57_14.jpg" width="400"/>

 What will be the value of EIP register after the execution of the instruction, cmp ebx, 1, in the above program?  

 a) 0078103D  
 b) 0078103F  
 c) 00781042  
 d) 00781044  

  **Answer** c) 

 **Description** 

 EIP register will always point to the next instruction which here is, jz labelEnd, whose EIP is 00781042 and it is evident from the disassembly shown.  

 ---
 ---


 15 : We have the below program,  

 ```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
    nTimesMultiplyM :

        mov ecx, eax

    labelLoopStart :
        cmp ebx, 1
        jz labelEnd

        dec ebx
        imul eax, ecx
        jmp labelLoopStart

    labelEnd :
        ret
    }
    return 0;
}
```

Register values are the following,

EAX = 00000002 EBX = 00000003 ECX = 00000000 EDX = 00000001 ESI = 006ACFC0 EDI = 00000000 EIP = 0078103D ESP = 0135F764 EBP = 0135F834 EFL = 00000204

Relevant memory is the following,

0x0135F75C 014c0000  
0x0135F760 0135f740  
0x0135F764 00781034  
0x0135F768 00781640  
0x0135F76C 00781640  
0x0135F770 0119a000  
0x0135F774 cccccccc  
0x0135F778 cccccccc  
0x0135F77C cccccccc  
0x0135F780 cccccccc  

Disassembly is the following,

 

What will be the value of EIP register after the execution of the instruction, jz labelEnd, in the above program?
 




