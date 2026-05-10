# Concurrent-Memory-Allocator

### Summary
This project is a systems programming and runtime infrastructure project focused on designing and implementing
a custom memory allocator optimized for performance, scalability, and low-level control.
The project aims to replicate the type of engineering work found in:
- Operating Systems
- Game engines
- Database systems
- Browsers
- Compilers and runtimes

The allocator will manage dynamic memory manually rather than relying solely on the default allocator provided
by the operating system or standard library.
### Core Objectives
- Heap Management
- Allocation strategies
- Fragmentation reduction
- Cache locality optimization
- Thread-local allocation
- Lock-free/free-list data structures
- Virtual memory interaction
- Low-level performance engineering
This project is fundamentally about learning how modern runtimes and systems software manage memory efficiently
under real-world workloads.
###Problem Statement
General-purpose allocators such as malloc, new, or standard runtime allocators are designed for broad
compatibility rather than specialization.

Problems with generic allocators include:

- Fragmentation
- Lock contention
- Cache inefficiency
- Poor behavior under specific workloads
- Non-deterministic latency
- Excessive system calls

Modern high-performance systems often implement custom allocators to:

- Reduce allocation latency
- Improve throughput
- Control memory layout
- Improve cache behavior
- Reduce synchronization overhead

This project exists to build a production-style allocator from first principles and understand how modern
runtimes solve these challenges.

## Core Goals

### Goal 1 - Build a Fully Functional Heap Allocator
The allocator should support:

- allocate(size)
- deallocate(ptr)
- aligned allocation
- block splitting
- block coalescing
- metadata management

The allocator should eventually behave similarly to:

- jemalloc
- tcmalloc
- mimalloc

without copying their implementation directly.

### Goal 2 - Understand Low-Level Memory Systems
The project should provide hands-on understanding of:

- Virtual memory
- Heap layout
- Page allocation
- Memory mapping
- Address spaces
- Pointer arithmetic
- Cache alignment
- CPU cache behavior
- TLB effects

### Goal 3 - Optimize for Performance
The allocator should aim for:

- Low allocation latency
- High throughput
- Reduced fragmentation
- Minimal synchronization overhead
- Efficient reuse of freed memory

Performance engineering is a central part of the project.

### Goal 4 — Implement Advanced Allocation Strategies

Potential strategies include:

- Slab allocators
- Arena allocators
- Pool allocators
- Buddy allocators
- Segregated free lists
- Thread-local allocators
- Lock-free freelists

### Goal 5 — Develop Systems Engineering Expertise

The project should demonstrate:

- Advanced C++ knowledge
- Systems-level debugging
- Performance profiling
- Concurrent programming
- Runtime design
- Memory correctness analysis
