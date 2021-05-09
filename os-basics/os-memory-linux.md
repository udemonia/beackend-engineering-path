# Memory Management In Linux

## single address space

Memory and peripherals share

- memory is mapped to one part
- peripherals are mapped to another

All processes and OS share the same memory space

- no memory protection
- process can stomp one another
- user space can stop kernal memory

CPUs w/ single address space

## Virtual Memory

its a mapping -> you map a virtual address to a physical address

- maps virtual address to RAM
- maps virtual address to physical hardware devices

- PCI devices
- GPU RAM
- On-Soc IP Blocks

Advantages

each process can have a different memory mapping - one processes RAM is in accessible to other processes 

Kernel ram is invisible to user space processes

Memory can be moved

Memory can be swapped to disk
