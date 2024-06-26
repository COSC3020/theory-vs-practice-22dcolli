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
with faster calculating compentents and a greater memory capacity. The hardware itself might be a constant factor when looking at the complexity, but calculating that assumes that the constant hardware is the ideal hardware, and not in fact hardware that might perform as ideally as we expect in the actual world.

1b) The second reason I can think of for the asymptotic analysis being misleading has to do with the lower order terms rather than looking at the constants(see 1c) is the lower order terms. for example, in calculating complexity we could, for the sake of an example, have the statement $n^3+n^7\in\Theta(n^7)$ be true. But when we look at $n^3$ and $n^7$ we know logically that those are two very different numbers, an exponentially different value.

1c)The final reason(revised) is that during asymptotic analysis certain things are ignored to a certain extent that will absolutely affect actual performance. For example, early on we were informed that the constants are dropped when trying to find the time complexity.
Those constants could be anything from 1 to 10000, through this example, it can be seen that the runtime might be drastically different in actual practice even though on paper it may look the same even with the initial differing constants. When the dataset becomes large enough these constants do not have a high impact on the runtime which is why we ignore them in the first place, but on smaller datasets that difference is more easily noticed.



2)We went over this particular problem in class I believe, and so I'll go through to the best of my understanding. We start by looking at the average complexity of any standard binary search tree($\theta(log_n$)). Using that knowledge
we are able to set up a system of equations, which would look like this $constant * log_2(1000 elements) = 5 seconds$, with this equation we find the constant to be around $.5$. Finally we plug that $.5$ into the equation with $10000$ elements which looks like
$.5 * log_2(10000 elements)$ which calculates out to a complexity of 6-7 seconds.



3a)One reason I can think of as to why the time would be so much greater relates back as to why aymptotic analysis may be misleading. My reason being that maybe you try to run the algorithm on a more simple device such as an arduino or a pi. These are very bare bones when it comes to computational power and memory, so while a full computer might follow the asymtotic analysis, 10000 items for a one of the more simple devices might be pushing what it is capabl of holding, or it may have to access and store the items differently when the number of items increases drastically.In better terms though, even if the calculated asymptotic complexity for runtine may be the same between 10000 and 1000 elements, if the hardware is slower, then the expected result is not what actually happens,the result is skewed. If the hardware is old enough, it might just run out of memory before it can actually get through all elements.

3b)Another reason is something we learned in 2030, that being the tree you are using might be unbalanced. The tree being unbalanced would lead to navigation of said tree being less efficient than it could be, meaning that it would take more time than expected based off of asymtotic analysis alone. I do believe that this can account for such a large difference in time, for example, a badly balanced tree, and I mean a really unbalanced tree is more akin to a linked list. In that case you might be having to go through every single item searching for the correct one. Even if your computational device is highly advanced, that would still take much more time in the end.In addition the reason why it took way longer than expected in this scenario is that the search tree changed when increased to 10000. What I mean by this is that in this scenario lets say that the desired item is on a relatively high level for the 1000 item search, but then the tree has to be expanded for the 10000 items. Depending on the items that were added the position of the desired item might have shifted. Essentially the search could have possibly turned from the ideal or average case to the worst possible case with the 10000 items intead of the 1000, which could explain the large jump in time the second time using binary search. So in the end neither reason alone is enough to account for the increase in time but both together could account for such a drastic increase in time.

3c)My final reason for why the complexity may suggest a different time is with the testing itself. We made no extra assumptions with this problem, and with that same process we can't assume whoever was testing the search was using the same inputs for both. In many cases you may use a pre-determined method for testing, this means that if you have a method that tests by randomly generating 1000 elements to test 1000 elements, if you do that twice it wont have the same 1000 elements. This goes for the 1000 to 10000 elements as well. There is a large possibility in that testing 10000 elements the test method happened to randomly select a bad data set or a data set that works very poorly with larger scale implementation. 
