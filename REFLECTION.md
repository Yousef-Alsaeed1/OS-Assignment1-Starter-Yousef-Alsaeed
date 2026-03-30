# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

[Before the assignment i did not know much about multithreading but after implementing the three features i learned how threads are created and managed i learned about context switching which is when the CPU stops one process and starts another i also learned about waiting time which is the total time a process spends waiting in the queue before getting into thr CPU i learned about priority which decide the importance level of each process what surprised me most was how the scheduler keeps track of all processes using a queue and switches between them automatically. This assignment made threading concepts much clearer to me than just reading about them.
 ]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

[
the most challenging part was implementing Feature 3, which had tracking waiting time for each process. This feature required learning several new methods and concepts that i had not used before such as System.currentTimeMillis() to track time. I also had to understand how to use setter and getter methods properly to access private fields the biggest challenge was a bug where the waiting times were showing extremely large numbers after investigating i found that the getcreatedTime() method was returning the priority value instead of createdTime. This taught me how important it is to carefully check what each method returns. debugging this error improved my problem solving skills .]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

[
when I faced challenges my main approach was to search for information about the new methods i needed to use i learned how System.currentTimeMillis() works and how to use it to calculate time differences when I got red underline errors in vscode i read the error messages carefully to understand what was wrong for the bug with getcreatedTime() returning the wrong value i traced through the code step by step until i found the mistake i also tested my code after each small change to make sure it was working correctly before moving on this approach helped me solve problems faster. at the end breaking down each problem into smaller steps made everything easier to handle.]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]
multithreading is used in many applications that we use every day for example in whatsapp threads allow you to receive messages, download photos, and play voice notes all at the same time without the app freezing in video games threads handle graphics rendering sound effects and player input simultaneously to create a smooth experience web browsers use threads to load multiple tabs at the same time without one tab slowing down another the round-robin scheduling concept from this assignment is similar to how operating systems manage multiple applications running on your computer without multithreading, apps would have to complete one task fully before starting another making them very slow. This assignment helped me understand why multithreading is essential for building fast and responsive applications.

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[I am  curious about other scheduling algorithms like priority scheduling and shortest job first.]

---

### How confident do you feel about multithreading concepts now?

[Intermediate]

[I understand how threads are created and how context switching works and how Round Robin scheduling manages processes 
 i still need more practice with advanced concepts like thread synchronization and deadlocks.]

---

### Feedback on the assignment

[ the assignment was definitely helpful and i learned a lot from implementing the features myself instysed of reading about threading concepts. for me it was medium difficulty but becuse it happened with ramadan and eid it was harder to find time to work on it
]
