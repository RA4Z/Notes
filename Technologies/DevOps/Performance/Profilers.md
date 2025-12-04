Software tools used in [[Performance Measurement]] to analyze the execution of a program and identify where the time is being spent

The Profiler primary function is to gather statistics about the program's resource utilization during runtime, usually involves tracking:
- **Execution Time (CPU Usage):** How much time is spent executing specific functions, methods or lines of code
- **Memory Allocation:** How much memory is being requested and held by different parts of the program
- **Call Frequency:** How many times a specific function is invoked
- **[[I & O|I/O]] Operations:** Time spent waiting for disk access, network transfers or database interactions

A profiler typically generates a report or visualization highlighting critical performance statistics, including:

| Metric | Description | Importance |
| :--- | :--- | :--- |
| **Inclusive Time** | The total time spent within a function *including* the time spent in all functions it calls. | Shows the overall cost of initiating a function chain. |
| **Exclusive Time** | The time spent executing *only* the code lines within a function itself, excluding time spent in called functions. | Identifies inefficient code directly within that function. |
| **Call Graph/Call Stack** | A visualization of the relationship between functions (who called whom). | Helps trace the path from the program start to the bottleneck. |
| **Hot Spots** | The specific functions or code lines that consume the most CPU time (usually presented as a ranked list). | Directs the developer to where optimization efforts should begin. |
| **Wait Time** | The time a thread spends waiting for locks, I/O completion, or other resources. | Essential for optimizing concurrent and distributed systems. |
| **Memory Leaks** | Identification of objects that are allocated but never properly released, leading to continuous memory consumption. | Critical for long-running applications. |