I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
- Asymptotic analysis finds a bound that applies for all values >= n so it doesn't tell us anything about complexity for input sizes less than n (unless using little o or little omega).
- Certain operations may be constant time and ignored in asymptotic analysis when the operations take a long time relative to many other operations in practice.
- The bounds can be very large in asymptotic analysis so two algorithms could be ∈ $theta$(n) but one could be 2n + 1 complexity while the other is 28n + 50 but in the notation they appear to be the same performance.


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
- The array size of 1000 was less than the lower bound on the theoretical time complexity so it shouldn't be applied.
- The larger array contained strings while the small array contained integers which are compared more quickly
- The computer had other intensive operations during the run with 10,000 elements so it had limited access to cpu resources resulting in longer execution time

Add your answers to this markdown file.
