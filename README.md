# JMeter GUI Test Plan Results (Before Optimization)

## 1. `/all-students` endpoint:

![All Students Test Results](/assets/images/testplan1.png)

## 2. `/all-student-name` endpoint:

![All Student Name Test Results](/assets/images/testplan2.png)

## 3. `/highest-gpa` endpoint:

![All Student Name Test Results](/assets/images/testplan3.png)


# JMeter CLI Test Plan Results (Before Optimization)

## 1. `/all-students` endpoint:

![All Students Test Results](/assets/images/testplan1nongui.png)

## 2. `/all-student-name` endpoint:

![All Student Name Test Results](/assets/images/testplan2nongui.png)

## 3. `/highest-gpa` endpoint:

![All Student Name Test Results](/assets/images/testplan3nongui.png)

# JMeter GUI Test Plan Results (After Optimization)

## 1. `/all-students` endpoint:

![All Students Test Results](/assets/images/testplan1after.png)

## 2. `/all-student-name` endpoint:

![All Student Name Test Results](/assets/images/testplan2after.png)

## 3. `/highest-gpa` endpoint:

![All Student Name Test Results](/assets/images/testplan3after.png)

# JMeter CLI Test Plan Results (After Optimization)

## 1. `/all-students` endpoint:

![All Students Test Results](/assets/images/testplan1cliafter.png)

## 2. `/all-student-name` endpoint:

![All Student Name Test Results](/assets/images/testplan2cliafter.png)

## 3. `/highest-gpa` endpoint:

![All Student Name Test Results](/assets/images/testplan3cliafter.png)

# Conclusion
After completed the profiling and performance optimization, there is an significant improvement across all endpoints:

1. `/all-student` endpoint:
    - Before Optimization: ~49,000 - 50,000 ms
    - After Optimization: ~4,100 - 4,600 ms
    - Improvement: ~90.8% reduction in execution time

2. `/all-student-name` endpoint:
    - Before Optimization: ~4,300 - 5,200 ms
    - After Optimization: ~100 - 200 ms
    - Improvement: ~95.3% reduction in execution time

3. `/highest-gpa` endpoint:
    - Before Optimization: ~57 - 86 ms
    - After Optimization: ~11 - 37 ms
    - Improvement: ~80.7% reduction in execution time 

The performance optimizations significantly improved execution times across all endpoints, reducing delays and enhancing efficiency. These improvements not only make the system more responsive but also optimize resource usage, allowing it to handle higher loads effectively. This highlights the importance of continuous profiling and tuning to maintain a scalable and high-performing application.

# Reflection
1. **What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?** <br><br>

    JMeter is primarily used for load testing, simulating multiple concurrent users to measure an application’s response time, throughput, and overall performance under different loads. It helps identify performance bottlenecks at a high level, such as slow response times due to database queries or inefficient API calls.
    On the other hand, IntelliJ Profiler provides in-depth insights into the application's internal behavior, including CPU usage, memory consumption, and method execution times. It helps pinpoint specific functions or code segments that contribute to performance issues. While JMeter focuses on external performance metrics, IntelliJ Profiler helps diagnose and optimize internal code inefficiencies. <br><br>

2. **How does the profiling process help you in identifying and understanding the weak points in your application?** <br><br>

   Profiling helps by providing a detailed analysis of where the most time is spent during execution. By identifying methods with high CPU usage, memory leaks, or excessive object allocations, it allows me to focus optimization efforts on specific problem areas rather than guessing. It also highlights redundant computations and inefficient loops, enabling targeted performance improvements. <br><br>
3. **Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?** <br><br>

   Yes, IntelliJ Profiler is effective because it provides real-time insights into method execution times, CPU usage, and memory allocation. It offers call graphs and flame charts, making it easier to visualize performance bottlenecks. Additionally, its ability to analyze thread behavior helps in identifying concurrency-related issues. However, interpreting profiler data requires experience, and combining it with performance testing tools like JMeter gives a more complete picture. <br><br>
4. **What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?**
   - **Interpreting profiler results**: Profiling generates a large amount of data, and understanding which metrics are relevant can be challenging. To overcome this, I focus on key performance indicators such as execution time, memory usage, and CPU load.
   - **Replicating real-world scenarios**: JMeter tests need to simulate realistic user behavior, which requires fine-tuning test configurations. I use actual traffic data or expected load patterns to ensure realistic testing.
   - **Ensuring optimizations do not introduce bugs**: Performance optimizations sometimes change application behavior. To mitigate this, I conduct thorough regression testing after making changes.
   - **Inconsistent profiling results**: External factors such as system load and JVM optimizations can affect profiling results. Running multiple profiling sessions and averaging results helps in achieving more reliable conclusions. <br> <br>
5. **What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?** <br><br>

   - **Granular insights into performance bottlenecks: It allows pinpointing slow methods, expensive database queries, and excessive memory usage.
   - **Visual representation of execution flow**: Call trees and flame graphs make it easier to identify hotspots.
   - **Thread analysis**: Helps detect concurrency issues, such as deadlocks or thread contention.
   - **Integration with IntelliJ IDEA**: Seamless integration makes it convenient to analyze and debug performance issues without switching tools.
   - **Real-time monitoring**: Allows observing performance trends while the application is running. <br><br>

6. **How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?** <br><br>

   In such cases, I analyze the discrepancies by considering factors such as differences in test conditions, JVM optimizations, and background processes. I run multiple tests under controlled environments to ensure consistency. Additionally, I cross-check findings by using other profiling tools or logging execution times within the application code. If necessary, I adjust JMeter scenarios to better reflect real-world conditions. <br><br>

7. **What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?** <br><br>

    I enhance code efficiency by refactoring inefficient loops, eliminating redundant computations, and optimizing database queries for better performance.
    

