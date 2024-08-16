---
---


1 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {
        mov esi, 1
        cmp edx, esi
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0042FE04 EIP = 011B13E5 ESP = 0042FD2C EBP = 0042FE04 EFL = 00000210

Relevant memory is the following,

0x0042FD20 fa 36 97 77   
0x0042FD24 f2 32 97 77  
0x0042FD28 a8 7e 57 00  
0x0042FD2C 00 00 00 00  
0x0042FD30 00 00 00 00  
0x0042FD34 00 e0 fd 7e  
0x0042FD38 cc cc cc cc  
0x0042FD3C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_1.jpg" width="400"/>

What will be the value of ESI after the execution of the instruction mov esi, 1?  

a) CCCCCCCC  
b) 00000000  
c) 00000001  
d) None of the above  

**Answer** c) 

**Description**  

By the instruction mov esi, 1 we are moving the value 1 to ESI, so it will become 00000001.  

---
---


2 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {
        mov esi, 1
        cmp edx, esi
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0042FE04 EIP = 011B13E5 ESP = 0042FD2C EBP = 0042FE04 EFL = 00000210

Relevant memory is the following,

0x0042FD20 fa 36 97 77  
0x0042FD24 f2 32 97 77  
0x0042FD28 a8 7e 57 00  
0x0042FD2C 00 00 00 00  
0x0042FD30 00 00 00 00  
0x0042FD34 00 e0 fd 7e  
0x0042FD38 cc cc cc cc  
0x0042FD3C cc cc cc cc   

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_2.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov esi, 1?  

a) 011B13DE  
b) 011B13E5  
c) 011B13EA  
d) 011B13EC  

**Answer** c) 

**Description**

After the instruction mov esi, 1 the EIP will be pointing to next instruction, which is 011B13EA  and it is evident from the disassembly.  

---
---


3 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {
        mov esi, 1
        cmp edx, esi
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0042FE04 EIP = 011B13E5 ESP = 0042FD2C EBP = 0042FE04 EFL = 00000210

Relevant memory is the following,

0x0042FD20 fa 36 97 77  
0x0042FD24 f2 32 97 77  
0x0042FD28 a8 7e 57 00  
0x0042FD2C 00 00 00 00  
0x0042FD30 00 00 00 00  
0x0042FD34 00 e0 fd 7e  
0x0042FD38 cc cc cc cc  
0x0042FD3C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_3.jpg" width="400"/>

Which Flag/s will get set after the instruction cmp edx, esi in the above program?  

a) Sign flag  
b) Carry flag  
c) Zero flag  
d) Both a & b  

**Answer** c) 

**Description**

cmp edx, esi is subtracting esi from edx, so 1 – 1, which is 0. So the Zero flag will become 1.   

---


4 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {
        mov esi, 1
        cmp edx, esi
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0042FE04 EIP = 011B13E5 ESP = 0042FD2C EBP = 0042FE04 EFL = 00000210

Relevant memory is the following,

0x0042FD20 fa 36 97 77  
0x0042FD24 f2 32 97 77  
0x0042FD28 a8 7e 57 00  
0x0042FD2C 00 00 00 00  
0x0042FD30 00 00 00 00  
0x0042FD34 00 e0 fd 7e  
0x0042FD38 cc cc cc cc  
0x0042FD3C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q-53_4.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, cmp edx, esi in the above program?  

a) 011B13DE  
b) 011B13E5  
c) 011B13EA  
d) 011B13EC  

**Answer** d) 

**Description**

After the instruction, cmp edx, esi the EIP will be pointing to next instruction which is 011B13EC  and it is evident from the disassembly. Je (jump equal to) shown in the disassembly is same as jz in the program, as jump on zero means both values are equal.  

---
---


5 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {
        mov esi, 1
        cmp edx, esi
        jz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0042FE04 EIP = 011B13E5 ESP = 0042FD2C EBP = 0042FE04 EFL = 00000210

Relevant memory is the following,

0x0042FD20 fa 36 97 77  
0x0042FD24 f2 32 97 77  
0x0042FD28 a8 7e 57 00  
0x0042FD2C 00 00 00 00  
0x0042FD30 00 00 00 00  
0x0042FD34 00 e0 fd 7e  
0x0042FD38 cc cc cc cc  
0x0042FD3C cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_5.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jz label1 in the above program?  

a) 011B13DE  
b) 011B13E5  
c) 011B13EA  
d) 011B13EE  

**Answer** a) 

**Description**

Here after the instruction, jz label1, it will jump as Zero flag is 1 and the value of the comparison is 0. So EIP will be pointing to label1, not to next instruction, which is 011B13DE.  Je (jump equal to) shown in the disassembly is same as jz in the program, as jump on zero means both values are equal.

---
---


6 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov esi, 3
        cmp edx, esi
        jnz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003AFEAC EIP = 009D13E5 ESP = 003AFDD4 EBP = 003AFEAC EFL = 00000200

Relevant memory is the following,

0x003AFDC8 fa 36 97 77  
0x003AFDCC f2 32 97 77  
0x003AFDD0 a8 7e 79 00  
0x003AFDD4 00 00 00 00  
0x003AFDD8 00 00 00 00  
0x003AFDDC 00 e0 fd 7e  
0x003AFDE0 cc cc cc cc  
0x003AFDE4 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_6.jpg" width="400"/>

What will be the value of ESI after the execution of the instruction mov esi, 3?  

a) CCCCCCCC  
b) 00000000  
c) 00000003  
d) None of the above  

**Answer** c) 

**Description**

By the instruction mov esi, 3 we are moving the value 3 to ESI, so it will become 00000003.  

---
---


7 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov esi, 3
        cmp edx, esi
        jnz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003AFEAC EIP = 009D13E5 ESP = 003AFDD4 EBP = 003AFEAC EFL = 00000200

Relevant memory is the following,

0x003AFDC8 fa 36 97 77  
0x003AFDCC f2 32 97 77  
0x003AFDD0 a8 7e 79 00  
0x003AFDD4 00 00 00 00  
0x003AFDD8 00 00 00 00  
0x003AFDDC 00 e0 fd 7e  
0x003AFDE0 cc cc cc cc  
0x003AFDE4 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_7.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov esi, 3?  

a) 009D13DE  
b) 009D13E5  
c) 009D13EA  
d) 009D13EC  

**Answer** c) 

**Description**

After the instruction mov esi, 3 the EIP will be pointing to next instruction, which is 009D13EA   and it is evident from the disassembly.

---
---


8 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov esi, 3
        cmp edx, esi
        jnz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003AFEAC EIP = 009D13E5 ESP = 003AFDD4 EBP = 003AFEAC EFL = 00000200

Relevant memory is the following,

0x003AFDC8 fa 36 97 77  
0x003AFDCC f2 32 97 77  
0x003AFDD0 a8 7e 79 00  
0x003AFDD4 00 00 00 00  
0x003AFDD8 00 00 00 00  
0x003AFDDC 00 e0 fd 7e  
0x003AFDE0 cc cc cc cc  
0x003AFDE4 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_8.jpg" width="400"/>

Which Flag/s will get set after the instruction cmp edx, esi in the above program?  

a) Sign flag  
b) Carry flag  
c) Zero flag  
d) Both a & b  

**Answer** d) 

**Description**

cmp edx, esi is subtracting esi from edx, so 1 – 3, which is a negative value. So the Sign flag will become 1. Also the entire register will overflow and Carry flag will also get set.  

---
---


9 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov esi, 3
        cmp edx, esi
        jnz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003AFEAC EIP = 009D13E5 ESP = 003AFDD4 EBP = 003AFEAC EFL = 00000200

Relevant memory is the following,

0x003AFDC8 fa 36 97 77   
0x003AFDCC f2 32 97 77  
0x003AFDD0 a8 7e 79 00   
0x003AFDD4 00 00 00 00  
0x003AFDD8 00 00 00 00  
0x003AFDDC 00 e0 fd 7e  
0x003AFDE0 cc cc cc cc  
0x003AFDE4 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_9.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, cmp edx, esi in the above program?  

a) 009D13DE  
b) 009D13E5  
c) 009D13EA  
d) 009D13EC  

**Answer** d) 

**Description**

After the instruction, cmp edx, esi the EIP will be pointing to next instruction which is 009D13EC and it is evident from the disassembly. Jne (jump not equal) shown in the disassembly is same as jnz in the program, as jump on non zero means the values are not equal.  

---
---


10 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    label1:
        int a = 20;

    __asm
    {	
        mov esi, 3
        cmp edx, esi
        jnz label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 003AFEAC EIP = 009D13E5 ESP = 003AFDD4 EBP = 003AFEAC EFL = 00000200

Relevant memory is the following,

0x003AFDC8 fa 36 97 77  
0x003AFDCC f2 32 97 77  
0x003AFDD0 a8 7e 79 00  
0x003AFDD4 00 00 00 00  
0x003AFDD8 00 00 00 00  
0x003AFDDC 00 e0 fd 7e  
0x003AFDE0 cc cc cc cc  
0x003AFDE4 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_10.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jnz label1 in the above program?  

a) 009D13DE  
b) 009D13E5  
c) 009D13EA  
d) 009D13EC  

**Answer** a) 

**Description**

Here after the instruction, jnz label1, it will jump as the value of Zero flag is 0 and the result of previous operation is not 0. So EIP will be pointing to label1, not to next instruction, which is  009D13DE. Jne (jump not equal) shown in the disassembly is same as jnz in the program, as jump on non zero means the values are not equal.       

---
---


11 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov esi, 7
        add edx, esi
        jmp label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0022FB10 EIP = 00FF13E5 ESP = 0022FA38 EBP = 0022FB10 EFL = 00000214

Relevant memory is the following,

0x0022FA2C fa 36 89 77  
0x0022FA30 f2 32 89 77  
0x0022FA34 a8 7e 57 00  
0x0022FA38 00 00 00 00  
0x0022FA3C 00 00 00 00  
0x0022FA40 00 e0 fd 7e  
0x0022FA44 cc cc cc cc  
0x0022FA48 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_11.jpg" width="400"/>

What will be the value of ESI after the execution of the instruction mov esi, 7?  

a) 00000000  
b) 00000007  
c) 0022FA38  
d) 0022FA34  

**Answer** b) 

**Description**

By the instruction mov esi, 7 we are moving the value 7 to ESI, so it will become 00000007.  

---
---


12 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov esi, 7
        add edx, esi
        jmp label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0022FB10 EIP = 00FF13E5 ESP = 0022FA38 EBP = 0022FB10 EFL = 00000214

Relevant memory is the following,

0x0022FA2C fa 36 89 77  
0x0022FA30 f2 32 89 77  
0x0022FA34 a8 7e 57 00  
0x0022FA38 00 00 00 00  
0x0022FA3C 00 00 00 00  
0x0022FA40 00 e0 fd 7e  
0x0022FA44 cc cc cc cc  
0x0022FA48 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_12.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction mov esi, 7?  

a) 00FF13DE  
b) 00FF13E5  
c) 00FF13EA  
d) 00FF13EC  

**Answer** c) 

**Description**

After the instruction mov esi, 7 the EIP will be pointing to next instruction, which is 00FF13EA   and it is evident from the disassembly.  

---
---


13 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov esi, 7
        add edx, esi
        jmp label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0022FB10 EIP = 00FF13E5 ESP = 0022FA38 EBP = 0022FB10 EFL = 00000214

Relevant memory is the following,

0x0022FA2C fa 36 89 77  
0x0022FA30 f2 32 89 77   
0x0022FA34 a8 7e 57 00  
0x0022FA38 00 00 00 00  
0x0022FA3C 00 00 00 00  
0x0022FA40 00 e0 fd 7e  
0x0022FA44 cc cc cc cc  
0x0022FA48 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_13.jpg" width="400"/>

What will be the value of EDX after the execution of the instruction add edx, esi?  

a) 00000001  
b) 00000000  
c) 00000008  
d) 00000007  

**Answer** c) 

**Description**

By the instruction, add edx, esi we are adding esi and edx. So the value of EDX will become 00000008. (1 + 7)  

---
---


14 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov esi, 7
        add edx, esi
        jmp label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0022FB10 EIP = 00FF13E5 ESP = 0022FA38 EBP = 0022FB10 EFL = 00000214

Relevant memory is the following,

0x0022FA2C fa 36 89 77  
0x0022FA30 f2 32 89 77  
0x0022FA34 a8 7e 57 00  
0x0022FA38 00 00 00 00  
0x0022FA3C 00 00 00 00  
0x0022FA40 00 e0 fd 7e  
0x0022FA44 cc cc cc cc  
0x0022FA48 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_14.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, add edx, esi?  

a) 00FF13DE  
b) 00FF13E5  
c) 00FF13EA  
d) 00FF13EC  

**Answer** d) 

**Description**

After the instruction, add edx, esi, the EIP will be pointing to next instruction, which is 00FF13EC and it is evident from the disassembly.  

---
---


15 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
  label1:
    int a = 20;

    __asm
    {	
        mov esi, 7
        add edx, esi
        jmp label1
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0022FB10 EIP = 00FF13E5 ESP = 0022FA38 EBP = 0022FB10 EFL = 00000214

Relevant memory is the following,

0x0022FA2C fa 36 89 77  
0x0022FA30 f2 32 89 77  
0x0022FA34 a8 7e 57 00  
0x0022FA38 00 00 00 00  
0x0022FA3C 00 00 00 00  
0x0022FA40 00 e0 fd 7e  
0x0022FA44 cc cc cc cc  
0x0022FA48 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_15.jpg" width="400"/>

What will be the value of EIP after the execution of the instruction, jmp label1?  

a) 00FF13DE  
b) 00FF13EE  
c) 00FF13EA  
d) 00FF13EC  

**Answer** a) 

**Description**

Jmp label1 is unconditional jump. So it will jump to label1. So the EIP will be 00FF13DE, which is evident from disassembly.

---
---


16 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        mov dword ptr[esp], 8h
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033F99C EIP = 009A13DE ESP = 0033F8D0 EBP = 0033F99C EFL = 00000200

Relevant memory is the following,

0x0033F8C4 30 7e 66 00  
0x0033F8C8 00 00 00 00  
0x0033F8CC 00 00 00 00  
0x0033F8D0 00 00 00 00  
0x0033F8D4 00 00 00 00  
0x0033F8D8 00 e0 fd 7e  
0x0033F8DC cc cc cc cc  
0x0033F8E0 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_16.jpg" width="400"/>

What is the value of ESP after the execution of the instruction, sub esp, 4?  

a) 0033F8D0  
b) 0033F8CC  
c) 0033F8C8  
d) 0033F8D4  

**Answer** b) 

**Description**

Sub esp, 4 is allocating 4 bytes of stack memory, so ESP will become 0033F8CC.    

---
---


17 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        mov dword ptr[esp], 8h
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033F99C EIP = 009A13DE ESP = 0033F8D0 EBP = 0033F99C EFL = 00000200

Relevant memory is the following,

0x0033F8C4 30 7e 66 00  
0x0033F8C8 00 00 00 00  
0x0033F8CC 00 00 00 00  
0x0033F8D0 00 00 00 00  
0x0033F8D4 00 00 00 00  
0x0033F8D8 00 e0 fd 7e  
0x0033F8DC cc cc cc cc  
0x0033F8E0 cc cc cc cc  

Disassembly is the following,

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_17.jpg" width="400"/>

What is the value of EIP after the execution of the instruction, sub esp, 4?  

a) 009A13DE  
b) 009A13E1  
c) 009A13E8  
d) 009A13E9  

**Answer** b) 

**Description**

After the execution of the instruction, sub esp, 4, EIP will be pointing to the next instruction whose EIP is 009A13E1 and it is evident from the disassembly.  

---
---


18 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        mov dword ptr[esp], 8h
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033F99C EIP = 009A13DE ESP = 0033F8D0 EBP = 0033F99C EFL = 00000200

Relevant memory is the following,

0x0033F8C4 30 7e 66 00  
0x0033F8C8 00 00 00 00  
0x0033F8CC 00 00 00 00  
0x0033F8D0 00 00 00 00  
0x0033F8D4 00 00 00 00  
0x0033F8D8 00 e0 fd 7e  
0x0033F8DC cc cc cc cc    
0x0033F8E0 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_18.jpg" width="400"/>

What will be the value of the memory location 0033F8CC after the execution of the instruction, mov dword ptr[esp], 8h?  

a) 00000000  
b) 0033F8D0  
c) 0033F8C8  
d) 00000008  

**Answer** d) 

**Description**

We are moving the value 8h to the memory location [esp], which is 0033F8CC. So its value will become 00000008.   

---
---


19 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        mov dword ptr[esp], 8h
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033F99C EIP = 009A13DE ESP = 0033F8D0 EBP = 0033F99C EFL = 00000200

Relevant memory is the following,

0x0033F8C4 30 7e 66 00  
0x0033F8C8 00 00 00 00  
0x0033F8CC 00 00 00 00  
0x0033F8D0 00 00 00 00  
0x0033F8D4 00 00 00 00  
0x0033F8D8 00 e0 fd 7e  
0x0033F8DC cc cc cc cc  
0x0033F8E0 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_19.jpg" width="400"/>

What is the value of EIP after the execution of the instruction, mov dword ptr[esp], 8h?  

a) 009A13DE  
b) 009A13E1  
c) 009A13E8  
d) 009A13E9  

**Answer** c) 

**Description**

After the execution of the instruction, mov dword ptr[esp], 8h , EIP will be pointing to the next instruction which is 009A13E8 and it is evident from the disassembly.  

---
---


20 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        mov dword ptr[esp], 8h
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033F99C EIP = 009A13DE ESP = 0033F8D0 EBP = 0033F99C EFL = 00000200

Relevant memory is the following,

0x0033F8C4 30 7e 66 00  
0x0033F8C8 00 00 00 00  
0x0033F8CC 00 00 00 00  
0x0033F8D0 00 00 00 00  
0x0033F8D4 00 00 00 00  
0x0033F8D8 00 e0 fd 7e  
0x0033F8DC cc cc cc cc  
0x0033F8E0 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_20.jpg" width="400"/>

What will change after the execution of the instruction, pop eax?  

a) ESP  
b) EIP  
c) EAX  
d) All of the above  

**Answer** d) 

**Description**

Pop eax is effectively two instructions, mov eax, dword ptr[esp] (readingfrom memory) and add esp, 4 (deallocating stack memory). So EAX & ESP will change. EIP will be pointing to next instruction, so it also will change.  

---
---


21 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        mov dword ptr[esp], 8h
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033F99C EIP = 009A13DE ESP = 0033F8D0 EBP = 0033F99C EFL = 00000200

Relevant memory is the following,

0x0033F8C4 30 7e 66 00  
0x0033F8C8 00 00 00 00  
0x0033F8CC 00 00 00 00  
0x0033F8D0 00 00 00 00  
0x0033F8D4 00 00 00 00  
0x0033F8D8 00 e0 fd 7e  
0x0033F8DC cc cc cc cc  
0x0033F8E0 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_21.jpg" width="400"/>

What is the value of ESP after the execution of the instruction, pop eax?  

a) 0033F8D0  
b) 0033F8CC  
c) 0033F8C8  
d) 0033F8D4  

**Answer** a) 

**Description**

Pop eax is effectively two instructions, mov eax, dword ptr[esp] (readingfrom memory) and add esp, 4 (deallocating stack memory). So ESP will return to its previous value 0033F8D0.   

---
---


22 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        mov dword ptr[esp], 8h
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033F99C EIP = 009A13DE ESP = 0033F8D0 EBP = 0033F99C EFL = 00000200

Relevant memory is the following,

0x0033F8C4 30 7e 66 00  
0x0033F8C8 00 00 00 00  
0x0033F8CC 00 00 00 00  
0x0033F8D0 00 00 00 00  
0x0033F8D4 00 00 00 00  
0x0033F8D8 00 e0 fd 7e  
0x0033F8DC cc cc cc cc  
0x0033F8E0 cc cc cc cc  

Disassembly is the following,  

<img src="https://github.com/sourcelens/The_Ultimate_Beginners_Course_For_ComputerScience_Or_IT/blob/main/Questions/Q_53_AssemblyMultipleInstructionPractice_jmp_pop/Images/Q_53_22.jpg" width="400"/>

What is the value of EIP after the execution of the instruction, pop eax?  

a) 009A13DE  
b) 009A13E1  
c) 009A13E8  
d) 009A13E9  

**Answer** d) 

**Description**

After the execution of the instruction, pop eax, EIP will be pointing to the next instruction which is 009A13E9 and it is evident from the disassembly.   

---
---


23 : We have the below program,  

```
#include "stdafx.h"
int _tmain(int argc, _TCHAR* argv[])
{
    __asm
    {
        sub esp, 4
        mov dword ptr[esp], 8h
        pop eax
    }
    return 0;
}
```

Register values are the following,

EAX = CCCCCCCC EBX = 7EFDE000 ECX = 00000000 EDX = 00000001 ESI = 00000000 EDI = 0033F99C EIP = 009A13DE ESP = 0033F8D0 EBP = 0033F99C EFL = 00000200

Relevant memory is the following,

0x0033F8C4 30 7e 66 00  
0x0033F8C8 00 00 00 00  
0x0033F8CC 00 00 00 00  
0x0033F8D0 00 00 00 00  
0x0033F8D4 00 00 00 00  
0x0033F8D8 00 e0 fd 7e   
0x0033F8DC cc cc cc cc  
0x0033F8E0 cc cc cc cc  

Disassembly is the following,  

<img src="" width="400"/>

What is the fate of the program?




