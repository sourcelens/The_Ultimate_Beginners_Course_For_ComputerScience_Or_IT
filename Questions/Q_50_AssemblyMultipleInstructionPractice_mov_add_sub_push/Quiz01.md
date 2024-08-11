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


4 : 


