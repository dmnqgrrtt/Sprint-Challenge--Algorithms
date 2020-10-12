#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n): The number of computations is equal to the size of n. Since they both increase at the same rate then the algorithm is linear. The loop is based on n^3 but the conditional, a, is increasing by n^2


b) O(n^2): The for loop and the while loop are both dependant on the size on n. Each loop itself is O(n). Since the while loop is inside of the foor loop O(n) gets multiplied by O(n) giving us O(n^2).


c) O(n): This is a recursive function but each call is only calling itself once. So the number of functions ran will be equal to the number passed in and each funtion 

## Exercise II

# Set the top and bottom floors
Set the topFloor equal to n
Set bottomFloor equal to 1

# Halve the floors by starting the throw floor at the midpoint
Set the f to (topFloor - bottomFloor) // 2 

# Set a found floor variable equal to false since we havent found the correct floor yet
foundfloor = False

# create a while loop while the floor is not found
while not foundFloor:
    Throw the egg from floor f:
          If the eggs breaks:
              throw the egg from 1 floor beneath it (f - 1):
                    If the egg doesnt break:
                        set foundFloor equal to True
                    else (egg does break):
                        # We are too high, so split the bottom floors in half and set f equal to the midpoint
                        set f equal to (f - bottomFloor) // 2 
          else ( the egg doesnt break):
              throw the egg from 1 floor above ( f + 1 ):
                    If the egg breaks:
                        set f = f + 1
                        set foundFloor equal to True

                    else (the egg doesnt break):
                        # we are too low, so split the upper floors in hald and set f equal to the midpoint
                        f equals (topFloor - f) // 2

return f


