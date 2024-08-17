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

<img src="" width="400"/>

What will be the value of the memory location 003BF848, after the execution of the instruction mov dword ptr[esp + 8], 12?
