# Chapter 4
## Process Abstraction

**crux**: creating the illusion of many cpus

**process**: a running program 

**machine state of a process**: what a program reads or writes, what’s important to the execution of the program  

e.g. address space: memory that the process can address  

e.g registers: instructions read or update registers  

Special registers:  

- program counter/instruction pointer: tells the instruction that will execute next  

- stack pointer/frame pointer: manage the stack  

**process api**: create/destroy/wait/status/miscellaneous(suspend,resume) processes

### Process creation:
1. load code and static data to memory, done lazily, i.e., load only when needed  
2. allocate memory for stack and heap  
3. initialization tasks, e.g. I/O  
4. execute at main()

### Process states:

Events transfer the states of processes  

OS makes decisions of when to run different processes

**Process Structure**: the OS will keep a process list to keep track of all processes

### Virtualizing the cpu:
- **time sharing**: running one process, stop one and run another one, and so forth  
- **space sharing**: resource is divided in space  
- **context switch**: stop running one program and start another  

**mechanisms**(how?): low level methods that implement a functionality  

**policies**(which?): algorithms for making decisions within the OS, e.g. scheduling policy

