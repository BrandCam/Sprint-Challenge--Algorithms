# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```
this code has a complexity of O(n), because n^2 will have to added to itself n times to equal n^3.
The code will add n^2 to 0 then procede to add n^2 to the accumulated number untill the value is not less than n^3.
```
b)  sum = 0
    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1
```
I'm not for sure what the complexity is, but I do know that as n grows so does the number of times that each loop must run. my brain isnt working enough to figure out the rate of growth though....
```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```
I think this is O(n), because I think the function will run recursively n times and will look something
like this bunnyEars(n-1) + bunnyEars(n-2) + bunnyEars(n-3) ......+ bunnyEars(n-n). 
## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

The first solution that comes to mind would be. first drop the egg from the top floor if it dosent break then f must be equal to or greater than n so n would be our best guess. next if the egg breaks from the top move to the middle and drop the egg. if the egg breaks go to the middle of the last tested floor and the ground floor. if the egg stays whole move to the middle of the last droped floor and the top floor. repeat these steps till you find the magic floor f replacing the bottom and top floors with the closest tested floors up or down .