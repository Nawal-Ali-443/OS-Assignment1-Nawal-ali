# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**A process is an independent program with its own memory space, while a thread is a smaller unit of execution that runs inside a process and shares its memory. Threads are faster to create and have lower overhead compared to processes, which makes them more efficient for concurrent tasks. In this assignment, we used threads instead of processes because all tasks share the same memory and need fast communication during scheduling. For example, in SchedulerSimulation.java, each process is executed using a Thread object and managed in a ready queue. Also, threads allow faster context switching and better performance when applying the Round-Robin scheduling algorithm.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**:In Round-Robin scheduling, if a process does not finish within its time quantum, it is placed back at the end of the ready queue. This ensures that all processes get a fair share of CPU time and prevents starvation. For example, in the program output, you may see a process like P1 running for a short time and then being re-added to the queue with remaining time. This re-queuing behavior allows other processes to execute before P1 gets another turn. It is important because it maintains fairness and balanced CPU utilization among all processes.>> example from Your program output P1 added to ready queue
? P1 executing quantum [5000ms] 
  ? Quantum progress: [???????????????] 100%
  ? P1 completed quantum 5000ms ? Overall progress: [????????????????????] 80%
     Remaining time: 1199ms
  ? P1 yields CPU for context switch

  ? P1 added to ready queue ? Burst time: 6199ms
?? Ready Queue ?????????????????????????????????????????????????????????????????
? [P3 ? P4 ? P5 ? P6 ? P7 ? P8 ? P9 ? P10 ? P11 ? P12 ? P13 ? P14 ? P15 ? P16 ? P1]
????????????????????????????????????????????????????????????????????????????????

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/6c1e2a35-ab30-45bf-818b-7c82259ce10d" />
Explain why this re-queueing behavior is important for fairness in CPU scheduling?
Because  complete her work and not finished
[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]



## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

****

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]

2. **Runnable**: [When does P1 become Runnable?]

3. **Running**: [When is P1 Running?]

4. **Waiting**: [When/why would P1 be Waiting?]

5. **Terminated**: [When is P1 Terminated?]
New: P1 is in New state after new Thread(process) is called in addProcessToQueue(), creating the thread object before it starts.

Runnable: P1 becomes Runnable when currentThread.start() is called in the main scheduling loop, making it ready for CPU execution.

Running: P1 is Running when the OS scheduler selects it and begins executing the run() method, calculating runtime and processing its quantum.

Waiting: P1 enters Timed-Waiting when Thread.sleep(stepTime) is called during execution to simulate work progress; the main thread also waits via currentThread.join() for P1 to complete.

Terminated: P1 is Terminated when the run() method returns normally after completing its quantum or

finishing entirely via runToCompletion().
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

Example 1: Web Server Handling Client Requests

Description:
A web server receives multiple requests from different users at the same time, such as loading web pages or submitting forms. Each request is handled by a separate thread, and all threads are placed in a ready queue to be executed by the CPU. Similar to our program, requests take turns executing just like processes P1, P2, and P3 in the output. If a request is not completed within its time quantum, it goes back to the queue with remaining processing time. This allows the server to serve many users efficiently without blocking.

Why Round-Robin works well here:
Round-Robin ensures fairness by giving each request equal CPU time, preventing any single request from monopolizing resources. It improves responsiveness because users do not have to wait too long for their request to start processing. The predictable time quantum also helps maintain consistent performance across all requests. This behavior is similar to how our scheduler cycles through processes in a balanced way.

⸻

Example 2: Mobile Applications (Multitasking Apps)

Description:
In mobile devices, multiple applications run simultaneously, such as messaging apps, music players, and background updates. Each app runs as a process with one or more threads, and the CPU switches between them rapidly. Like in our simulation, each task gets a small time quantum to execute before the next one runs. For example, a music app continues playing while a user browses social media because CPU time is shared among tasks. This creates the illusion that everything is running at the same time.

Why Round-Robin works well here:
Round-Robin scheduling is ideal because it provides fair CPU access to all applications, ensuring no app is completely blocked. It enhances user experience by keeping the system responsive and smooth. The frequent context switching allows background tasks to progress without interrupting foreground activities. This is similar to how processes in our program share CPU time equally and continue execution in cycles.

## Summary


**Key concepts I understood through these questions:**
1. I understood the difference between threads and processes and why threads are more efficient for this assignment.
 2. I learned how Round-Robin scheduling works by giving each process a fixed time quantum and re-queuing unfinished processes.
 3. I understood the thread lifecycle and how threads move between different states during execution.
 

**Concepts I need to study more:**
 1. Thread synchronization and how to avoid issues like race conditions.
 2. Other CPU scheduling algorithms and how they compare to Round-Robin in performance and efficiency.
