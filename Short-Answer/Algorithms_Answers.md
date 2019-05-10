Add your answers to the Algorithms exercises here.

```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```

## Answer (a)

The time complexity = O(n) because the while loop creates a linear growth of operation of ratio 1:1 based off of the input of _n_. A negative _n_ value will create an infinite loop, while a positive _n_ value will run based on the size of n.

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

## Answer (b)

With a runtume of approximately O(n) there seem to be four nested for-loops with one of them being a constant as it will always iterate over ten times no matter how large k gets which can be dropped from the runtime. Therefore the nested _n_ growth is multiplied by that number of times which gives O(n^3)

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Answer (c)

O(n) Linear runtime as bunnies will run the number of times _n_ is equal to.

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

##Answer exercise II

-- Start by implimenting a binary search algorithm
-- Starting at the middle of the building drop the egg,
-- If it does break we move down half again, repeatedly until it doesnt break.
If it doesnt break, we move up by half until it does to find _f_
