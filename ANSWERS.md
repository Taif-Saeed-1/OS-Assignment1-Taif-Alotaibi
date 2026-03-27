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

A process is pushed back to the end of the ready queue in Round-Robin scheduling if it does not complete within the allotted time quantum. This ensures fairness by giving other processes an opportunity to run. A thread in the program gets re-added to the queue and waits for its next turn when it completes its time slice but still has time left. No process will be able to monopolize the CPU thanks to this behavior.
Example from my output:

P1 added to ready queue
P1 executing...
P1 not finished, re-queued

**Explanation of example:**
In this instance, process P1 was moved back to the end of the queue since it failed to finish its burst period within one quantum. It will then be chosen once more and carried out. This illustrates how Round-Robin scheduling equitably cycles through processes.
---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

Throughout its lifetime, a thread goes through a number of states. The states of process P1 in this simulation can be traced as follows:


1. **New**: When the Process object is initialized but has not yet begun to execute, a thread is generated.

2. **Runnable**: The thread is prepared to execute when it is added to the ready queue and the start() method is invoked.

3. **Running**: When the scheduler chooses a thread and starts utilizing CPU time to execute it, the thread enters the running state.

4. **Waiting**: When a thread is suspended using techniques like sleep(), it may go into a waiting state so that other threads can run.

5. **Terminated**: When the thread's execution is complete and its remaining time is zero, it enters this state.

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
