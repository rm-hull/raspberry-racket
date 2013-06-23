# Rasberry Racket

_document work-in-progress_

Racket v5.2.1 is currently available as a package on the Raspian distribution
for the $25 Raspberry Pi. However the DrRacket environment fails to start:

    $ drracket
    Seg fault internal error at 0x204f398  
    SIGSEGV SEGV_ACCERR SI_CODE 2 fault on 0x204f398
    Aborted
    
The aim of this [Lisp of Summer Projects submission](http://lispinsummerprojects.org/) 
is to get an up-to-date 5.3.x build compiled (with full build documentation) for the 
Raspberry Pi with a working DrRacket GUI and push it back into the Raspbian distro.

## Build instructions

The Raspberry Pi is based on the Broadcom 2708 Cortex ARM6 chipset; There are
two mechanisms for building executables for the Raspberry Pi, either locally
on a Pi itself (which will take approximately XX hours) or cross-compiling on
a unix host. This guide will attempt to document both approaches.

### Pre-requisites

### Building locally

    $ wget http://download.racket-lang.org/installers/5.3.5/racket/racket-5.3.5-src-unix.tgz
    $ tar xvfj racket-5.3.5-src-unix.tgz
    $ cd racket/src
    $ mkdir build
    $ cd build
    $ ../configure
    $ make

