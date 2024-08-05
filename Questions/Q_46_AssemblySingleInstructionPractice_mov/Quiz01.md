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


11 : 
