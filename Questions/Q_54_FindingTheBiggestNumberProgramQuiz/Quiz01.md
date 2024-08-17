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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_2.jpg" width="400"/>

What will be the value of the memory location 003BF840, after the execution of the instruction mov dword ptr[esp], 77?  

a) 779432f2  
b) 00668398  
c) 006683a0  
d) 0000004D (Hex value of 77)  

**Answer** d) 

**Description** 

mov dword ptr[esp], 77 instruction will move the value 77 (Hex value is 4D) to the memory location [esp] that is 003BF840.  

---
---


3 : We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_3.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp], 77 (Hex value of 77 is 4D)?  

a) 00F413E1  
b) 00F413E8  
c) 00F413F0  
d) 00F413F8  

**Answer** b) 

**Description**

EIP will always point to the next instruction that is 00F413E8, which is evident from the disassembly shown.  

---
---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 4], 35
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_4.jpg" width="400"/>

Value of which memory location will become 23 (Hex value of 35) after the execution of the instruction mov dword ptr[esp + 4], 35?  

a) 003BF840  
b) 003BF844  
c) 003BF848  
d) 003BF84C  

**Answer** b) 

**Description**

[esp + 4] is next memory location after [esp] which is 003BF844 and it will become 23 (Hex value of 35). It is understood from the relevant memory locations shown. 

---
---


5 :We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 4], 35
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_5.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp + 4], 35? (Hex value of 35 is 23)  

a) 00F413E1  
b) 00F413E8  
c) 00F413F0  
d) 00F413F8  

**Answer** c) 

**Description**

EIP will always point to the next instruction that is 00F413F0, which is evident from the disassembly shown.  

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 8], 12
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_6.jpg" width="400"/>

What will be the value of the memory location 003BF848, after the execution of the instruction mov dword ptr[esp + 8], 12?  

a) 00000008  
b) 0000000C (Hex value of 12)  
c) 00000000  
d) CCCCCCCC  

**Answer** b) 

**Description**

mov dword ptr[esp + 8], 12 instruction will move the value 12 (Hex value is C) to the memory location [esp + 8] that is 003BF848.  

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 8], 12
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_7.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp + 8], 12? (Hex value of 12 is 0C)  

a) 00F413E1  
b) 00F413E8  
c) 00F413F0  
d) 00F413F8  

**Answer** d) 

**Description**

EIP will always point to the next instruction that is 00F413F8, which is evident from the disassembly shown.  

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 0Ch], 4
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_8.jpg" width="400"/>

Value of which memory location will become 4, after the execution of the instruction mov dword ptr[esp + 0Ch], 4?  

a) 003BF840  
b) 003BF844  
c) 003BF848  
d) 003BF84C  

**Answer** d) 

**Description**

[esp + 0Ch] is the third memory location after [esp] which is 003BF84C and it will become 4. It is understood from the relevant memory locations shown.   

---
---


9 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 0Ch], 4
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_9.jpg" width="400"/>
  
What will be the value of EIP after the execution of the instruction mov dword ptr[esp + 0Ch], 4?  

a) 00F41400  
b) 00F413E8  
c) 00F413F0  
d) 00F413F8  

**Answer** a) 

**Description**

EIP will always point to the next instruction that is 00F41400, which is evident from the disassembly shown.  

---
---


10 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 10h], 66
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_10.jpg" width="400"/>

Value of which memory location will become 42 (Hex value of 66), after the execution of the instruction mov dword ptr[esp + 10h], 66?  

a) 003BF840  
b) 003BF844  
c) 003BF848  
d) 003BF850  

**Answer** d) 

**Description**

[esp + 10h] is the fourth memory location after [esp] which is 003BF850 and it is understood from the relevant memory locations shown.   

---
---


11 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov dword ptr[esp + 10h], 66
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_11.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov dword ptr[esp + 10h], 66? (Hex value of 66 is 42)  

a) 00F41408  
b) 00F413E8  
c) 00F413F0  
d) 00F413F8  

**Answer** a) 

**Description**

EIP will always point to the next instruction that is 00F41408, which is evident from the disassembly shown.  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov eax, 0
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_12.jpg" width="400"/>

What will be the value of EAX after the execution of the instruction mov eax, 0?  

a) CCCCCCCC  
b) 00000000  
c) 00000001  
d) None of the above  

**Answer** b) 

**Description**

Here we are moving 0 to the register EAX by the instruction mov eax, 0. So the value of EAX register will become 00000000.  

---
---


13 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov eax, 0
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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_13.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov eax, 0?  

a) 00F41408  
b) 00F413E8  
c) 00F413F0  
d) 00F4140D  

**Answer** d) 

**Description**

EIP will always point to the next instruction that is 00F4140D, which is evident from the disassembly shown.  

---
---


14 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	    mov ecx, 0
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

What will be the value of ECX after the execution of the instruction mov ecx, 0?


