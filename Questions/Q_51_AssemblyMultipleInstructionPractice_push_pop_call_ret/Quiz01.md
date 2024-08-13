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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly3.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, push 0x5 in the above program?  

a) 008313DE  
b) 008313E0  
c) 008313E4  
d) 008313DC  

**Answer** b) 

**Description**

After the execution of the first instruction push 0x5, EIP will be pointing to the next instruction, which is 008313E0 and is evident from the disassembly.  

---
---


4 : We have the below program,  

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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly4.jpg" width="400"/>  

What will be the value of the memory location 0x0038FAD0, after the execution of the instruction, push 0x5 in the above program?  

a) 00000005  
b) 0038FAD0  
c) 00000000  
d) None of the above  

**Answer** a) 

**Description**

push 0x5 will allocate stack memory and push (write) the value 0x5 to the value of that memory location, so it will become 00000005.  

---
---


5 : We have the below program,

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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly5.jpg" width="400"/>  

What will be the value of the memory location [esp] after the execution of the second instruction, add dword ptr[esp], 0x4 in the above program?  

a) 00000004  
b) 00000005  
c) 00000009  
d) 0038FAD0  

**Answer** a) 

**Description**

Second instruction is adding 0x4 to the value of the memory location [esp], so it will become 00000009. ( 5 + 4)  

---
---


6 : We have the below program,  

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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly6.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, add dword ptr[esp], 0x4 in the above program?  

a) 008313DE  
b) 008313E0  
c) 008313E4  
d) 008313E5  

**Answer** c) 

**Description**

After the execution of the second instruction, add dword ptr[esp], 0x4 EIP will be pointing to the next instruction, which is 008313E4 and is evident from the disassembly.  

---
---


7 : We have the below program,  

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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly7.jpg" width="400"/>  

What will be the value of ESP after the execution of the instruction, add dword ptr[esp], 0x4 in the above program?  

a) 0038FAD4  
b) 0038FAD0  
c) 0038FACC  
d) 0038FAD8  

**Answer** b) 

**Description**

ESP will be same as that of the above instruction (0038FAD0) because we are not allocating or deallocating stack memory in this instruction.  

---
---


8 : We have the below program,  

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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly8.jpg" width="400"/>  

What will be the value of ESP after the execution of the third instruction, pop eax, in the above program?  

a) 0038FAD4  
b) 0038FAD0  
c) 0038FACC  
d) 0038FAD8  

**Answer** a) 

**Description**

With the instruction pop eax we are reading the memory to eax (mov eax, dword ptr[esp]) and also we are deallocating the stack memory by add esp, 4. So ESP will return to the value which it was at the beginning which is 0038FAD4.   

---
---


9 : We have the below program,  

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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly9.jpg" width="400"/>  

What will be the value of EIP after the execution of the instruction, pop eax in the above program?  

a) 008313DE  
b) 008313E0  
c) 008313E4  
d) 008313E5  

**Answer** d) 

**Description**

After the execution of the third instruction, pop eax, EIP will be pointing to the next instruction, which is 008313E5 and is evident from the disassembly.  

---
---


10 : We have the below program,  

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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly10.jpg" width="400"/>  

What will be the value of EAX after the execution of the instruction, pop eax in the above program?  

a) 00000009  
b) CCCCCCCC  
c) 00000000  
d) 00000005  

**Answer** a) 

**Description**

By the instruction, pop eax, we are moving the value of the memory location [esp] to EAX. So it will become 00000009.   

---
---


11 : We have the below program,  

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
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly11.jpg" width="400"/>  

What will be the fate of the above program?  

a) Program will crash  
b) Program will not crash  
c) Nothing will happen  
d) None of the above  

**Answer** b) 

**Description**

The above program will not crash, because we are deallocating the stack memory (add esp, 4) by the instruction pop eax, that we are allocating by the push instruction at the beginning.  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
            mov eax, 3
            mov ecx, 2
            call label1
            add eax, 1
         
        label1 :
            imul eax, ecx
            ret
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0015FC48 EIP = 00A713DE ESP = 0015FB7C EBP = 0015FC48 EFL = 00000204

Relevant memory is the following,

0x0015FB70 b0 7e 25 00   
0x0015FB74 00 00 00 00  
0x0015FB78 00 00 00 00  
0x0015FB7C 00 00 00 00  
0x0015FB80 00 00 00 00  
0x0015FB84 00 e0 fd 7e  
0x0015FB88 cc cc cc cc   

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly12.jpg" width="400"/>  

What will change after the first instruction, mov eax, 3?   

a) EAX  
b) EIP  
c) ESP  
d) Both a & b  

**Answer** d) 

**Description**

In the first instruction, mov eax, 3 we are moving a value 3 to eax register. So it will change. EIP will change and will be pointing to next instruction. ESP does not change because we are not touching stack memory.  

---
---


13 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
            mov eax, 3
            mov ecx, 2
            call label1
            add eax, 1
         
        label1 :
            imul eax, ecx
            ret
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0015FC48 EIP = 00A713DE ESP = 0015FB7C EBP = 0015FC48 EFL = 00000204

Relevant memory is the following,

0x0015FB70 b0 7e 25 00  
0x0015FB74 00 00 00 00  
0x0015FB78 00 00 00 00  
0x0015FB7C 00 00 00 00  
0x0015FB80 00 00 00 00  
0x0015FB84 00 e0 fd 7e  
0x0015FB88 cc cc cc cc  

Disassembly is the following,  
<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_51_AssemblyMultipleInstructionPractice_push_pop_call_ret/Images/Q_51_Disassembly13.jpg" width="400"/>  

What will be the value of EAX after the first instruction, mov eax, 3?  

a) CCCCCCCC  
b) 00000000  
c) 00000003  
d) None of the above  

**Answer** c) 

**Description**

In the first instruction, mov eax, 3 we are moving a value 3 to eax register. So it will change and become 00000003.  

---
---


14 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {	
            mov eax, 3
            mov ecx, 2
            call label1
            add eax, 1
         
        label1 :
            imul eax, ecx
            ret
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0015FC48 EIP = 00A713DE ESP = 0015FB7C EBP = 0015FC48 EFL = 00000204

Relevant memory is the following,

0x0015FB70 b0 7e 25 00  
0x0015FB74 00 00 00 00  
0x0015FB78 00 00 00 00  
0x0015FB7C 00 00 00 00   
0x0015FB80 00 00 00 00  
0x0015FB84 00 e0 fd 7e  
0x0015FB88 cc cc cc cc  

Disassembly is the following,  
<img src="" width="400"/>

What will be the value of EIP after the first instruction, mov eax, 3?





