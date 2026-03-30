# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[
 A process is a complete independent program running on the computer with its own memory space 
 a thread is a smaller unit that runs inside a process and shares the same memory with other threads in the same process
 the main differences are that threads are much cheaper to create than processes, threads share memory so they can communicate faster and switching between threads is faster than switching between processes
 In this assignment we used threads instead of separate processes because all our processes share the same simulation data like the queue and the map 
 using threads made it easier and faster to simulate multiple processes competing for CPU time.
]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[
    In Round-Robin scheduling when a process does not finish within its time quantum
    it is removed from the CPU and placed back at the end of the ready queue It then waits for all other processes in the queue to get their turn before it runs again
    This ensures fairness because no single process can monopolize the CPU
]


Example from my output:



[  ? P2 executing quantum [3000ms]
  ? Quantum progress: [███████████████] 100%
  ? P2 completed quantum 3000ms │ Overall progress: [█████████████░░░░░░░] 68%
     Remaining time: 1394ms
  ? P2 yields CPU for context switch

  ? P2(Priority: 1) added to ready queue │ Burst time: 4394ms
┌─ Ready Queue ─────────────────────────────────────────────────────────────────
│ [P4 ? P5 ? P6 ? P7 ? P8 ? P9 ? P10 ? P11 ? P12 ? P13 ? P14 ? P2]
└───────────────────────────────────────────────────────────────────────────────
]


**Explanation of example:**
[p2 ran for 3000ms but still had 1394ms remaining and instead of continuing it yielded the cpu and was added back to the end of the queue
 this allowed other processes like p3 and p4 to run before P2 got its next turn. This behavior is important because it gives every process a fair chance to use the cpu.
]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**


1. **New**: [p1 is in the New state when we create it with new Process("P1", burstTime, timeQuantum) and new Thread(process) but before we call start()]

2. **Runnable**: [p1 becomes runnable when we call currentThread.start()  it is ready to run but waiting for the CPU to actually execute it]

3. **Running**: [p1 is Running when the cpu actually executes its run() method]

4. **Waiting**: [p1 enters the Waiting state when Thread.sleep() is called inside the run method  it pauses and waits for the sleep time to finish usaly becuse it is waiting for i/o]

5. **Terminated**: [p1 is Terminated when its run() method finishes completely  this happens when remainingTime reaches 0]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [ Video Game Engine]

**Description**: 
[a video game needs to handle many tasks at the same time such as rendering graphics, playing sounds, detecting player input, and updating game physics
each task runs in its own thread]

**Why Round-Robin works well here**: 
[Round Robin works well here because all these tasks need regular cpu time to keep the game running smoothly if one task like graphics took all the CPU time the game would freeze and not respond to player input
Round Robin ensures each task gets regular turns so the game feels smooth and responsive.]

### Example 2: [Web Server]

**Description**: 
[ a web server receives requests from many users at the same time
  Each user request is handled by a separate thread for example when 100 users visit a website at the same time, the server creates 100 threads to handle them.]

**Why Round-Robin works well here**: 
[Round Robin is suitable because it gives every user request a fair chance to be processed no single user request will block others from being handled This makes the server responsive to all users instead of making some users wait a very long time while others finish quickly.]

---

## Summary

**Key concepts I understood through these questions:**
1. threads share memory while processes do not
2. Round Robin gives every process a fair turn using time quantum
3. Threads go through different states from new to terminated during execution


**Concepts I need to study more:**
1. thread synchronization and avoiding conflicts between threads
2. Other scheduling algorithms like Priority Scheduling and Shortest Job First
