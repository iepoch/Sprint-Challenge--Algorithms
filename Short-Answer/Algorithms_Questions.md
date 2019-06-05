# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0   # This here is O(1) because we are only doing 1 thing here
    while (a < n * n * n):  # This is a loop which some loops will be O(n)
      a = a + n * n   # this is going to be just 1 so it would stay O(1)

      # So now this should be O(n)  =  O(1) + O(n) * O(1)
```

```
b)  sum = 0 # This here is O(1) because we are only doing 1 thing here
    for i in range(n): # This is again we are calculating the O(n)
      i += 1  # Again we are only doing 1 thing so O(1)
      for j in range(i + 1, n): # This is again we are calculating the O(n)
        j += 1 # Again we are only doing 1 thing so O(1)
        for k in range(j + 1, n): # This is again we are calculating the O(n)
          k += 1 # Again we are only doing 1 thing so O(1)
          for l in range(k + 1, 10 + k): # This one did throw me off but it has no n
            l += 1# Again we are only doing 1 thing so O(1)
            sum += 1 # Again we are only doing 1 thing so O(1)

            # This breaks down to O(1) + O(n) * O(1) + O(n) * O(1) + O(n) * O(1) + O(n) * O(1) * O(1)
            # If we drop coefficients then O(n) + O(n) + O(n) = O(n**3)
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
      # This one is a recursive call that means the first function being called is consider O(n)
```

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

```
For this we could start to see how large the building is by getting the length. Then we can find the mid point.
Once we have the mid point we can then determine higher then the mid point of the building or lower then the mid point of the building.
This will allow us to know if we are on a higher floor or lower floor. We can then throw an egg and check to see if we are on a higher floor or lower floor and if it's on a higher floor then we know it broken. If its on a lower floor we know its not broken. But because I know what is high floor and low floor now that I have setup recursively this should reduce the broken eggs.

This would be a O(n) strategy


```
