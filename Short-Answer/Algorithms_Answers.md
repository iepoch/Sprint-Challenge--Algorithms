Add your answers to the Algorithms exercises here.

```
Answer here is = O(n)
a)  a = 0      # O(1)
    while (a < n * n * n): # O(n^3 )
      a = a + n * n    # O(n^2)

      # The n's will be dropped and you will be left with just O(n)
```

```
Answer here is = O(n^3)

b)  sum = 0    # O(1)  This is only doing one thing
    for i in range(n):  #O(n) Loops always start as a O(n)
      i += 1            # O(1) We are only doing one thing here as well
      for j in range(i + 1, n): # O(n) Looping again stays O(n)
        j += 1                  # 0(1)  This is only doing one thing
        for k in range(j + 1, n): # O(n)Looping again stays O(n)
          k += 1                  # 0(1) We are only doing one thing here as well
          for l in range(k + 1, 10 + k): # O(10) Because we are not using K we use the 10 which will become 1 after droping 0
            l += 1                       # O(1)   We are only doing one thing here as well
            sum += 11                     # O(1) We are only doing one thing here as well

    # 0(1) + ( 0(n) *(0(1) + (O(n) * (0(1) +( O(n) * (0(1) + 0(10)) )
    # O(n) * O(n) * O(n)
```

```
# Answer here is = 0(n)

c)  def bunnyEars(bunnies): O(n)
      if bunnies == 0: # 0(1)
        return 0       # 0 (1)

      return 2 + bunnyEars(bunnies-1) # 0(n)

      # We drop 1st n Recursion is always at its best 0(n) for the first call it will get larger as it grows
```

## Exercise II

```
    My first initial was With Linear Search

            for i in range(floor):
                if floor < floor_egg_broke:
                    return 1 # or we could return True If the egg didn't break
                else:
                return -1  # and we could return False or if the egg did break

With Linear Search you can get a run time at worst O(n)


However if wanted to be better with this we can get of runtime of 0(log n) using Binary Search like so
            floors = [ 0,1,2,3,4,5,6]

            def boken_eggs(floors, target):

                we need to get the length to know how may floors there are
                  So we need to get the base case which is ground 0
                    if len(floors) == 0:
                        return -1  # empty array

                    low = 0  We know that we will always start at ground 0
                    upper = len(floors) - 1 We know we will travel down

                    so now while len(floors) is equal or greater than 1
                    we will find our midpoint
                        mid = (upper - low) // 2

                        And if our floors[mid] is equal to our target:
                            then we know we are in the middle and the egg will not break
                        But if our floors[mid] is greater then the upper floor then eggs will break
                        Otherwise  anything lower will not break any eggs

```
