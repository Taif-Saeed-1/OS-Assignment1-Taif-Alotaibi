# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

A thread is a smaller unit of execution that resides within a process and shares its memory, whereas a process is an independent program in execution with its own memory space and system resources. Compared to processes, threads are lighter and may be created and switched between more quickly. While threads can communicate effectively through shared variables, processes need greater overhead because they do not share memory. Because threads enable many jobs (process simulations) to run concurrently with reduced overhead, we used them in this assignment. As a result, the scheduler simulation becomes more accurate and resembles actual CPU scheduling behavior.
---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

A process is pushed back to the end of the ready queue in Round-Robin scheduling if it does not complete within the allotted time quantum. By letting each process use the CPU in turn, this guarantees equity for all. It is evident from the program output that processes that fail to finish their execution are queued up and run again at a later time.

Example from my output:

▶ P2 executing quantum [4000ms]
⚡ Quantum progress: [███████████████] 100%
⏸ P2 completed quantum 4000ms │ Overall progress: [█████████░░░░░░░░░░░] 46%
   Remaining time: 4676ms
↻ P2 yields CPU for context switch

**Explanation of example:**
In this instance, process P2 ran for one full time quantum (4000 ms), however it didn't finish because 4676 ms remained. As a result, it returns to the ready queue after yielding the CPU. It will be rescheduled once other processes have had a chance. This illustrates how Round-Robin scheduling guarantees equity and keeps the CPU from being monopolized by any one operation.
---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

Throughout its lifetime, a thread goes through a number of states. The real program output in this simulation allows us to track the states of process P2.


1. **New**: When the process is initialized and ready to enter the system before execution starts, a thread is generated.


2. **Runnable**: When the thread is prepared for scheduling and is awaiting CPU time in the ready queue, it becomes runnable.


3. **Running**: When the thread is chosen by the scheduler, it goes into the running state: ▶  P2 executing quantum [4000ms]



4. **Waiting**: The thread releases the CPU after finishing its quantum but not its execution: ↻ P2 yields CPU for context switch                                       At this point, it waits for its next turn in the ready queue.



5. **Terminated**:The thread completes its execution and leaves the system when the remaining time is zero (this shows up later in the output after the process is finished).

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**
In real-world systems where responsiveness and fairness are crucial, round-robin scheduling is frequently employed. It makes it possible for several tasks to effectively share CPU time

### Example 1: Web Server

**Description**: 
A web server uses threads to manage several client requests at once.


**Why Round-Robin works well here**: 
Every request receives an equal amount of CPU time thanks to Round-Robin. This increases responsiveness for all users and stops any one request from blocking others.

### Example 2:Operating System Task Scheduling

**Description**: 
Operating systems distribute CPU time among several active programs.


**Why Round-Robin works well here**: 
By allocating a time slice to each task, Round-Robin guarantees equity. It keeps the system snappy and avoids hunger, particularly when a lot of apps are running.
---

## Summary

**Key concepts I understood through these questions:**
1. How threads share memory and how they vary from processes
2. How Round-Robin scheduling ensures process fairness
3. A thread's life cycle and state transitions

**Concepts I need to study more:**
1. Avoiding race situations and synchronizing threads
2. Complex concurrency ideas include resource management and deadlocks 
