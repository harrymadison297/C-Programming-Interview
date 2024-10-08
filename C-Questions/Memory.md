## C Memory
### 1. Memory layout of a process?
![](/Assets/memory_layout_of_a_process.png)
A process has main memory component:
* Text segment
* Data segment (Initialized Data Segment)
* BSS segment (uninitialized Data Segment)
* Heap
* Memory mapping segment
* Stack

![](/Assets/process_mem.png)
Memory has about 4Gb memory for detail:
* 0x00000000 - 0x00399999 (4MB) : Unuse part
* 0x00400000: Start address by .elf file
* 0x00400000 - 0x00401000 (4KB) : Text Segment, min size is 4KB. Text Segment is where to save code of program. User couldn't modify this memory.
* 0x00600000 - 0x00601000 (4KB) : Initialize Data Segment, min is 4KB, where to save all global, static and external variable has initalized value.
* 0x00601000 - 0x00602000 (4KB) : BSS segment, min is 4KB, where to save global, static variable has init by 0 or uninitalized.
* ....

### 3. Stack segment and stack frame
Stack frame has structure:
* Function parameter
* Return address
* Saved previous frame pointer
* Local variable

### 4. Heap segment

### 5. Memory mapping segment
Contain files Shared Lib with ext .so. Address of librarys change each time run.
