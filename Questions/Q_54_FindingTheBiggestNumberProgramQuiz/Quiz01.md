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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_14.jpg" width="400"/>

What will be the value of ECX after the execution of the instruction mov ecx, 0?  

a) CCCCCCCC  
b) 00000000  
c) 00000001  
d) None of the above  

**Answer** b) 

**Description**

Here we are moving 0 to the register ECX by the instruction mov ecx, 0. So the value of ECX register will become 00000000. 

---
---


15 : We have the below program,  

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

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_15.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov ecx, 0?  

a) 00F41408  
b) 00F413E8  
c) 00F413F0  
d) Point to next instruction  

**Answer** d) 

**Description**

EIP will always point to next instruction to execute.  

---
---


16 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FC84 EIP = 003F1412 ESP = 0033FBA4 EBP = 0033FC84 EFL = 00000202

Relevant memory is the following,

0x0033FB94 7701041d  
0x0033FB98 01e61843  
0x0033FB9C fffffffe  
0x0033FBA0 76fd36fa  
0x0033FBA4 0000004d  
0x0033FBA8 00000023  
0x0033FBAC 0000000c  
0x0033FBB0 00000004  
0x0033FBB4 00000042  
0x0033FBB8 00000000  
0x0033FBBC 00000000  
0x0033FBC0 7efde000  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_16.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction cmp ecx, 5?  

a) 003F1412  
b) 003F1415  
c) 003F1417  
d) 003F1425  

**Answer** b) 

**Description**

After the execution of cmp ecx, 5 the EIP will be pointing to next instruction whose EIP is 003F1415 which is evident from the disassembly. Je is same as jz, as jump on zero means that both values are equal, that is je.

---
---


17 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FC84 EIP = 003F1412 ESP = 0033FBA4 EBP = 0033FC84 EFL = 00000202

Relevant memory is the following,

0x0033FB94 7701041d  
0x0033FB98 01e61843  
0x0033FB9C fffffffe   
0x0033FBA0 76fd36fa  
0x0033FBA4 0000004d  
0x0033FBA8 00000023  
0x0033FBAC 0000000c  
0x0033FBB0 00000004  
0x0033FBB4 00000042  
0x0033FBB8 00000000  
0x0033FBBC 00000000  
0x0033FBC0 7efde000  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_17.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz labelExitLoop, if the value of ECX is 0?  

a) 003F1412  
b) 003F1415  
c) 003F1417  
d) 003F1425  

**Answer** c) 

**Description**

After the execution of the instruction, jz labelExitLoop, EIP will be pointing to next instruction whose EIP is 003F1417. It will not jump to LabelExitLoop, as when ECX is 0, jump on zero (jz) will not succeed as 0 – 5 is not 0. Je is same as jz, as jump on zero means that both values are equal, that is je.

---
---


18 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FC84 EIP = 003F1412 ESP = 0033FBA4 EBP = 0033FC84 EFL = 00000202

Relevant memory is the following,

0x0033FB94 7701041d   
0x0033FB98 01e61843  
0x0033FB9C fffffffe  
0x0033FBA0 76fd36fa  
0x0033FBA4 0000004d  
0x0033FBA8 00000023  
0x0033FBAC 0000000c  
0x0033FBB0 00000004  
0x0033FBB4 00000042  
0x0033FBB8 00000000  
0x0033FBBC 00000000  
0x0033FBC0 7efde000  

Disassembly is the following,    

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_18.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz labelExitLoop, if the value of ECX is 1?  

a) 003F1412  
b) 003F1417  
c) 003F1425  
d) None of the above  

**Answer** b) 

**Description**

After the execution of the instruction, jz labelExitLoop, EIP will be pointing to next instruction whose EIP is 003F1417. It will not jump to LabelExitLoop, as when ECX is 1, jump on zero (jz) will not succeed as 1 – 5 is not 0. Je is same as jz, as jump on zero means that both values are equal, that is je.  

---
---


19 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FC84 EIP = 003F1412 ESP = 0033FBA4 EBP = 0033FC84 EFL = 00000202

Relevant memory is the following,

0x0033FB94 7701041d  
0x0033FB98 01e61843  
0x0033FB9C fffffffe  
0x0033FBA0 76fd36fa  
0x0033FBA4 0000004d  
0x0033FBA8 00000023  
0x0033FBAC 0000000c  
0x0033FBB0 00000004  
0x0033FBB4 00000042  
0x0033FBB8 00000000  
0x0033FBBC 00000000  
0x0033FBC0 7efde000  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_19.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz labelExitLoop, if the value of ECX is 2?  

a) 003F1412  
b) 003F1415  
c) 003F1417  
d) 003F1425  

**Answer** c) 

**Description**

After the execution of the instruction, jz labelExitLoop, EIP will be pointing to next instruction whose EIP is 003F1417. It will not jump to LabelExitLoop, as when ECX is 2, jump on zero (jz) will not succeed as 2 – 5 is not 0.   Je is same as jz, as jump on zero means that both values are equal, that is je.  

---
---


20 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FC84 EIP = 003F1412 ESP = 0033FBA4 EBP = 0033FC84 EFL = 00000202

Relevant memory is the following,

0x0033FB94 7701041d  
0x0033FB98 01e61843  
0x0033FB9C fffffffe  
0x0033FBA0 76fd36fa  
0x0033FBA4 0000004d  
0x0033FBA8 00000023  
0x0033FBAC 0000000c  
0x0033FBB0 00000004  
0x0033FBB4 00000042  
0x0033FBB8 00000000  
0x0033FBBC 00000000  
0x0033FBC0 7efde000  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_20.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz labelExitLoop, if the value of ECX is 3?  

a) 003F1412  
b) 003F1425  
c) 003F1415  
d) 003F1417  

**Answer** d) 

**Description**

After the execution of the instruction, jz labelExitLoop, EIP will be pointing to next instruction whose EIP is 003F1417. It will not jump to LabelExitLoop, as when ECX is 3, jump on zero (jz) will not succeed as 3 – 5 is not 0. Je is same as jz, as jump on zero means that both values are equal, that is je.  

---
---


21 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FC84 EIP = 003F1412 ESP = 0033FBA4 EBP = 0033FC84 EFL = 00000202

Relevant memory is the following,

0x0033FB94 7701041d  
0x0033FB98 01e61843  
0x0033FB9C fffffffe  
0x0033FBA0 76fd36fa  
0x0033FBA4 0000004d  
0x0033FBA8 00000023  
0x0033FBAC 0000000c  
0x0033FBB0 00000004  
0x0033FBB4 00000042  
0x0033FBB8 00000000  
0x0033FBBC 00000000  
0x0033FBC0 7efde000  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_21.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz labelExitLoop, if the value of ECX is 4?  

a) 003F1417  
b) 003F1412  
c) 003F1415  
d) 003F1425  

**Answer** a) 

**Description**

After the execution of the instruction, jz labelExitLoop, EIP will be pointing to next instruction whose EIP is 003F1417. It will not jump to LabelExitLoop, as when ECX is 4, jump on zero (jz) will not succeed as 4 – 5 is not 0.  Je is same as jz, as jump on zero means that both values are equal, that is je.  

---
---


22 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
	labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FC84 EIP = 003F1412 ESP = 0033FBA4 EBP = 0033FC84 EFL = 00000202

Relevant memory is the following,

0x0033FB94 7701041d  
0x0033FB98 01e61843  
0x0033FB9C fffffffe  
0x0033FBA0 76fd36fa  
0x0033FBA4 0000004d  
0x0033FBA8 00000023  
0x0033FBAC 0000000c  
0x0033FBB0 00000004  
0x0033FBB4 00000042  
0x0033FBB8 00000000  
0x0033FBBC 00000000  
0x0033FBC0 7efde000  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_22.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz labelExitLoop, if the value of ECX is 5?  

a) 003F1412  
b) 003F1415  
c) 003F1417  
d) 003F1425  

**Answer** d) 

**Description**

After the execution of the instruction, jz labelExitLoop, EIP will be pointing to LabelExitLoop whose EIP is 003F1425. It will jump to LabelExitLoop, as when ECX is 5, jump on zero (jz) will succeed as 5 – 5 is 0. Je is same as jz, as jump on zero means that both values are equal, that is je.  

---
---


23 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

	    mov eax, 0
	    mov ecx, 0

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
	return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_23.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jle labelMoveToEAX in the above program?  

a) 000F141A  
b) 000F141C  
c) 000F141D  
d) 000F141F  

**Answer** d) 

**Description**

Here EAX & ECX is zero as seen from the registers, the instruction, cmp eax, dword ptr[esp + ecx * 4], will boil down to cmp eax, dword ptr[esp + 0 * 4], which is equal to cmp eax, dword ptr[esp]. Now the value inside [esp] is 77 (4D in hex). So basically we are compairing 0 with 77. So jle will succeed, as 0 is less than 77 and it will jump to labelMoveToEAX whose EIP is 000F141F.   

---
---


24 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

	    mov eax, 0
	    mov ecx, 0

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_24.jpg" width="400"/>

What will be the value of EAX after the execution of the instruction, mov eax, dword ptr[esp + ecx * 4]?  

a) 4D (Hex value of 77)  
b) 23 (Hex value of 35)  
c) 0C (Hex value of 12)  
d) 4  

**Answer** a) 

**Description**

Here the instruction mov eax, dword ptr[esp + ecx * 4], will boil down to cmp eax, dword ptr[esp + 0 * 4], because ECX is 0 as seen from the registers, which is equal to cmp eax, dword ptr[esp]. Now the value inside [esp] is 77 (4D in hex). So the value of [esp] will move to EAX and that is 77 which is 4D in Hex.  

---
---


25 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

	    mov eax, 0
	    mov ecx, 0

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa   
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_25.jpg" width="400"/>

What will be the value of ECX after the execution of the instruction, inc ecx?  

a) 00000000  
b) 00000001  
c) CCCCCCCC  
d) None of the above  

**Answer** b) 

**Description**

Inc ecx will increment the value of ECX by 1, so it will become 00000001.

---
---


26 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

	    mov eax, 0
	    mov ecx, 0

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 00000000 EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_26.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jmp labelLoopStart in the above program?  

a) 000F1423  
b) 000F1425  
c) 000F1412  
d) 000F1415  

**Answer** c) 

**Description**

Jmp labelLoopStart is an unconditional jump and it will jump to labelLoopStart whose EIP is 000F1412.  

---
---


27 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000001 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_27.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jle labelMoveToEAX in the above program?  

a) 000F141A  
b) 000F141C  
c) 000F141D  
d) 000F141F  

**Answer** b) 

**Description**

Here EAX is 4D (Hex value of 77) &amp; ECX is 1 as seen from the registers, the instruction, cmp eax, dword ptr[esp + ecx * 4], will boil down to cmp eax, dword ptr[esp + 1 * 4], which is equal to cmp eax, dword ptr[esp + 4]. Now the value inside [esp + 4] is 35 (Hex value is 23). So basically we are compairing 77and 35 and 77 is not less than or equal to 35. So jle will not succeed and it will execute the next instruction, whose EIP is 000F141C.   

---
---


28 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000001 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_28.jpg" width="400"/>

What will be the value of ECX after the execution of the instruction, inc ecx?  

a) 00000000  
b) 00000001  
c) CCCCCCCC  
d) 00000002  

**Answer** d) 

**Description**

Inc ecx will increment the value of ECX by 1, so it will become 00000002.  

---
---


29 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000002 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_29.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jle labelMoveToEAX in the above program?  

a) 000F141A  
b) 000F141C  
c) 000F141D  
d) 000F141F  

**Answer** b) 

**Description**

Here EAX is 4D (77) & ECX is 2 as seen from the registers, the instruction, cmp eax, dword ptr[esp + ecx * 4],will boil down to cmp eax, dword ptr[esp + 2 * 4], which is equal to cmp eax, dword ptr[esp + 8]. Now the value inside [esp + 8] is 12 (Hex value is 0C). So basically we are compairing 77and 12 and 77 is not less than or equal to 12. So jle will not succeed and it will execute the next instruction, whose EIP is 000F141C.

---
---


30 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000002 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  


Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_30.jpg" width="400"/>

What will be the value of ECX after the execution of the instruction, inc ecx?  

a) 00000000  
b) 00000002  
c) CCCCCCCC  
d) 00000003  

**Answer** d) 

**Description**

Inc ecx will increment the value of ECX by 1, so it will become 00000003.  

---
---


31 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000003 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_31.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jle labelMoveToEAX in the above program?   

a) 000F141A  
b) 000F141C  
c) 000F141D  
d) 000F141F  

**Answer** b) 

**Description**

Here EAX is 4D (77) & ECX is 3 as seen from the registers, the instruction, cmp eax, dword ptr[esp + ecx * 4],will boil down to cmp eax, dword ptr[esp + 3 * 4], which is equal to cmp eax, dword ptr[esp + 0Ch]. Now the value inside [esp + 0Ch] is 4. So basically we are compairing 77and 4 and 77 is not less than or equal to 4. So jle will not succeed and it will execute the next instruction, whose EIP is 000F141C. 

---
---


32 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000003 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_32.jpg" width="400"/>

What will be the value of ECX after the execution of the instruction, inc ecx?  

a) 00000000  
b) 00000004  
c) CCCCCCCC  
d) 00000003  

**Answer** b) 

**Description**

Inc ecx will increment the value of ECX by 1, so it will become 00000004.  

---
---


33 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000004 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_33.jpg" width="400"/>
  
What will be the value of EIP after the execution of the instruction, jle labelMoveToEAX in the above program?  

a) 000F141A  
b) 000F141C  
c) 000F141D  
d) 000F141F  

**Answer** b) 

**Description**

Here EAX is 4D (77) &amp; ECX is 4 as seen from the registers, the instruction, cmp eax, dword ptr[esp + ecx * 4],will boil down to cmp eax, dword ptr[esp + 4 * 4], which is equal to cmp eax, dword ptr[esp + 10h] (10 is hex value of 16) Now the value inside [esp + 10h] is 66 (Hex value is 42). So basically we are compairing 77and 66 and 77 is not less than or equal to 66.  So jle will not succeed and it will execute the next instruction, whose EIP is 000F141C.   

---
---


34 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000004 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c  
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_34.jpg" width="400"/>

What will be the value of ECX after the execution of the instruction, inc ecx?  

a) 00000000  
b) 00000004  
c) CCCCCCCC  
d) 00000005  

**Answer** d) 

**Description**

Inc ecx will increment the value of ECX by 1, so it will become 00000005.  

---
---


35 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{
            sub esp, 20

	    mov dword ptr[esp], 77
	    mov dword ptr[esp + 4], 35
	    mov dword ptr[esp + 8], 12
	    mov dword ptr[esp + 0Ch], 4
	    mov dword ptr[esp + 10h], 66

        labelLoopStart:
	    cmp ecx, 5
	    jz labelExitLoop

	    cmp eax, dword ptr[esp + ecx * 4]
	    jle labelMoveToEAX

	    inc ecx
	    jmp labelLoopStart

        labelMoveToEax :
	    mov eax, dword ptr[esp + ecx * 4]
	    inc ecx
	    jmp labelLoopStart

        labelExitLoop :
	    add esp, 20
	}
    return 0;
}
```

Register values are the following,

EAX = 0000004D EBX = 7EFDE000 ECX = 00000005 EDX = 00000001 ESI = 00000000 EDI = 0038FD2C EIP = 000F1412 ESP = 0038FC4C EBP = 0038FD2C EFL = 00000212

Relevant memory is the following,

0x0038FC40 003e081c  
0x0038FC44 fffffffe  
0x0038FC48 770a36fa  
0x0038FC4C 0000004d  
0x0038FC50 00000023  
0x0038FC54 0000000c   
0x0038FC58 00000004  
0x0038FC5C 00000042  
0x0038FC60 00000000  
0x0038FC64 00000000  
0x0038FC68 7efde000  
0x0038FC6C cccccccc  
0x0038FC70 cccccccc  
0x0038FC74 cccccccc    

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_54_FindingTheBiggestNumberProgramQuiz/Images/Q_54_35.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz labelExitLoop in the above program?  

a) 000F1415  
b) 000F1417  
c) 000F1425  
d) 000F1428  

**Answer** c) 

**Description**

After the execution of the instruction jz labelExitLoop it will jump to labelExitLoop because the result of previous operation is zero. ECX is 5 as seen in the register values and we are compairing 5 with 5. It is equal to zero. So EIP will be pointing to labelExitLoop, whose EIP is 000F1425, which is evident from disassembly.      

---
---








