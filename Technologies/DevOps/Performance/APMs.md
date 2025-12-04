Application Performance Monitoring (APM) is a set of practices, tools and processes designed to **measure, analyze and optimize the performance and availability of software applications**.

In simpler terms, APM helps you answer the questions: **"Is my application running well?"** and **"If not, why not?"**

### Possibilities with APMs
- 1. **Transaction Tracing:** Tracks a single request, for example a user clicking a button, as it moves across various components of the system (web server, application code, database calls, external services). It's used to identify the part of the code or infrastructure that is causing latency or errors for a specific user action.

- 2. **Application Code Monitoring:** Instruments the application code to monitor metrics like method execution times, garbage collection frequency, memory usage, and CPU utilization *within* the application process

- 3. **User Experience Monitoring / Real User Monitoring:** Measures the performance metrics experienced directly by the end-user in their browser or mobile device. Examples are Page Load Time (PLT), First Contentful Paint (FCP), Time to Interactive (TTI) and tracking of JavaScript errors.

- 4. **Database Performance Monitoring:** Monitors database interactions, specifically tracking slow queries, connection pool issues, query execution plans and overall database resource usage

- 5. **Infrastructure Monitoring:** Tracks the health and utilization of the foundational components that host the application, like CPU load, memory utilization, disk [[I & O|I/O]] and network throughput.

### Summary of Key APM Metrics

| Area               | Metric                            | What it Measures                                           |
| :----------------- | :-------------------------------- | :--------------------------------------------------------- |
| **Throughput**     | Requests per Minute (RPM)         | Application load and capacity.                             |
| **Latency**        | Average/P95/P99 Response Time     | How quickly the application responds to user actions.      |
| **Errors**         | Error Rate (e.g., HTTP 5xx codes) | The frequency of application failures.                     |
| **Code**           | Garbage Collection Time           | The efficiency of memory management (critical in Java/Go). |
| **Database**       | Query Execution Time              | The time spent waiting for database responses.             |
| **RUM/UEM**        | Page Load Time, Core Web Vitals   | The performance as experienced by the user's browser.      |
| **Infrastructure** | CPU Utilization, Memory Usage     | Resource availability and bottlenecks on hosts/containers. |