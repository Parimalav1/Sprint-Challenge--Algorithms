#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)The runtime for a while loop is O(n) though the input is (a < n * n * n) and O(1) for (a = a + n * n).
n ^ 3 = n * n ^ 2. So it takes n steps to get to n ^ 3.
The running time increases linearly or n times with the size of the input data. So  O(n) * O(1) =  O(n). 


b)```
sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```
The runtime for a for loop is O(n), for a while loop is O(n), for  (j *= 2) is O(1) and for (sum += 1) is O(1).
O(n) * O(log(n)) * O(1) * O(1) = O(nlog(n))


c)The runtime is O(n) because the function only includes one recursive call.

## Exercise II
Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

A strategy to determine the value of f such that the number of dropped + broken eggs is minimized.
n-story building
floor f or higher
floor less than floor f

1. The function takes input of n floors and x no of eggs
2. Find the midpoint of n-story building and check if an egg gets broken but not the highest floor as the egg breaks anyway when thrown.  
3. If egg breaks at midpoint, then update your midpoint by halving it. 
4. Else update midpoint by adding half of the range
5. Complexity is O(log(n)) this is basically binary search algorithm
