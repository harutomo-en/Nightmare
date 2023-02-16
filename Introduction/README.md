# Introduction

In the introduction of Nightmare, the objective was to familiarize myself with assembly language (it's registers and instructions) as well as get somewhat comfortable navigating and utilizing the most popular tools for reversing and binary exploitation:

* Python scripting with Pwntools
* Using GDB to view and analyze assembly code and registers of binaries
* Using Ghidra to decompile a binary into C

The end goal of the Introduction was to to accomplish a few CTF style challenges using previously mentioned tools.


Assembly Crash Course Video
https://www.youtube.com/watch?v=75gBFiFtAb8


## What is assembly code?

Assembly code is a more accurate representation of what actually is run on the computer by the processor when you execute a program.  For example, a standard "Hello, World!" program in C, when compiled, produces the following assembly code:

<img src="https://i.imgur.com/NkqNuhC.png" align="center" alt="isolated"/>


Although languages like C make it easier to not having to deal with assembly programming for the sake of easier software development.  However, when dealing with malware or looking to exploit programs, more often than not we are working with compiled binaries without the accompanying source code.  This means the only way to understand exactly what a program does when it is run is by looking at the assembly code.

###### Architectures

There are different types of assembly code architectures, however since I am running on a UNIX system and the Nightmare course primarily discusses UNIX type architecture assembly, the architectures that will be discussed most are 64 bit ELF (x64) and 32 bit ELF (x86).