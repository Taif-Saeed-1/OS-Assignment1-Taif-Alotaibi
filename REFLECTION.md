# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

This assignment taught me how multithreading enables the simultaneous execution of several tasks within a single process. I understood how threads are created and managed using methods like start() and run(). Additionally, I discovered that threads communicate more quickly than processes since they share memory. One key idea I discovered is how scheduling algorithms, such as Round-Robin, regulate thread execution. I also saw how threads change states while they are being executed. This made it easier for me to comprehend how actual operating systems effectively handle several tasks. In general, this task helped me better grasp CPU scheduling and concurrency.

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

Understanding the internal workings of the scheduling mechanism was the hardest element of this project. In particular, it was challenging to decide when and where to apply features like waiting time calculation and context switch counting. Careful code tracing was necessary because of how threads interacted with the ready queue. Making sure that changes did not impair the original functionality presented another difficulty. It was also difficult to understand where the logic should be placed within the code. It also took more work to connect theoretical ideas with real code implementation. Because of this, the task was both difficult and instructive.

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

By closely examining the code and methodically testing each change, I was able to overcome these obstacles. I monitored the flow of threads through the system using debugging and displayed outputs. In order to solidify my grasp of scheduling and threading ideas, I also went over the lecture materials again. I was able to concentrate on one aspect at a time by breaking the problem down into smaller components. To prevent adding errors, I made sure to test the application after every modification. I also looked at how each feature influences the system's overall behavior. I was able to progressively comprehend and successfully finish the task thanks to this method.

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

Real-world applications including operating systems, mobile apps, and web browsers frequently use multithreading. Web browsers, for instance, use threads to load several tabs at once. Threads are used by mobile applications to manage background operations, such as retrieving data, without causing the UI to freeze. Threads are utilized in games to concurrently handle user input, physics, and visuals. To effectively manage several processes, operating systems mostly rely on multithreading. I gained a better understanding of how these systems guarantee timeliness and fairness thanks to this assignment. Additionally, it demonstrated the practical applications of scheduling algorithms.---

## Additional Reflections (Optional)

### What would you like to learn more about?

I'd like to know more about thread synchronization and how to prevent deadlocks and race situations in complicated systems.
---

### How confident do you feel about multithreading concepts now?

I consider myself to be intermediate. I still need more practice with more complex issues like synchronization and performance optimization, but I do understand the fundamental ideas and how threads work.

---

### Feedback on the assignment

Understanding how operating system scheduling functions was greatly aided by the assignment. It offered a useful method for putting theoretical ideas into practice. But it needed close attention to detail, particularly when making changes to the code. All in all, it was a worthwhile educational experience.
