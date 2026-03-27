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

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]

2. **Runnable**: [When does P1 become Runnable?]

3. **Running**: [When is P1 Running?]

4. **Waiting**: [When/why would P1 be Waiting?]

5. **Terminated**: [When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
