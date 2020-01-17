# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to a repository to complete the task. Remember to also submit your answers to Blackboard

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is when multiple tasks run in the same time period. Parallelism is when multiple tasks run at the same time, literally. Difference: in concurrency, the tasks share the resources, so that they can't run everything at the same time, but have to wait in order to run their subtasks. In parallelism, the tasks and their subtasks run at the same time, e.g. on a multi-core processor.
 
 ### Why have machines become increasingly multicore in the past decade?
 > To increase the efficiency of parallelism.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > When there are more tasks to run than individual processors, concurrency efficiently divides the processor or computing resources to the different subtasks, so that all the tasks can be run almost at the same time. 
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > Harder, more thing to consider
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Process: a series of actions or steps taken in order to achieve a particular end
 Threads: a component of a process, the smallest sequence of programmed instructions that can be managed independently by a scheduler
 Green threads: "User-level threads", scheduled by an "ordinary" user-level process, not by the kernel. Can be used to simulate multi-threading on platforms that don't provide that capability.
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > `pthread_create()` : creates a thread
 `threading.Thread()` : creates a thread
 `go` : creates a green thread
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > It makes sure only one thread can execute at a time
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Multiprocessing
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > Max number of CPUs that can be executing simultaneously 
