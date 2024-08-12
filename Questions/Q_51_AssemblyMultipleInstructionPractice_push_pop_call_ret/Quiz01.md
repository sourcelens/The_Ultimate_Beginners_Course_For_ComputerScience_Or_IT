---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x5
        add dword ptr[esp], 0x4
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FBA0 EIP = 008313DE ESP = 0038FAD4 EBP = 0038FBA0 EFL = 00000200

Relevant memory is the following,

0x0038FAC8 b0 7e 3f 00  
0x0038FACC 00 00 00 00  
0x0038FAD0 00 00 00 00  
0x0038FAD4 00 00 00 00  
0x0038FAD8 00 00 00 00  
0x0038FADC 00 e0 fd 7e  
0x0038FAE0 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly1.jpg" width="400"/>  

What will change after the execution of the instruction, push 0x5 in the above program?  

a) ESP  
b) EIP  
c) Value of the memory location 0x0038FAD0  
d) All of the above  

**Answer** d) 

**Description** 

push 0x5 is effectively two instructions, that is sub esp, 4 &amp; mov dword ptr[esp], 0x5. So ESP will change. EIP will change and will be pointing to next instruction. The value 0x5 will get moved to the value of the memory location 0x0038FAD0, so it also will change.  

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x5
        add dword ptr[esp], 0x4
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FBA0 EIP = 008313DE ESP = 0038FAD4 EBP = 0038FBA0 EFL = 00000200

Relevant memory is the following,

0x0038FAC8 b0 7e 3f 00  
0x0038FACC 00 00 00 00  
0x0038FAD0 00 00 00 00  
0x0038FAD4 00 00 00 00  
0x0038FAD8 00 00 00 00  
0x0038FADC 00 e0 fd 7e  
0x0038FAE0 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly2.jpg" width="400"/>  

What will be the value of ESP after the execution of the instruction, push 0x5 in the above program?  

a) 0038FAD4  
b) 0038FAD0  
c) 0038FACC  
d) 0038FAD8  

**Answer** b) 

**Description**

push 0x5 will allocate stack memory (sub esp, 4) and write 0x5 to that memory (mov dword ptr[esp], 0x5). So ESP will get decremented by 4 bytes and will become 0038FAD0.   

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
        push 0x5
        add dword ptr[esp], 0x4
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0038FBA0 EIP = 008313DE ESP = 0038FAD4 EBP = 0038FBA0 EFL = 00000200

Relevant memory is the following,

0x0038FAC8 b0 7e 3f 00  
0x0038FACC 00 00 00 00  
0x0038FAD0 00 00 00 00  
0x0038FAD4 00 00 00 00  
0x0038FAD8 00 00 00 00  
0x0038FADC 00 e0 fd 7e  
0x0038FAE0 cc cc cc cc  

Disassembly is the following,  
<img src="" width="400"/>

What will be the value of EIP after the execution of the instruction, push 0x5 in the above program?
