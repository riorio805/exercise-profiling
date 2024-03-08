# what is this

i don't know

## Screen capture
### performance test with GUI
![](readme-images/highest-gpa-pre.png)
Results of performance testing for endpoint **'/highest-gpa'** using GUI

![](readme-images/all-student-name-pre.png)
Results of performance testing for endpoint **'/all-student-name'** using GUI

### performance test with command-line
![](readme-images/highest-gpa-pre-cli.png)
Results of performance testing for endpoint **'/highest-gpa'** using command-line

![](readme-images/all-student-name-pre-cli.png)
Results of performance testing for endpoint **'/all-student-name'** using command-line

### optimizing /all-student
![unoptimized-all-student.png](readme-images%2Funoptimized-all-student.png)
Tests performed before optimization.
Average CPU time is ~8 seconds.

![optimized-all-student.png](readme-images%2Foptimized-all-student.png)
Tests performed after optimization.
Average CPU time is ~1.6 seconds.

![before-after-all-student.png](readme-images%2Fspeed-diff-all-student.png)
Sample comparison of before optimization and after optimization,
which shows an **~81% reduction** in CPU time (8.5s -> 1.6s).
Optimized by querying the student_courses table directly (get all) 
instead of finding by every student id.

### optimizing /highest-gpa
![unoptimized-highest-gpa.png](readme-images%2Funoptimized-highest-gpa.png)
Tests performed before optimization.
Average CPU time is ~170 milliseconds.

![optimized-highest-gpa.png](readme-images%2Foptimized-highest-gpa.png)
Tests performed before optimization.
Average CPU time is ~48 milliseconds.

![speed-diff-highest-gpa.png](readme-images%2Fspeed-diff-highest-gpa.png)
Sample comparison of before optimization and after optimization,
which shows an **~73% reduction** in CPU time (180ms -> 48ms).
Optimized by using a better query which automatically
returns all students with the highest gpa.

### optimizing /all-student-name
![speed-diff-all-student-names.png](readme-images%2Fspeed-diff-all-student-names.png)
Sample comparison of before optimization and after optimization,
which shows an **~78% reduction** in CPU time (784ms -> 169ms).
Optimized by using StringBuilder instead of String, which
is mutable so faster writes.

### Conlusion
i have no idea

## Reflection 1
ans:
- What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?
> lorem ipsum dolor
- How does the profiling process help you in identifying and understanding the weak points in your application?
> sit amet consectetur
- Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
> adipiscing elit sed
- What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?
> do eiusmod tempor
- What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?
> incididunt ut labore
- How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?
> et dolore magna aliqua
- What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?
> Ut enim ad minim



## Checklist
- [x] Commit your source code into your main branch in your repository
- [x] Create 2 other test plan for endpoints /all-student-name and /highest-gpa. Perform performance testing as has been done above. Take a screenshot of the results and place it in the README.md file
- [x] Run both test plans that you have previously created (for endpoint /highest-gpa and /all-student-name) using the command line, take a screenshot of the results, and include them in the README.md file.
- [x] Refactor that code to achieve better performance. Commit in a new branch named “optimize”. Create representative commit messages. Do not use commit messages like "OK", "Cool", "Great", but instead create commit messages like "[Refactoring] - Optimizing method getAllStudentWithCourse".
- [ ] Perform the profiling process and optimizing the code for others endpoint (/all-student-name and /highest-gpa). Also achieve a 20% performance improvement for both of those endpoints. Commit in “optimize” branch also create representative commit messages. Do not use commit messages like "OK", "Cool", "Great", but instead create commit messages like "[Refactoring] - Optimizing method getAllStudentWithCourse".
- [ ] After the profiling and performance optimization process is completed, perform a performance test again using JMeter, see the results, and compare with the first measurement. Is there an improvement from JMeter measurements? Write your conclusion in the README.md file.


