# CPE 159 — Real-Time Operating System Kernel

A multi-phase implementation of a real-time operating system (RTOS) kernel built in C, Assembly, and C++, developed as coursework for CPE 159 (Real-Time Operating Systems Principles and Design).

The project was built incrementally across several phases, each adding a new layer of OS functionality — from basic process management to inter-process communication and synchronization.

---

## Overview

This repository contains the full progression of a custom RTOS kernel developed from scratch. Each phase introduced new systems programming concepts and extended the kernel's capabilities.

---

## Phases

| Phase | Description |
|---|---|
| Phase 4 | Initial kernel setup and process initialization |
| Phase 5 | Process scheduling — context switching and the ready queue |
| Phase 6 | System calls and process state management |
| Phase 7 | Inter-process communication (IPC) — message passing |
| Phase 8 | Synchronization primitives — semaphores and blocking |
| Phase 9 | Final integration and system hardening |

> Individual phase directories (e.g. `phase7-FOX`, `phase8-FOX`) contain personal implementations; shared/combined versions are in the base phase folders.

---

## Tech Stack

| Technology | Purpose |
|---|---|
| C | Core kernel implementation |
| Assembly (x86) | Low-level context switching and CPU register management |
| C++ | Supporting utilities |
| Makefile | Build system for compiling multi-file kernel modules |

---

## Key Concepts Demonstrated

- **Process Control Blocks (PCBs)** — Managing process state, priority, and metadata.
- **Context Switching** — Saving and restoring CPU registers in Assembly to switch between processes.
- **Process Scheduling** — Implementing a ready queue and dispatcher for multi-process execution.
- **System Calls** — Designing a kernel-level API for user processes to request OS services.
- **Inter-Process Communication (IPC)** — Message queues enabling communication between running processes.
- **Semaphores** — Implementing counting semaphores for process synchronization and mutual exclusion.
- **Makefiles** — Structured build system to compile and link multi-module kernel code.

---

## Project Structure

```
/
├── PhaseTest/       # Integration test environment
├── phase5/          # Scheduling and context switching
├── phase6/          # System calls (multiple implementations)
├── phase6V2/
├── phase7/          # IPC — message passing
├── phase7-FOX/      # Personal IPC implementation
├── phase7V3/
├── phase8/          # Semaphores and synchronization
├── phase8-FOX/      # Personal semaphore implementation
├── phase8-JR/
├── phase9/          # Final integrated kernel
├── Demo-lab.dli     # Lab demo configuration
└── output.txt       # Sample program output
```

---

## Building

Each phase directory contains its own `Makefile`. To build a specific phase:

```bash
cd phase9
make
```

---

## Background

CPE 159 is a systems programming course focused on the design and implementation of real-time operating systems. Students build a functional RTOS kernel incrementally, learning how modern operating systems manage processes, memory, and hardware at a low level. The course emphasizes hands-on systems programming in C and Assembly.
