# µOS++ IIIe tree repo

The **µOS++ IIIe** _(micro oh ɛs plus plus third edition)_ project is the 
third iteration of **µOS++**, an open source, royalty-free, multi-tasking 
operating system intended for embedded systems, focused on Cortex-M device.

This GitHub repository project is basically a tree of references to other 
projects
and does not contain any source code; for the actual code please refer to 
the linked projects.

To achieve packages integration, this repository makes extensive use 
of `git` submodules.

This project is mainly used as a convenience during development.

## CMSIS++

The core component of **µOS++** is **CMSIS++**, a proposal for the next 
generation **CMSIS**.

**µOS++** also provides a reference implementation for the CMSIS++ RTOS 
scheduler. A POSIX synthetic platform implementation is planned, and
will be provided in the posix-arch xPack. 

## Based on packages

**µOS++** is composed of multiple separate packages, each hosted as a 
GitHub project. Original packages are hosted in 
[µOS++](https://github.com/micro-os-plus) and packages based on 
third party code are hosted in [xPacks](https://github.com/xpacks).

## Folders hierarchy

From the functional point of view, the folders hierarchy is not relevant, since
the content is grouped in packages, and the packages framework automatically
handles dependencies, regardless of the actual location in the hierarchy.

As such, the hierarchy is kept relatively simple:

```
author
└── group
    └── xpack
```

The design is remotely influenced by CMSIS PACK, where packages are 
grouped by vendors.

However, the very rigid naming convention used by CMSIS PACK is not addopted, 
and packages can have any name and each author is free to use any hierarchy.

## Status

This project is currently in development stage.

Files from previous versions are updated, packed as separate packages and 
linked to this repository.

During this stage the focus is less on contributing original code, and more on 
defining the various layers and APIs; the initial implementation will rely on
existing code, like CMSIS RTOS, FreeRTOS, lwIP, FAT FS, etc.

The core APIs are defined in the CMSIS++ package. In addition to the RTOS 
and Drivers APIs, another major component is the POSIX IO layer, that brings 
together, under a standard API, files, sockets, devices, etc.

