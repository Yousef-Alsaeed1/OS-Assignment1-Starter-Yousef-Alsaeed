# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 27]
**What I did**: setting up GitHub account and fork the repository

**Details**: 
- Created GitHub account using university email
- Forked the starter repository from the professor's account
- Renamed the repository to my name
- Made sure the repository is public
- Set my student ID in SchedulerSimulation.java


**Challenges**: no major challenges

**Solution**: Followed the README instructions step by step

**Time spent**: 30 minutes

---

### Entry 2 - [March 27]
**What I did**: Set up VS code and cloned the repository

**Details**: 
- Downloaded and installed VS Code
- Installed Java Extension Pack
- Cloned my repository to my computer
- Tried to run the code but got a Java version error

**Challenges**: java version was outdated code needed a newer version

**Solution**: Downloaded and installed Java 25 

**Time spent**: 30 minutes

---

### Entry 3 - [March 28]
**What I did**: Implemented feature 1 / Process Priority

**Details**: 
**Details**: 
- Added priority variable to process class
- Added getPriority() getter method
- Modified addProcessToQueue to display priority
- Committed with message "Added priority"


**Challenges**: got red underline because priority was private

**Solution**: created a getter method getPriority() to access it properly

**Time spent**: 1:30 hour

---

### Entry 4 - [March 29]
**What I did**: Implemented Feature 2 / Context Switch Counter

**Details**: 
- Added contextSwitches variable initialized to 0
- Incremented it every time thread.start() is called
- Printed total context switches at end of simulation
- Committed with message "implemented context switch counter"

**Challenges**: there was a problem with the output found that i accidentally set contextSwitches to 9 instead of 0

**Solution**: Fixed it to start at 0

**Time spent**: 1h

---

### Entry 5 - [March 29]
**What I did**: Implemented Feature 3 / Waiting Time Tracking

**Details**: 
- Added createdTime and waitingTime fields to Process class
- Added getter and setter methods
- Calculated waiting time each time a process starts running
- Printed summary table at end showing all processes
- Committed with message "Feature 3: Added waiting time tracking and summary table"

**Challenges**: waiting times were showing large numbers like 3549593006209ms

**Solution**: i found out that getcreatedTime() was returning priority instead of createdTime fixed the return value

**Time spent**: 1.5 hours

---

## Summary

**Total time spent on assignment**: [Around 5 hours]

**Most challenging part**:  feature 3 (waitingtime) because it required understanding how to track time using System.currentTimeMillis() and there was some new methods that i had to learn

**Most interesting learning**: learning how threads work and how the cpu switches between processes  and implmenting some of it myself was very helpful

**What I would do differently next time**: start earlier and test each feature more carefully before moving to the next one

