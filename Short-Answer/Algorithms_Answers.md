Add your answers to the Algorithms exercises here.

## Exercise I

a ) 
```
a = 0                   # O(1)
while (a < n * n * n):  # O(n)
    a = a + n * n       # O(1)
```
while 0 < 2 * 2 * 2 (8)
a = 0 + 2 * 2 (4)
4 < 8
a = 4 + 2 * 2 (8)
8 !< 8

The runtime is O(n), or linear time because the number of additional operations the algorithm needs to perform grows in direct proportion to the increase in input size.


b )

n * n * n * n
```
sum = 0                                     # O(1)
for i in range(n):                          # O(n)
    i += 1                                  # O(1)
    for j in range(i + 1, n):               # O(n)
        j += 1                              # O(1)
        for k in range(j + 1, n):           # O(n)
            k += 1                          # O(1)
            for l in range(k + 1, 10 + k):  # O(n + 10)
                l += 1                      # O(1)
                sum += 1                    # O(1)
```
The runtime is O(n^4) because with all these nested loops, our outer loop runs n times, and then out inner loops run n times for each iteration of the outer loop. So we multiply each of the runtimes of all of the loops to get O(n^4), or Quadratic Time.


c )
```
def bunnyEars(bunnies):
    if bunnies == 0:
        return 0

        return 2 + bunnyEars(bunnies-1)
```
The runtime is O(n) because the recursion acts as if it's a loop. So it will run n times (or "bunnies" times) + 2, until bunnies reaches zero. Linear Time.

## Exercise II

        # I would loop through each floor in the building
        for each_floor in building:
        
            # and drop an egg
            
            # if the egg does not break
            if egg_breaks == false:
                
                # set the value of f equal to that floor, meaning it's still okay to drop eggs off this floor
                f = each_floor
                
            # If the egg does break
            elif egg_breaks == true:
                
                print(f"Sorry, {f} is the last floor you can drop eggs off before they start to break.")
                
                # Return the value of f
                return f
            
The runtime complexity of this solution would be O(n) at worst case. If we find that we only have to loop through the first 2 floors to get our f value, that would be great, but we might find that we have to loop through all the way to the top of the building (all the floors) before we get the value of f.
                
