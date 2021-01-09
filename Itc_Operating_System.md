<font face="Dejavu Sans"/>

# ItC Week 12 - Operating System

###### tags: `Intro_to_Comp`

- ## What is OS
  - Goals
    - Execute user programs and make solving user problems easier
    - Make the computer system convenient to use
    - Use the computer hardware in an efficient manner
  - A resouce allocator
    - Manage which resource can be used by which program
  - A control program

- ## Startup
  - "bootstrap program" is loaded at powerup or reboot
    - Usually stored in ROM or EPROM
    - aka firmware
    - Initialize system in all aspects
    - Loads OS kernel and transfer control to it

- ## Intertupt
  - Function 
    - An interrupt transfers control to the interrupt service routine
    - Through the "Interrupt vector", which contains the addresses of all service routines
    - Interrupt architecture must save the address of the interrupted instuction
    - A "trap" or "exception" si a software-generated interrupt caused by either an erro ror a user request
    - An OS support such things is "interrupt driven".
  - Interrupt handling
    - OS preserves CPU state by storing registers and program counter
    - Determines which type of interrupt has occerred
      - Vectored interrupt system
      - Polling
        - poll each possible I/O device, check for requests




- ## Cache
  - Use some faster storage to store often-accessed data
  - Replacement policy
    - FIFO
    - MRU
    - LRU

- ## System Architecture
  - Multiprocessors
    - pros
      - increase throughput
      - economy
      - increase reliability
    - types
      - asymmetric
      - symmetric
  - Types
    - Asymmetric Multiprocessing
      - each processor is assigned with a specific task
    - SYmmetric Multiprocessing
      - each processor performs all tasks

- ## Clustered Systems
  - Multiple systems working together
  - Share storage via a storage-area network (SAN)
  - high-availability bc is can survive some failure
    - Asymmetric clustering
      - one machine in hot-standby mode
    - Symmetric clustering
      - multiple nodes running apps and monitoring each other
  - Some have distributed lock manager to avoid conflicting operations

- ## OS Structure
  - Multiprogramming (Batch System)
    - job scheduling
    - switch other job when waiting (like I/O)
  - Timesharing (Multitasking)
    - CPU scheduling
    - memory swapping
    - virtual memory
  
- ## OS Operations
  - Interrupt
    - hardware
    - software
      - software error
      - system request
      - infinite loop....
  - Dual-mode
    - allow OS protects and other system components
    - 

{%hackmd OQo9p0ONRaSb9WIkZQZZ7w %}