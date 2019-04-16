# implement List.indexOf

`while`-style and recursive implementations at the top of
OrderedList_inArraySlots.java

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

## 2.  Re-think about inverse functions and logarithms ##
count = log2n
Count is the exponent that when 2 is raised to gives n. 

## 3.  describe the recursive solution ##
0. Find the page in which the targeted name is on given a set of pages with lower bound xi and upper bound xf. 
1. The recursive abstraction can find the page in which the targeted name is on given a set of pages with lower bound xi and upper bound (xi + xf )/2 -1 , or lower bound (xi +xf)/2 +1 and upper bound xf.
2. Decision: Is the lower bound greater than the upper bound?
   Instructions for base case: The name does not exist in the book. Return -1
   Instructions for recursive abstraction: 
   Combining operator: null
   Leftover: Check if the name on the page is the targeted name
   Recursive abstraction: If the name on the page is greater than the targeted name, follow these instructions to find the page in which the targeted name is on given a set of pages with lower bound xi and upper bound (xi + xf )/2 -1.
   If the name on the page is less than the targeted name, find the page in which the targeted name is on given a set of pages with lower bound (xi +xf)/2 +1 and upper bound xf