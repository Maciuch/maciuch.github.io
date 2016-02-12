---
title: Environment setup
author: Maciej Maciejewski
layout: post
---
NVML is meant to facilitate NVM programming model. 
Data allocated with NVML is put to the virtual memory address space, and concrete ranges are relaying on result of mmap(2) operation performed on the user defined files.
Such files can exist on any storage media, however data consistency assurance embedded within NVML requires frequent synchronisation of data that is being modified. Depending on platform capabilities, and underlying device where the files are, a different set of commands is used to facilitate synchronisation. It might be msync(2) for the regular hard drives, or combination of cache flushing instructions followed by memory fence instruction for the real persistent memory.

That is the reason to work either with real equipment (type 1) or emulated environment.

### DAX enabled filesystem
What is DAX
Getting Kernel >4.2
Configuring Kernel
Seeing the device
Installing filesystem

### NVML Setup 
Fetching NVML
Compiling
PMEM is PMEM

