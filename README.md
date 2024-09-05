# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
- Asymptotic analysis finds a bound that applies for all values >= n so it may be faster or slower than stated when at input sizes of < n.
- Certain operations may be constant time and ignored in asymptotic analysis when the operations take a long time relative to many other operations in practice.
- 
  

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  $log{n}$ to find in a binary tree
  $T(1,000)$ = $log{_2}{1000}$ = 3/$log{2}$
  $T(10,000)$ = $log{_2}{10000}$ = 4/$log{2}$

  

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.
