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

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13DE ESP = 0133FA58 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_1.jpg" width="400"/>

What will be the value of ESP after the execution of the instruction sub esp, 20 in the above program?   

a) 0133FA58  
b) 0133FA54  
c) 0133FA48  
d) 0133FA44  

**Answer** d)

**Description** 

Sub esp, 20 means we are allocating 5 locations of stack memory 4 bytes each. So the value of ESP will be 0133FA44, which is evident from the stack memory locations given.  

---
---


2 : We have the below program,  

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

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13DE ESP = 0133FA58 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_2.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction sub esp, 20 in the above program?  

a) 00FD13DE  
b) 00FD13E1  
c) 00FD13E8  
d) 00FD13F0  

**Answer** d)

**Description**

EIP will always point to next instruction which here is 00FD13E1 and it is evident from the disassembly shown.  

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp], 0x1
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_3.jpg" width="400"/>

What will be the value of the memory location 0133FA44, after the execution of the instruction mov dword ptr[esp], 0x1?  

a) 00000001  
b) 0133FA44  
c) 00000035  
d) 00FD13E1  

**Answer** a)

**Description**

mov dword ptr[esp], 0x1 instruction will move the value 1 to the memory location [esp] that is 0133FA44.  

---
---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp], 0x1
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_4.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp], 0x1?  

a) 00FD13DE  
b) 00FD13E1  
c) 00FD13E8  
d) 00FD13F0  

**Answer** c)

**Description**

EIP will always point to next instruction which here is 00FD13E8 and it is evident from the disassembly shown.  

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 4], 0x35
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_5.jpg" width="400"/>

Value of which memory location will become 35 after the execution of the instruction mov dword ptr[esp + 4], 0x35?  

a) 0133FA44  
b) 0133FA48  
c) 0133FA4C  
d) 0133FA50  

**Answer** b)

**Description**

[esp + 4] is the next memory location after [esp], which is 0133FA48 and it is understood from the relevant memory locations shown and it will become 0x35.   

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 4], 0x35
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_6.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp + 4], 0x35?  

a) 00FD13DE  
b) 00FD13E1  
c) 00FD13E8  
d) 00FD13F0  

**Answer** d)

**Description**

EIP will always point to next instruction which here is 00FD13F0 and it is evident from the disassembly shown.  

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 8], 0x12
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000   
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_7.jpg" width="400"/>

What will be the value of the memory location 0133FA4C, after the execution of the instruction mov dword ptr[esp + 8], 0x12?   

a) 00000001  
b) 00000035  
c) 00000012  
d) 0133FA50  

**Answer** c)

**Description**

mov dword ptr[esp + 8], 0x12 instruction will move the value 0x12 to the memory location [esp + 8] that is 0133FA4C.  

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 8], 0x12
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000   
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_8.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp + 8], 0x12?  

a) 00FD13DE  
b) 00FD13E1  
c) 00FD13E8  
d) 00FD13F8  

**Answer** d)

**Description**

EIP will always point to next instruction which here is 00FD13F8 and it is evident from the disassembly shown.  

---
---


9 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 0Ch], 0x4
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_9.jpg" width="400"/>

Value of which memory location will become 0x4 after the execution of the instruction mov dword ptr[esp + 0Ch], 0x4?  

a) 0133FA44  
b) 0133FA48  
c) 0133FA4C  
d) 0133FA50  

**Answer** d)

**Description**

[esp + 0Ch] is the third memory location after [esp], which is 0133FA50 and it is understood from the relevant memory locations shown and it will become 0x4.   

---
---


10 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 0Ch], 0x4
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_10.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp + 0Ch], 0x4?  

a) 00FD13DE  
b) 00FD13E1  
c) 00FD13E8  
d) 00FD1400  

**Answer** d)

**Description**

EIP will always point to next instruction which here is 00FD1400 and it is evident from the disassembly shown.  

---
---


11 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 10h], 0x1
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_11.jpg" width="400"/>

What will be the value of the memory location 0133FA54, after the execution of the instruction mov dword ptr[esp + 10h], 0x1?  

a) 00000001  
b) 00000035  
c) 00000012  
d) 0133FA50  

**Answer** a)

**Description**

mov dword ptr[esp + 10h], 0x1 instruction will move the value 0x1 to the memory location [esp + 10h] that is 0133FA54, which is the fourth memory location from [esp].  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 10h], 0x1
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 01055000 ECX = 00000000 EDX = 00000001 ESI = 00FD1078 EDI = 0133FB24 EIP = 00FD13E1 ESP = 0133FA44 EBP = 0133FB24 EFL = 00000200

Relevant memory is the following,

0x0133FA38 00fd1078  
0x0133FA3C 01055000  
0x0133FA40 01560000  
0x0133FA44 015695d0  
0x0133FA48 f2b63fe4  
0x0133FA4C 01560000  
0x0133FA50 0133fa30  
0x0133FA54 0133fa74  
0x0133FA58 00fd1078  
0x0133FA5C 00fd1078  
0x0133FA60 01055000  

Disassembly is the following,  

<img src="Images/Q_56_12.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp + 10h], 0x1?  

a) 00FD13DE  
b) 00FD13E1  
c) 00FD13E8  
d) 00FD1408  

**Answer** d)

**Description**

EIP will always point to next instruction which here is 00FD1408 and it is evident from the disassembly shown.  

---
---


13 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
	__asm
	{
	labelLoopStartOuter:
	    cmp ecx, 4
	    jz EndOuterLoop

	EndOuterLoop :
	    add esp, 20
	}
	return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 00000000 ECX = 00000000 EDX = 00000000 ESI = 00000000 EDI = 00000000 EIP = 00CA1426 ESP = 010FFB9C EBP = 010FFC7C EFL = 00000214

Relevant memory is the following,

0x010FFB90 00ca1078  
0x010FFB94 00f65000  
0x010FFB98 013a0000  
0x010FFB9C 00000001  
0x010FFBA0 00000035  
0x010FFBA4 00000012  
0x010FFBA8 00000004  
0x010FFBAC 00000001  
0x010FFBB0 00ca1078  
0x010FFBB4 00ca1078  
0x010FFBB8 00f65000  

Disassembly is the following,  

<img src="Images/Q_56_13.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction cmp ecx, 4 in the above program?  

a) 00CA1426  
b) 00CA1429  
c) 00CA142B  
d) 00CA145B  

**Answer** b)

**Description**

EIP will always be pointing to the next instruction to execute which here is 00CA1429 and it is evident from the disassembly shown.   

---
---


14 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
	__asm
	{
	labelLoopStartOuter:
	    cmp ecx, 4
	    jz EndOuterLoop

	EndOuterLoop :
	    add esp, 20
	}
	return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 00000000 ECX = 00000000 EDX = 00000000 ESI = 00000000 EDI = 00000000 EIP = 00CA1426 ESP = 010FFB9C EBP = 010FFC7C EFL = 00000214

Relevant memory is the following,

0x010FFB90 00ca1078  
0x010FFB94 00f65000  
0x010FFB98 013a0000  
0x010FFB9C 00000001  
0x010FFBA0 00000035  
0x010FFBA4 00000012  
0x010FFBA8 00000004  
0x010FFBAC 00000001  
0x010FFBB0 00ca1078  
0x010FFBB4 00ca1078  
0x010FFBB8 00f65000  

Disassembly is the following,  

<img src="Images/Q_56_14.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction jz EndOuterLoop if the value of ECX is 0, in the above program?  

a) 00CA1426  
b) 00CA1429  
c) 00CA142B  
d) 00CA145B  

**Answer** c)

**Description**

After the execution of the instruction, jz EndOuterLoop, EIP will be pointing to next instruction whose EIP is 00CA142B. It will not jump to EndOuterLoop, as when ECX is 0, jump on zero (jz) will not succeed, because 0 – 4 is not equal to 0. Je is same as jz, as jump on zero means that both values are equal, that is je.  

---
---


15 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
	__asm
	{
	labelLoopStartOuter:
	    cmp ecx, 4
	    jz EndOuterLoop

	EndOuterLoop :
	    add esp, 20
	}
	return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 00000000 ECX = 00000000 EDX = 00000000 ESI = 00000000 EDI = 00000000 EIP = 00CA1426 ESP = 010FFB9C EBP = 010FFC7C EFL = 00000214

Relevant memory is the following,

0x010FFB90 00ca1078  
0x010FFB94 00f65000  
0x010FFB98 013a0000  
0x010FFB9C 00000001  
0x010FFBA0 00000035  
0x010FFBA4 00000012  
0x010FFBA8 00000004  
0x010FFBAC 00000001  
0x010FFBB0 00ca1078  
0x010FFBB4 00ca1078  
0x010FFBB8 00f65000  

Disassembly is the following,  

<img src="Images/Q_56_15.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction jz EndOuterLoop if the value of ECX is 1, in the above program?  

a) 00CA1426  
b) 00CA142B  
c) 00CA1429  
d) 00CA145B  

**Answer** c)

**Description**

After the execution of the instruction, jz EndOuterLoop, EIP will be pointing to next instruction whose EIP is 00CA142B. It will not jump to EndOuterLoop, as when ECX is 1, jump on zero (jz) will not succeed, because 1 – 4 is not equal to 0. Je is same as jz, as jump on zero means that both values are equal, that is je.  

---
---


16 : 


