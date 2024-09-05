---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, 3
        add eax, 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0034FCE4 EIP = 00D513DE ESP = 0034FC18 EBP = 0034FCE4 EFL = 00000204

Relevant memory is the following,

0x0034FC18 00 00 00 00  
0x0034FC1C 00 00 00 00  
0x0034FC20 00 e0 fd 7e  
0x0034FC24 cc cc cc cc  
0x0034FC28 cc cc cc cc  
0x0034FC2C cc cc cc cc  
0x0034FC30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly1.jpg" width="400"/>  

Which register/s will change after the execution of the first instruction, mov eax, 3 in the above program?  

a) EAX  
b) ESP  
c) EIP  
d) Both a & c  

**Answer** d)  

**Description**

In the first instruction of the program we are moving a value to EAX register. So it will change. EIP will change with every instruction.  

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, 3
        add eax, 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0034FCE4 EIP = 00D513DE ESP = 0034FC18 EBP = 0034FCE4 EFL = 00000204

Relevant memory is the following,

0x0034FC18 00 00 00 00  
0x0034FC1C 00 00 00 00  
0x0034FC20 00 e0 fd 7e  
0x0034FC24 cc cc cc cc   
0x0034FC28 cc cc cc cc  
0x0034FC2C cc cc cc cc  
0x0034FC30 cc cc cc cc   

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly2.jpg" width="400"/>    

What will be the value of EAX after the instruction, mov eax, 3 in the above program?  

a) CCCCCCCC  
b) 00000006  
c) 00000003  
d) None of the above  

**Answer** c)  

**Description**

In the first instruction of the program we are moving a value 3 to EAX register. So it will change and become 00000003.  

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, 3
        add eax, 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0034FCE4 EIP = 00D513DE ESP = 0034FC18 EBP = 0034FCE4 EFL = 00000204

Relevant memory is the following,

0x0034FC18 00 00 00 00  
0x0034FC1C 00 00 00 00  
0x0034FC20 00 e0 fd 7e  
0x0034FC24 cc cc cc cc  
0x0034FC28 cc cc cc cc  
0x0034FC2C cc cc cc cc  
0x0034FC30 cc cc cc cc   

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly3.jpg" width="400"/>  

What will be the value of EIP after the instruction, mov eax, 3 in the above program?  

a) 00D513DE  
b) 00D513E3  
c) 00000003  
d) 00000006  

**Answer** b)  

**Description**

After the first instruction, mov eax, 3 the EIP will be pointing to the next instruction, that is 00D513E3, which is evident from the disassembly.  

---
---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, 3
        add eax, 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0034FCE4 EIP = 00D513DE ESP = 0034FC18 EBP = 0034FCE4 EFL = 00000204

Relevant memory is the following,

0x0034FC18 00 00 00 00  
0x0034FC1C 00 00 00 00  
0x0034FC20 00 e0 fd 7e  
0x0034FC24 cc cc cc cc  
0x0034FC28 cc cc cc cc  
0x0034FC2C cc cc cc cc  
0x0034FC30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly4.jpg" width="400"/>  

Which register/s will change after the execution of the second instruction, add eax, 6 in the above program?  

a) EAX  
b) ESP  
c) EIP  
d) Both a & c  

**Answer** d)  

**Description**

In the second instruction, add eax, 6 we are adding a value 6 to the eax register. So it will change.EIP will be then pointing to the next instruction, so it will also change.  

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, 3
        add eax, 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0034FCE4 EIP = 00D513DE ESP = 0034FC18 EBP = 0034FCE4 EFL = 00000204

Relevant memory is the following,

0x0034FC18 00 00 00 00  
0x0034FC1C 00 00 00 00  
0x0034FC20 00 e0 fd 7e  
0x0034FC24 cc cc cc cc  
0x0034FC28 cc cc cc cc  
0x0034FC2C cc cc cc cc  
0x0034FC30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly5.jpg" width="400"/>  

What will be the value of EAX after the instruction, add eax, 6 in the above program?  

a) CCCCCCCC  
b) 00000006  
c) 00000003  
d) 00000009  

**Answer** d)  

**Description**

In the second instruction, add eax, 6 we are adding a value 6 to the eax register. So it will become 00000009 ( 3 + 6).  

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        mov eax, 3
        add eax, 6
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0034FCE4 EIP = 00D513DE ESP = 0034FC18 EBP = 0034FCE4 EFL = 00000204

Relevant memory is the following,

0x0034FC18 00 00 00 00  
0x0034FC1C 00 00 00 00  
0x0034FC20 00 e0 fd 7e  
0x0034FC24 cc cc cc cc  
0x0034FC28 cc cc cc cc  
0x0034FC2C cc cc cc cc  
0x0034FC30 cc cc cc cc  

Disassembly is the following,   
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly6.jpg" width="400"/>  

What will be the value of EIP after the instruction, add eax, 6 in the above program?  

a) 00D513DE  
b) 00D513E3  
c) 00D513E6  
d) 00000009  

**Answer** c)  

**Description**

After the second instruction, add eax, 6  the EIP will be pointing to the next instruction, that is 00D513E6, which is evident from the disassembly.  \

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{	
	    mov eax, 6
	    sub eax, 3
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003EFDE4 EIP = 00BC13DE ESP = 003EFD18 EBP = 003EFDE4 EFL = 00000204

Relevant memory is the following,

0x003EFD18 00 00 00 00  
0x003EFD1C 00 00 00 00  
0x003EFD20 00 e0 fd 7e  
0x003EFD24 cc cc cc cc    
0x003EFD28 cc cc cc cc  
0x003EFD2C cc cc cc cc  
0x003EFD30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly7.jpg" width="400"/>  

Which register/s will change after the execution of the first instruction, mov eax, 6 in the above program?  

a) EAX  
b) ESP  
c) EIP  
d) Both a & c  

**Answer** d)  

**Description**

In the first instruction of the program we are moving a value to EAX register. So it will change. EIP will change with every instruction.  

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{	
	    mov eax, 6
	    sub eax, 3
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003EFDE4 EIP = 00BC13DE ESP = 003EFD18 EBP = 003EFDE4 EFL = 00000204

Relevant memory is the following,

0x003EFD18 00 00 00 00  
0x003EFD1C 00 00 00 00  
0x003EFD20 00 e0 fd 7e  
0x003EFD24 cc cc cc cc  
0x003EFD28 cc cc cc cc  
0x003EFD2C cc cc cc cc  
0x003EFD30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly8.jpg" width="400"/>  

What will be the value of EAX after the instruction, mov eax, 6 in the above program?  

a) CCCCCCCC  
b) 00000006  
c) 00000003  
d) None of the above  

**Answer** b)  

**Description**

In the first instruction of the program we are moving a value 6 to EAX register. So it will change and become 00000006.  

---
---


9 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{	
	    mov eax, 6
	    sub eax, 3
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003EFDE4 EIP = 00BC13DE ESP = 003EFD18 EBP = 003EFDE4 EFL = 00000204

Relevant memory is the following,

0x003EFD18 00 00 00 00  
0x003EFD1C 00 00 00 00  
0x003EFD20 00 e0 fd 7e  
0x003EFD24 cc cc cc cc  
0x003EFD28 cc cc cc cc  
0x003EFD2C cc cc cc cc  
0x003EFD30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly9.jpg" width="400"/>  

What will be the value of EIP after the instruction, mov eax, 6 in the above program?  

a) 00BC13DE  
b) 00BC13E3  
c) 00BC13E6  
d) 00000006  

**Answer** b)  

**Description**

After the first instruction, mov eax, 6 the EIP will be pointing to the next instruction, that is, 00BC13E3, which is evident from the disassembly.  

---
---


10 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{	
	    mov eax, 6
	    sub eax, 3
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003EFDE4 EIP = 00BC13DE ESP = 003EFD18 EBP = 003EFDE4 EFL = 00000204

Relevant memory is the following,

0x003EFD18 00 00 00 00  
0x003EFD1C 00 00 00 00  
0x003EFD20 00 e0 fd 7e  
0x003EFD24 cc cc cc cc  
0x003EFD28 cc cc cc cc  
0x003EFD2C cc cc cc cc  
0x003EFD30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly10.jpg" width="400"/>  

Which register/s will change after the execution of the second instruction, sub eax, 3 in the above program?  

a) EAX  
b) ESP  
c) EIP  
d) Both a & c  

**Answer** d)  

**Description**

In the second instruction, sub eax, 3  we are subtracting a value 3 from the eax register. So it will change.EIP will be then pointing to the next instruction, so it will also change.  

---
---


11 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{	
	    mov eax, 6
	    sub eax, 3
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003EFDE4 EIP = 00BC13DE ESP = 003EFD18 EBP = 003EFDE4 EFL = 00000204

Relevant memory is the following,

0x003EFD18 00 00 00 00  
0x003EFD1C 00 00 00 00  
0x003EFD20 00 e0 fd 7e  
0x003EFD24 cc cc cc cc  
0x003EFD28 cc cc cc cc  
0x003EFD2C cc cc cc cc  
0x003EFD30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly11.jpg" width="400"/>  

What will be the value of EAX after the second instruction, sub eax, 3 in the above program?  

a) CCCCCCCC  
b) 00000006  
c) 00000003  
d) 00000009  

**Answer** c)  

**Description**

In the second instruction, sub eax, 3  we are subtracting a value 3 from the eax register. So it will become 00000003 ( 6 – 3).  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
	{	
	    mov eax, 6
	    sub eax, 3
	}
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003EFDE4 EIP = 00BC13DE ESP = 003EFD18 EBP = 003EFDE4 EFL = 00000204

Relevant memory is the following,

0x003EFD18 00 00 00 00  
0x003EFD1C 00 00 00 00  
0x003EFD20 00 e0 fd 7e  
0x003EFD24 cc cc cc cc  
0x003EFD28 cc cc cc cc  
0x003EFD2C cc cc cc cc  
0x003EFD30 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly12.jpg" width="400"/>  

What will be the value of EIP after the instruction, sub eax, 3 in the above program?  

a) 00BC13DE  
b) 00BC13E3  
c) 00BC13E6  
d) 00000003  

**Answer** c)  

**Description**

After the second instruction, sub eax, 3 the EIP will be pointing to the next instruction, that is 00BC13E6, which is evident from the disassembly.  

---
---


13 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x12
        mov eax, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FE58 EIP = 012C13DE ESP = 0033FD8C EBP = 0033FE58 EFL = 00000200

Relevant memory is the following,

0x0033FD80 b0 7e 64 00  
0x0033FD84 00 00 00 00  
0x0033FD88 00 00 00 00  
0x0033FD8C 00 00 00 00  
0x0033FD90 00 00 00 00   
0x0033FD94 00 e0 fd 7e  
0x0033FD98 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly13.jpg" width="400"/>  

What will change after the execution of the instruction, push 0x12 in the above program?  

a) ESP  
b) EIP  
c) Value of the memory location 0x0033FD88  
d) All of the above  

**Answer** d)  

**Description**

push 0x12 is effectively two instructions, that is sub esp, 4 & mov dword ptr[esp], 0x12. So ESP will change. EIP will change and will be pointing to next instruction. The value 0x12 will get moved to memory location 0x0033FD88, so it also will change.  

---
---


14 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x12
        mov eax, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FE58 EIP = 012C13DE ESP = 0033FD8C EBP = 0033FE58 EFL = 00000200

Relevant memory is the following,

0x0033FD80 b0 7e 64 00  
0x0033FD84 00 00 00 00  
0x0033FD88 00 00 00 00  
0x0033FD8C 00 00 00 00  
0x0033FD90 00 00 00 00  
0x0033FD94 00 e0 fd 7e  
0x0033FD98 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly14.jpg" width="400"/>   

What will be the value of ESP after the execution of the instruction, push 0x12 in the above program?  

a) 0033FD8C  
b) 0033FD88  
c) 0033FD90  
d) 0033FD84  

**Answer** b)  

**Description**

push 0x12 will allocate stack memory (sub esp, 4) and write 0x12 to that memory (mov dword ptr[esp], 0x12). So ESP will get decrement by 4 bytes and will become 0033FD88.   

---
---


15 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x12
        mov eax, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FE58 EIP = 012C13DE ESP = 0033FD8C EBP = 0033FE58 EFL = 00000200

Relevant memory is the following,

0x0033FD80 b0 7e 64 00  
0x0033FD84 00 00 00 00  
0x0033FD88 00 00 00 00  
0x0033FD8C 00 00 00 00  
0x0033FD90 00 00 00 00  
0x0033FD94 00 e0 fd 7e  
0x0033FD98 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly15.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, push 0x12 in the above program?  

a) 012C13E0  
b) 012C13E3  
c) 012C13DE  
d) 012C13E5  

**Answer** a)  

**Description**

After the execution of the first instruction push 0x12, EIP will be pointing to the next instruction, which is 012C13E0 and is evident from the disassembly.  

---
---


16 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x12
        mov eax, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FE58 EIP = 012C13DE ESP = 0033FD8C EBP = 0033FE58 EFL = 00000200

Relevant memory is the following,

0x0033FD80 b0 7e 64 00  
0x0033FD84 00 00 00 00  
0x0033FD88 00 00 00 00  
0x0033FD8C 00 00 00 00  
0x0033FD90 00 00 00 00  
0x0033FD94 00 e0 fd 7e  
0x0033FD98 cc cc cc cc   

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly16.jpg" width="400"/>  

What will be the value of the memory location 0x0033FD88 after the execution of the instruction, push 0x12 in the above program?  

a) 00000012  
b) 0033FD88  
c) 00000000  
d) None of the above  

**Answer** a)  

**Description**

push 0x12 will allocate stack memory and push (write) the value 0x12 to the value of that memory location, so it will become 00000012.

---
---


17 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x12
        mov eax, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FE58 EIP = 012C13DE ESP = 0033FD8C EBP = 0033FE58 EFL = 00000200

Relevant memory is the following,

0x0033FD80 b0 7e 64 00  
0x0033FD84 00 00 00 00  
0x0033FD88 00 00 00 00  
0x0033FD8C 00 00 00 00  
0x0033FD90 00 00 00 00  
0x0033FD94 00 e0 fd 7e   
0x0033FD98 cc cc cc cc   

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly17.jpg" width="400"/>  

What will be the value of EAX after the execution of the instruction, mov eax, dword ptr[esp] in the above program?  

a) 00000000  
b) CCCCCCCC  
c) 00000012  
d) None of the above  

**Answer** c)  

**Description**  

After the instruction, mov eax, dword ptr[esp], the value of the memory location [esp] will get moved to EAX. So it will become 00000012.

---
---


18 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x12
        mov eax, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FE58 EIP = 012C13DE ESP = 0033FD8C EBP = 0033FE58 EFL = 00000200

Relevant memory is the following,

0x0033FD80 b0 7e 64 00  
0x0033FD84 00 00 00 00  
0x0033FD88 00 00 00 00  
0x0033FD8C 00 00 00 00  
0x0033FD90 00 00 00 00  
0x0033FD94 00 e0 fd 7e    
0x0033FD98 cc cc cc cc    

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly18.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, mov eax, dword ptr[esp] in the above program?  

a) 012C13E0  
b) 012C13E3  
c) 012C13DE  
d) 012C13E5  

**Answer** b)  

**Description**

After the execution of the second instruction, mov eax, dword ptr[esp], EIP will be pointing to the next instruction, which is 012C13E3 and is evident from the disassembly.  

---
---


19 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x12
        mov eax, dword ptr[esp]
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033FE58 EIP = 012C13DE ESP = 0033FD8C EBP = 0033FE58 EFL = 00000200

Relevant memory is the following,

0x0033FD80 b0 7e 64 00  
0x0033FD84 00 00 00 00  
0x0033FD88 00 00 00 00  
0x0033FD8C 00 00 00 00  
0x0033FD90 00 00 00 00  
0x0033FD94 00 e0 fd 7e  
0x0033FD98 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly19.jpg" width="400"/>  

What will be the fate of the above program?  

a) Program will crash  
b) Program will not crash  
c) Nothing will happen  
d) None of the above  

**Answer** a)  

**Description**

The above program will crash, because we are not deallocating the stack memory that we are allocating at the beginning.  

---
---


20 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x33
        mov ecx, dword ptr[esp]
        add esp, 4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040F8B4 EIP = 00A113DE ESP = 0040F7E8 EBP = 0040F8B4 EFL = 00000200

Relevant memory is the following,

0x0040F7DC b0 7e 85 00  
0x0040F7E0 00 00 00 00  
0x0040F7E4 00 00 00 00  
0x0040F7E8 00 00 00 00  
0x0040F7EC 00 00 00 00  
0x0040F7F0 00 e0 fd 7e  
0x0040F7F4 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly20.jpg" width="400"/>  

What will change after the execution of the instruction, push 0x33 in the above program?  

a) ESP  
b) EIP  
c) Memory location 0x0040F7E4  
d) All of the above  

**Answer** d)  

**Description**

push 0x33 is effectively two instructions, that is sub esp, 4 & mov dword ptr[esp], 0x33. So ESP will change. EIP will change and will be pointing to next instruction. The value 0x33 will get moved to the value of the memory location 0x0040F7E4, so it also will change.  

---
---


21 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x33
        mov ecx, dword ptr[esp]
        add esp, 4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040F8B4 EIP = 00A113DE ESP = 0040F7E8 EBP = 0040F8B4 EFL = 00000200

Relevant memory is the following,

0x0040F7DC b0 7e 85 00  
0x0040F7E0 00 00 00 00  
0x0040F7E4 00 00 00 00  
0x0040F7E8 00 00 00 00  
0x0040F7EC 00 00 00 00  
0x0040F7F0 00 e0 fd 7e  
0x0040F7F4 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly21.jpg" width="400"/>  

What will be the value of ESP after the execution of the instruction, push 0x33 in the above program?  

a) 0040F7E8  
b) 0040F7E4  
c) 0040F7EC  
d) 0040F7E0  

**Answer** b)  

**Description**

push 0x33 will allocate stack memory (sub esp, 4) and write 0x33 to that memory (mov dword ptr[esp], 0x33). So ESP will get decrement by 4 bytes and will become 0040F7E4.   

---
---


22 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x33
        mov ecx, dword ptr[esp]
        add esp, 4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040F8B4 EIP = 00A113DE ESP = 0040F7E8 EBP = 0040F8B4 EFL = 00000200

Relevant memory is the following,

0x0040F7DC b0 7e 85 00  
0x0040F7E0 00 00 00 00  
0x0040F7E4 00 00 00 00  
0x0040F7E8 00 00 00 00  
0x0040F7EC 00 00 00 00  
0x0040F7F0 00 e0 fd 7e  
0x0040F7F4 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly22.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, push 0x33 in the above program?  

a) 00A113E0  
b) 00A113DE  
c) 00A113DC  
d) 00A113E3  

**Answer** a)  

**Description**

After the execution of the first instruction push 0x33, EIP will be pointing to the next instruction, which is 00A113E0 and is evident from the disassembly.  

---
---


23 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x33
        mov ecx, dword ptr[esp]
        add esp, 4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040F8B4 EIP = 00A113DE ESP = 0040F7E8 EBP = 0040F8B4 EFL = 00000200

Relevant memory is the following,

0x0040F7DC b0 7e 85 00  
0x0040F7E0 00 00 00 00  
0x0040F7E4 00 00 00 00  
0x0040F7E8 00 00 00 00  
0x0040F7EC 00 00 00 00  
0x0040F7F0 00 e0 fd 7e  
0x0040F7F4 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly23.jpg" width="400"/>  

What will be the value of the memory location 0x0040F7E4, after the execution of the instruction, push 0x33 in the above program?  

a) 00000033  
b) 0033FD88  
c) 00000000  
d) None of the above  

**Answer** a)  

**Description**

push 0x33 will allocate stack memory and push (write) the value 0x33 to the value of that memory location, so it will become 00000033.  

---
---


24 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x33
        mov ecx, dword ptr[esp]
        add esp, 4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040F8B4 EIP = 00A113DE ESP = 0040F7E8 EBP = 0040F8B4 EFL = 00000200

Relevant memory is the following,

0x0040F7DC b0 7e 85 00  
0x0040F7E0 00 00 00 00  
0x0040F7E4 00 00 00 00  
0x0040F7E8 00 00 00 00  
0x0040F7EC 00 00 00 00  
0x0040F7F0 00 e0 fd 7e  
0x0040F7F4 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly24.jpg" width="400"/>  

What will be the value of ECX after the execution of the instruction, mov ecx, dword ptr[esp] in the above program?  

a) 00000000  
b) CCCCCCCC  
c) 00000033  
d) None of the above  

**Answer** c)  

**Description**

After the instruction, mov ecx, dword ptr[esp], the value of the memory location [esp] will get moved to ECX. So it will become 00000033.  

---
---


25 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x33
        mov ecx, dword ptr[esp]
        add esp, 4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040F8B4 EIP = 00A113DE ESP = 0040F7E8 EBP = 0040F8B4 EFL = 00000200

Relevant memory is the following,

0x0040F7DC b0 7e 85 00  
0x0040F7E0 00 00 00 00  
0x0040F7E4 00 00 00 00  
0x0040F7E8 00 00 00 00   
0x0040F7EC 00 00 00 00  
0x0040F7F0 00 e0 fd 7e  
0x0040F7F4 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly25.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, mov ecx, dword ptr[esp] in the above program?  

a) 00A113E0  
b) 00A113DE  
c) 00A113DC  
d) 00A113E3  

**Answer** d)  

**Description**

After the execution of the second instruction, mov ecx, dword ptr[esp], EIP will be pointing to the next instruction, which is 00A113E3 and is evident from the disassembly.  

---
---


26 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x33
        mov ecx, dword ptr[esp]
        add esp, 4
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0040F8B4 EIP = 00A113DE ESP = 0040F7E8 EBP = 0040F8B4 EFL = 00000200

Relevant memory is the following,

0x0040F7DC b0 7e 85 00  
0x0040F7E0 00 00 00 00  
0x0040F7E4 00 00 00 00  
0x0040F7E8 00 00 00 00  
0x0040F7EC 00 00 00 00  
0x0040F7F0 00 e0 fd 7e  
0x0040F7F4 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_50_AssemblyMultipleInstructionPractice_mov_add_sub_push/Images/Q_50_Disassembly26.jpg" width="400"/>  

What will be the fate of the above program?  

a) Program will crash  
b) Program will not crash  
c) Nothing will happen  
d) None of the above  

**Answer** b)  

**Description**

The above program will not crash, because we are deallocating the stack memory (add esp, 4) that we are allocating at the beginning and ESP is same after the function/set of instructions.

---
---









