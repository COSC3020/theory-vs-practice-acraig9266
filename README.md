I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
No sources were used.
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  - Asymptotic analysis finds a complexity that applies for all values >= n<sub>0</sub> so it doesn't tell us anything about time complexity for input sizes less than n<sub>0</sub>.
  - Asymptotic analysis does not account for the speed of the system running an algorithm.
  - Algorithms that run in 28n + 1 and 2n + 1 both are written as O(n) or θ(n) and would be expected to have similar work and runtime at a glance even though one is roughly 14 times more complex than the other.


- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  $log{n}$ to find in a binary tree
  
  $T(1,000)$ = $log{_2}{1000}$ = 3 / $log{2}$
  
  $T(10,000)$ = $log{_2}{10000}$ = 4 / $log{2}$

  $T(10000) / T(1000)$ = (4 / $log{2}$) / (3 / $log{2}$) = 4/3
  4/3 * 5 seconds = 6.66666 seconds

  I'd expect it to run in about 6.6666 seconds with 10,000 elements because it should be the original time by the ratio of T(10000) and T(1000).
  

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  - The search is poorly implemented and has a higher complexity than log(n) like it should be.
  - Data used could've been generated differently where the small run had mostly or all integers which compare more quickly while the larger run had more or all strings which are compared much more slowly.
  - The computer had other intensive operations during the run with 10,000 elements so it had limited access to cpu resources resulting in longer execution time.
