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


2 : We have the below program,  

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

0x003DF888 00 00 00 00
0x003DF88C 00 00 00 00
0x003DF890 00 e0 fd 7e
0x003DF894 cc cc cc cc
0x003DF898 cc cc cc cc
0x003DF89C cc cc cc cc
0x003DF8A0 cc cc cc cc
0x003DF8A4 cc cc cc cc
0x003DF8A8 cc cc cc cc
0x003DF8AC cc cc cc cc
0x003DF8B0 cc cc cc cc
0x003DF8B4 cc cc cc cc

What is the value of EAX after the line, mov eax, ebx in the above program?  

a) CCCCCCCC  
b) 7EFDE000  
c) 00000000  
d) None of the above  

**Answer** b) 

**Description**  

In the above program the value of ebx will move to eax. So eax will become ebx value, that is 7EFDE000.

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 0x4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001AFA08 EIP = 012813DE ESP = 001AF93C EBP = 001AFA08 EFL = 00000204

Relevant memory is the following,

0x001AF93C 00 00 00 00
0x001AF940 00 00 00 00
0x001AF944 00 e0 fd 7e
0x001AF948 cc cc cc cc
0x001AF94C cc cc cc cc
0x001AF950 cc cc cc cc
0x001AF954 cc cc cc cc
0x001AF958 cc cc cc cc
0x001AF95C cc cc cc cc
0x001AF960 cc cc cc cc
0x001AF964 cc cc cc cc
0x001AF968 cc cc cc cc

Which register/s will change after the execution of the line sub esp, 0x4 in the above program?  

a) EIP  
b) ESP  
c) EAX  
d) Both a & b  

**Answer** d) 

**Description** 

EIP is a strictly special purpose register which always points to the next instruction to execute. So it will change after all instructions. ESP will change here because we are allocating stack memory, which is nothing but subtraction.   

---
---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	sub esp, 0x4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 001AFA08 EIP = 012813DE ESP = 001AF93C EBP = 001AFA08 EFL = 00000204 

Relevant memory is the following,

0x001AF93C 00 00 00 00
0x001AF940 00 00 00 00
0x001AF944 00 e0 fd 7e
0x001AF948 cc cc cc cc
0x001AF94C cc cc cc cc
0x001AF950 cc cc cc cc
0x001AF954 cc cc cc cc
0x001AF958 cc cc cc cc
0x001AF95C cc cc cc cc
0x001AF960 cc cc cc cc
0x001AF964 cc cc cc cc
0x001AF968 cc cc cc cc

What is the value of ESP after the execution of the line sub esp, 0x4 in the above program?  

a) 012813DE-0x4=012813DA  
b) 001AF93C-0x4=001AF938  
c) 00000204-0x4=00000200  
d) 001AF93C+0x4=001AF940 

**Answer** b) 

**Description** 

sub esp, 0x4 is nothing but allocation of 4 bytes of stack memory, which is a dword. So sub esp, 0x4 is current ESP value minus 0x4, which is here option b). Option a) is subtracting 0x4 from EIP, which is wrong. Option c) is subtracting 0x4 from EFL, which is also wrong. Option d) is adding 0x4 to ESP, which is deallocation of stack memory. It is also incorrect. 

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	mov eip, 0x4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003DF778 EIP = 00BB13DE ESP = 003DF6AC EBP = 003DF778 EFL = 00000204 

Relevant memory is the following,

0x003DF6AC 00 00 00 00
0x003DF6B0 00 00 00 00
0x003DF6B4 00 e0 fd 7e
0x003DF6B8 cc cc cc cc
0x003DF6BC cc cc cc cc
0x003DF6C0 cc cc cc cc
0x003DF6C4 cc cc cc cc
0x003DF6C8 cc cc cc cc
0x003DF6CC cc cc cc cc
0x003DF6D0 cc cc cc cc
0x003DF6D4 cc cc cc cc
0x003DF6D8 cc cc cc cc

What is the value of EIP after executing the instruction mov eip, 0x4 in the above program?  

a) 00000004  
b) 00000000  
c) Illegal instruction  
d) None of the above  

**Answer** c) 

**Description**

EIP is a strictly special purpose register which always point to the next instruction. We cannot move a value to EIP register by instructions like mov eip, 0x4. By jmp instructions, call & ret instructions we can move values to EIP. But with above instruction we cannot move a value to EIP. So the above one is an illegal instruction.

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	add eax, 0x4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002AFCB8 EIP = 002E13DE ESP = 002AFBEC EBP = 002AFCB8 EFL = 00000200 

Relevant memory is the following,

0x002AFBEC 00 00 00 00
0x002AFBF0 00 00 00 00
0x002AFBF4 00 e0 fd 7e
0x002AFBF8 cc cc cc cc
0x002AFBFC cc cc cc cc
0x002AFC00 cc cc cc cc
0x002AFC04 cc cc cc cc
0x002AFC08 cc cc cc cc
0x002AFC0C cc cc cc cc
0x002AFC10 cc cc cc cc
0x002AFC14 cc cc cc cc
0x002AFC18 cc cc cc cc

Which register/s will change after the execution of the line add eax, 0x4 in the above program?  

a) ESP  
b) EAX  
c) EBX  
d) None of the registers will change  

**Answer** b) 

**Description**

The above instruction will change EAX register, because we are adding 0x4 to eax. ESP & EBX will have no change, because we are not touching them.  

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	add eax, 0x4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002AFCB8 EIP = 002E13DE ESP = 002AFBEC EBP = 002AFCB8 EFL = 00000200 

Relevant memory is the following,

0x002AFBEC 00 00 00 00
0x002AFBF0 00 00 00 00
0x002AFBF4 00 e0 fd 7e
0x002AFBF8 cc cc cc cc
0x002AFBFC cc cc cc cc
0x002AFC00 cc cc cc cc
0x002AFC04 cc cc cc cc
0x002AFC08 cc cc cc cc
0x002AFC0C cc cc cc cc
0x002AFC10 cc cc cc cc
0x002AFC14 cc cc cc cc
0x002AFC18 cc cc cc cc

What is the value of EAX after the line add eax, 0x4 in the above program?  

a) CCCCCCCC+0x4=CCCCCCD0  
b) CCCCCCCC-0x4=CCCCCCC8  
c) No change  
d) Illegal instruction  

**Answer** a) 

**Description**

Here we are adding 0x4 to EAX, so the value of EAX will be added by 0x4. Option b) is incorrect because it is subtracting  0x4 from EAX. Option c) is also wrong, because EAX will get added by 0x4. Option d) is incorrect, because it is not an illegal instruction.

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	inc eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0039F734 EIP = 013413DE ESP = 0039F668 EBP = 0039F734 EFL = 00000204 

Relevant memory is the following,

0x0039F668 00 00 00 00
0x0039F66C 00 00 00 00
0x0039F670 00 e0 fd 7e
0x0039F674 cc cc cc cc
0x0039F678 cc cc cc cc
0x0039F67C cc cc cc cc
0x0039F680 cc cc cc cc
0x0039F684 cc cc cc cc
0x0039F688 cc cc cc cc
0x0039F68C cc cc cc cc
0x0039F690 cc cc cc cc
0x0039F694 cc cc cc cc

Which register/s will change after the execution of the line, inc eax, in the above program?  

a) ESP  
b) EIP  
c) EAX  
d) Both b & c  

**Answer** d) 

**Description**

The above instruction, inc eax will increase the value of EAX by 1. EIP will change after every instruction. So answer is both b & c.

---
---


9 :We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	inc eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0039F734 EIP = 013413DE ESP = 0039F668 EBP = 0039F734 EFL = 00000204 

Relevant memory is the following,

0x0039F668 00 00 00 00
0x0039F66C 00 00 00 00
0x0039F670 00 e0 fd 7e
0x0039F674 cc cc cc cc
0x0039F678 cc cc cc cc
0x0039F67C cc cc cc cc
0x0039F680 cc cc cc cc
0x0039F684 cc cc cc cc
0x0039F688 cc cc cc cc
0x0039F68C cc cc cc cc
0x0039F690 cc cc cc cc
0x0039F694 cc cc cc cc

What is the value of EAX after the line, inc eax, in the above program?  

a) CCCCCCCC  
b) CCCCCCCC+1=CCCCCCCD  
c) CCCCCCCC-1=CCCCCCCB  
d) None of the above  

**Answer** b) 

**Description**

The above instruction, inc eax will increase the value of EAX by 1. Option a) is incorrect because EAX will change. Option c) is also wrong because EAX is added by 1, not subtracted by 1.

---
---


10 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	sub ebx, 0x7
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0044FC18 EIP = 011E13DE ESP = 0044FB4C EBP = 0044FC18 EFL = 00000200 

Relevant memory is the following,

0x0044FB4C 00 00 00 00
0x0044FB50 00 00 00 00
0x0044FB54 00 e0 fd 7e
0x0044FB58 cc cc cc cc
0x0044FB5C cc cc cc cc
0x0044FB60 cc cc cc cc
0x0044FB64 cc cc cc cc
0x0044FB68 cc cc cc cc
0x0044FB6C cc cc cc cc
0x0044FB70 cc cc cc cc
0x0044FB74 cc cc cc cc
0x0044FB78 cc cc cc cc

Which register/s will change after the execution of the line sub ebx, 0x7 in the above program?  

a) EBX  
b) ESP  
c) EIP  
d) Both a & c  

**Answer** d) 

**Description**

We are subtracting a value from EBX, so it will surely change. We are not touching on ESP, so it will be unchanged. EIP will change after all instructions, because it will be pointing to next instruction.

---
---


11 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	sub ebx, 0x7
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0044FC18 EIP = 011E13DE ESP = 0044FB4C EBP = 0044FC18 EFL = 00000200 

Relevant memory is the following,

0x0044FB4C 00 00 00 00
0x0044FB50 00 00 00 00
0x0044FB54 00 e0 fd 7e
0x0044FB58 cc cc cc cc
0x0044FB5C cc cc cc cc
0x0044FB60 cc cc cc cc
0x0044FB64 cc cc cc cc
0x0044FB68 cc cc cc cc
0x0044FB6C cc cc cc cc
0x0044FB70 cc cc cc cc
0x0044FB74 cc cc cc cc
0x0044FB78 cc cc cc cc

What is the value of EBX after the line sub ebx, 0x7 in the above program?  

a) 7EFDE000-0x7=7EFDDFF9  
b) 011E13DE-0x7=011E13D7  
c) 7EFDE000+0x7=7EFDE007  
d) None of the above  

**Answer** a) 

**Description**

We are subtracting 0x7 from EBX, so its value will be reduced by 7. EIP value will change, but it will be the address of the next instruction. Adding 0x7 is also wrong, because we are subtracting.

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	mov dword ptr[esp], 0x6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002EFF14 EIP = 010E13DE ESP = 002EFE48 EBP = 002EFF14 EFL = 00000200 

Relevant memory is the following,

0x002EFE48 00 00 00 00
0x002EFE4C 00 00 00 00
0x002EFE50 00 e0 fd 7e
0x002EFE54 cc cc cc cc
0x002EFE58 cc cc cc cc
0x002EFE5C cc cc cc cc
0x002EFE60 cc cc cc cc
0x002EFE64 cc cc cc cc
0x002EFE68 cc cc cc cc
0x002EFE6C cc cc cc cc
0x002EFE70 cc cc cc cc
0x002EFE74 cc cc cc cc

Which will change after the execution of the line, mov dword ptr[esp], 0x6 in the above program?  

a) Value of the memory location 0x002EFE48 will become 00000006  
b) ESP register will become 00000006  
c) Value of the memory location 0x002EFE4C will become 00000006  
d) No change will happen  

**Answer** a) 

**Description**

mov dword ptr[esp], 0x6 means that we are moving 0x6 into the memory location which is pointed by the ESP which is equal to 0x002EFE48. Address inside the ESP register, which is the value inside the ESP register will not change, but the value inside that memory location is changing. The value inside the memory location which is pointed by the ESP which is equal to 0x002EFE4C will not change, because it is next memory location, which is [esp + 4].

---
---


13 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	mov eax, 0x5
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0036FA50 EIP = 001713DE ESP = 0036F984 EBP = 0036FA50 EFL = 00000204 

Relevant memory is the following,

0x0036F984 00 00 00 00
0x0036F988 00 00 00 00
0x0036F98C 00 e0 fd 7e
0x0036F990 cc cc cc cc
0x0036F994 cc cc cc cc
0x0036F998 cc cc cc cc
0x0036F99C cc cc cc cc
0x0036F9A0 cc cc cc cc
0x0036F9A4 cc cc cc cc
0x0036F9A8 cc cc cc cc
0x0036F9AC cc cc cc cc
0x0036F9B0 cc cc cc cc

Which register/s will change after the execution of the line mov eax, 0x5 in the above program?  

a) EIP  
b) EAX  
c) ECX  
d) Both a& b  

**Answer** d) 

**Description**

EIP is a strictly special purpose register which always points to the next instruction to execute. So it will change after all instructions. EAX will change here because we are moving a value to EAX. ECX will have no change as we are not touching it.  

---
---


14 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov eax, 0x5
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0036FA50 EIP = 001713DE ESP = 0036F984 EBP = 0036FA50 EFL = 00000204 

Relevant memory is the following,

0x0036F984 00 00 00 00
0x0036F988 00 00 00 00
0x0036F98C 00 e0 fd 7e
0x0036F990 cc cc cc cc
0x0036F994 cc cc cc cc
0x0036F998 cc cc cc cc
0x0036F99C cc cc cc cc
0x0036F9A0 cc cc cc cc
0x0036F9A4 cc cc cc cc
0x0036F9A8 cc cc cc cc
0x0036F9AC cc cc cc cc
0x0036F9B0 cc cc cc cc

What is the value of EAX after the execution of the line mov eax, 0x5 in the above program?  

a) CCCCCCCC  
b) 00000005  
c) 00000000  
d) 001713DE  

**Answer** b) 

**Description**

Here we are moving the value 0x5 to EAX. So EAX register will become 00000005.

---
---


15 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	mov ecx ebx
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0031FD58 EIP = 009C13DE ESP = 0031FC8C EBP = 0031FD58 EFL = 00000200 

Relevant memory is the following,

0x0031FC8C 00 00 00 00
0x0031FC90 00 00 00 00
0x0031FC94 00 e0 fd 7e
0x0031FC98 cc cc cc cc
0x0031FC9C cc cc cc cc
0x0031FCA0 cc cc cc cc
0x0031FCA4 cc cc cc cc
0x0031FCA8 cc cc cc cc
0x0031FCAC cc cc cc cc
0x0031FCB0 cc cc cc cc
0x0031FCB4 cc cc cc cc
0x0031FCB8 cc cc cc cc

Which register/s will change after the execution of the line, mov ecx ebx in the above program?  

a) ECX  
b) EBX  
c) EIP  
d) Incorrect instruction  

**Answer** d) 

**Description**

The above instruction has a syntax error, because there is no comma after ecx. So this is an incorrect instruction. Correct instruction is mov ecx, ebx. 

---
---


16 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
	mov dword ptr[esp + 4], 0x9
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FCB8 EIP = 009513DE ESP = 0038FBEC EBP = 0038FCB8 EFL = 00000200 

Relevant memory is the following,

0x0038FBEC 00 00 00 00
0x0038FBF0 00 00 00 00
0x0038FBF4 00 e0 fd 7e
0x0038FBF8 cc cc cc cc
0x0038FBFC cc cc cc cc
0x0038FC00 cc cc cc cc
0x0038FC04 cc cc cc cc
0x0038FC08 cc cc cc cc
0x0038FC0C cc cc cc cc
0x0038FC10 cc cc cc cc
0x0038FC14 cc cc cc cc
0x0038FC18 cc cc cc cc

Which will change after the execution of the line, mov dword ptr[esp + 4], 0x9 in the above program?  

a) Value of the memory location 0x0038FBEC will become 00000009  
b) ESP register will become 00000009  
c) Value of the memory location 0x0038FBF0 will become 00000009  
d) No change will happen  

**Answer** c) 

**Description**

mov dword ptr[esp + 4], 0x9 means that we are moving 0x9 to the value of the memory location which is pointed by the ESP which is equal to 0x0038FBF0 . ESP register will not change, but the value of the memory location is changing. Value of the memory location 0x0038FBEC will not change because it is the memory location, which is [esp].

---
---


17 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov ebx, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0018FEBC EIP = 000513DE ESP = 0018FDF0 EBP = 0018FEBC EFL = 00000204 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

What will change after the execution of the above instruction, mov ebx, dword ptr[esp] in the above program?  

a) Value in the memory location [esp]  
b) EBX  
c) Value in the memory location [esp + 4]  
d) ECX  

**Answer** b) 

**Description**

This instruction moves the value in the memory location [esp] to ebx. So EBX register will change. ECX register will have no change as we are not touching it. Value of the memory locations also will not have any change.

---
---


18 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov ebx, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0018FEBC EIP = 000513DE ESP = 0018FDF0 EBP = 0018FEBC EFL = 00000204 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

What will be the value of EBX after the execution of the above instruction?  

a) 00000000  
b) 00 e0 fd 7e  
c) 7EFDE000  
d) 0018FDF0  

**Answer** a) 

**Description**

This instruction moves the value in the memory location [esp] to ebx. So ebx register will become 00000000.

---
---


19 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov dword ptr[esp + 4], dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0018FEBC EIP = 000513DE ESP = 0018FDF0 EBP = 0018FEBC EFL = 00000204 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

What will change after the execution of the above instruction, mov dword ptr[esp + 4], dword ptr[esp] in the program?  

a) Value of the memory location [esp + 4]  
b) Value of the memory location [esp]  
c) No change  
d) Illegal instruction  

**Answer** d) 

**Description**

We cannot move a value from one memory location to another. So the above instruction is an illegal instruction. We can move a value from one memory location to another only with the help of registers like this, mov eax, dword ptr[esp + 4] and then mov dword ptr[esp], eax.   

---
---


20 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov dword ptr[esp + 8], 0x2
    }
    return 0; 
}
```
Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003BF734 EIP = 002813DE ESP = 0018FDF0 EBP = 003BF734 EFL = 00000204 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

Which will change after the execution of the line, mov dword ptr[esp + 8], 0x2 in the above program?  

a) Value of the memory location 0x0018FDF4 will become 00000002  
b) ESP register will become 00000002  
c) Value of the memory location 0x0018FDF8 will become 00000002  
d) No change will happen  

**Answer** c) 

**Description**

mov dword ptr[esp + 8], 0x2 means that we are moving 0x2 to the value of the memory location 0x0018FDF8. ESP register will not change, but value of the memory location pointed by the ESP is changing. Value of the memory location 0x0018FDF4 will not change because it is [esp + 4].  

---
---


21 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov dword ptr[esp], eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040FC48 EIP = 000C13DE ESP = 0018FDF0 EBP = 0040FC48 EFL = 00000204 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

What will change after the execution of the above instruction, mov dword ptr[esp], eax in the program?  

a) Value of the memory location [esp]  
b) EAX  
c) Value of the memory location [esp + 4]   
d) ECX  

**Answer** a) 

**Description**

Here the value of eax will move to the value of the memory location [esp]. So it will change. ECX will have no change as we are not touching it.  

---
---


22 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        mov dword ptr[esp], eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040FC48 EIP = 000C13DE ESP = 0018FDF0 EBP = 0040FC48 EFL = 00000204 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

What will be the value of memory location [esp] after the execution of the above instruction?  

a) CCCCCCCC  
b) 00000000  
c) 00e0fd7e  
d) None of the above  

**Answer** a) 

**Description**

Here the value of eax will move to the value of the memory location [esp]. So it will become CCCCCCCC.  

---
---


23 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub edx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002DF7D0 EIP = 013E13DE ESP = 0018FDF0 EBP = 002DF7D0 EFL = 00000200 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

Which will change after the execution of the above instruction?  

a) EDX  
b) EIP  
c) EFL  
d) All of the above  

**Answer** d) 

**Description**

Here EDX will change as we are subtracting 1 from EDX. EIP changes with every instruction. EFL changes, the Zero flag will become set as the result of the operation is zero.  

---
---


24 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub edx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 002DF7D0 EIP = 013E13DE ESP = 0018FDF0 EBP = 002DF7D0 EFL = 00000200 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

What will be the value of EDX after the execution of the above instruction?  

a) 00000000  
b) 00000001  
c) 00000002  
d) None of the above  

**Answer** a) 

**Description**

The value of EDX will become 00000000 as we are subtracting 1 from 1.  

---
---


25 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        add edx, 1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0048FC1C EIP = 003113DE ESP = 0018FDF0 EBP = 0048FC1C EFL = 00000204 

Relevant memory is the following,

0x0018FDF0 00 00 00 00
0x0018FDF4 00 00 00 00
0x0018FDF8 00 e0 fd 7e
0x0018FDFC cc cc cc cc
0x0018FE00 cc cc cc cc
0x0018FE04 cc cc cc cc
0x0018FE08 cc cc cc cc
0x0018FE0C cc cc cc cc
0x0018FE10 cc cc cc cc
0x0018FE14 cc cc cc cc
0x0018FE18 cc cc cc cc
0x0018FE1C cc cc cc cc

What will be the value of EDX after the instruction add edx, 1 in the above program?  

a) 00000000  
b) 00000001  
c) 00000002  
d) None of the above  

**Answer** c) 

**Description**

The value of EDX register was 1 before executing the instruction. So it will become 00000002 after adding 1 to it.

---
---






