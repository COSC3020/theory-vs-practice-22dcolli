[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.


1a) The first reason I can think of as to why the asymptotic analysis may be misleading with respect to actual performace is obviously hardware.
In many cases theory depends on the ideal conditions to any given experiment, but the one thing that varies most user to user in my mind is hardware.
Many people can run programs much faster if the hardware is better, a computer that that is 2 months old is almost assuredly faster than the 5 year old computer
with faster calculating compentents and a greater memory capacity.

1b) The second reason I can think of for the asymptotic analysis being misleading is simular to differences in hardware, but only now in your compiler and or coding language. What I mean by that
is that asymptotic analysis does not account for in any way, you can have the same process coded out in two different languages but differences in how those languages operate may effect the runtime and memory usage.
On that same tangent, if one algorithm has to work with multiplication of integers over and over, some compilers may use standard integers or floating point values depending on what it thinks is best. 
This might eventually lead to a different outcome than the asymptotic analysis may have indicated.

1c)The final reason that asymptotic analysis may be misleading is that it also does not account for the edge case data sets. On paper different sorting algorithms 
may have the same result with asymptotic analysis, but then different data sets may be favored more or less by each algorithm. For example,(using quicksort as an example because I'm more comfortable with it)
quicksort does very poorly with an already sorted list, not just poorly, it is generally considered it's worst scenario. On the other hand, insertion sort does really well with the already sorted list,
even though both quicksort and insertion sort are evaluated the same through asymptotic analysis.



2)We went over this particular problem in class I believe, and so I'll go through to the best of my understanding. We start by looking at the average complexity of any standard binary search tree($\theta(log_n$)). Using that knowledge
we are able to set up a system of equations, which would look like this $constant * log_2(1000 elements) = 5 seconds$, with this equation we find the constant to be around $.5$. Finally we plug that $.5$ into the equation with $10000$ elements which looks like
$.5 * log_2(10000 elements)$ which calculates out to a complexity of 6-7 seconds.



3a)One reason I can think of as to why the time would be so much greater relates back as to why aymptotic analysis may be misleading. My reason being that maybe you try to run the algorithm on a more simple device such as an arduino or a pi. These are very bare bones when it comes to computational power and memory, so while a full computer might follow the asymtotic analysis, 10000 items for a one of the more simple devices might be pushing what it is capabl of holding, or it may have to access and store the items differently when the number of items increases drastically.

3b)Another reason is something we learned in 2030, that being the tree you are using might be unbalance

3c)
