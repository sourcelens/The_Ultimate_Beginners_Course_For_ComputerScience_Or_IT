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
<img src="" width="400"/>

What will change after the execution of the instruction, push 0x12 in the above program?



