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

---

Answers:

#### Question 1

- Constants are neglected in the final complexities of algorithms, and sometimes they mattein practice, because we aren't actually working with infinitely large input sizes. For example, the average and worst case of Insertion sort are both $\Theta(n^2)$, but thaverage case is really half that. That can matter in certain situations.
- Similar to above, asymptotic analysis only takes into account input sizes that arreaching infinity, but there are a lot of times where the input is fairly small, and thasymptotic behavior would lead you away from using that particular algorithm.
- In the case of recursive algorithms, like heap sort or merge sort, there could bsituations where you run into stack constraints when input sizes grow too large. In generalthere are real-life constraints that can exist that would make asymptotic analysis misleading when it comes to picking an algorithm to approach a problem.

#### Question 2

I would say that given that the computer is processing at the same rate, the process should take about 7 seconds. At least, when considering that the average time to reach a leaf in a balanced n-ary tree is in the logarithmic realm, the expression would be $plog_2(10000)$, where _p_ is the average time it took the computer to do an operation in the last search (about 0.5017 seconds in this case).

#### 3

1. Both the average and best case time complexities of searching a binary search tree are $\Theta(log(n))$. Considering this, the tree must have been fairly skewed one way or another, to a point where the traversal was similar to that of a linked list.
2. A physical, more real-world, type of problem could be lack of necessary memory to handle a massive tree and the recursive steps might have gotten out of hand. Although $log_2(10000) = 13.2877...$, so maybe the RAM was not very accessible at the time.
3. An extension of 2: maybe the computer that was performing the search of the tree was also carrying out a multitude of other processes at the same time, therefore limiting the ability to handle a large input size efficiently.

---

**I certify that I have listed all sources used to complete this exercise, including the use
of any Large Language Models. All of the work is my own, except where stated
otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is
suspected, charges may be filed against me without prior notice.**
