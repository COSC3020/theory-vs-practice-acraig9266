I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
- Asymptotic analysis finds a bound that applies for all values >= n so it may be faster or slower than stated when at input sizes of < n.
- Certain operations may be constant time and ignored in asymptotic analysis when the operations take a long time relative to many other operations in practice.
- Best case or worst case scenarios may be very commmon so looking at average case may be drastically different from what happens most often.
  

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
- The array was unsorted with the element in the worst possible index to find
- There was a setTimeout call made with a delay set to about 93.33333 seconds.

Add your answers to this markdown file.
