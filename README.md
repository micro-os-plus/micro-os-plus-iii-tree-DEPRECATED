# µOS++ IIIe repo

The **µOS++ IIIe** (micro oh ɛs plus plus third edition) project is the 
third iteration of **µOS++**, an open source, royalty-free, multi-tasking 
operating system intended for embedded systems, focused on Cortex-M device.

**µOS++** is composed of multiple separate pacakges, each hosted as a 
GitHub project. Original packages are hosted in 
[µOS++](https://github.com/micro-os-plus) and packages based on 
third party code are hosted in [xPacks](https://github.com/xpacks).

To achieve packages integration, this project makes extensive use 
of `git` submodules.

It is mainly used as a convenience during development.

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

This project is currently in early development stage.

Files from previous versions are updated, packed as separate packages and 
linked to this repository.

During this stage the focus is less on contributing original code, and more on 
defining the various layers and APIs, the initial implementation relying on
existing code, like CMSIS RTOS, FreeRTOS, lwIP, FAT FS, etc.

The central piece is a POSIX IO layer, that brings together, under a 
standard API, files, sockets, devices, etc.

As for RTOS, currently the preferred API is CMSIS RTOS; it is not perfect, but 
for the moment it shoud be just fine.

