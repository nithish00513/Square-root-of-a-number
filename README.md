# Find the square root of a number

## AIM:
To write a program to find the square root of a number.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Define a function.
2. Assign number_iters = 100 in the function to perform 100 iteratios.
3. Set i = 0.
4. Calculate  number = 0.5 * (number + a / number) for 100 iterations.
5. Return number

## Program:
def newton_sqrt(number, tolerance=1e-7):
   
    
    if number < 0:
        raise ValueError("Cannot compute square root of a negative number.")

   
    x = number if number >= 1 else 1

    while True:
        next_x = 0.5 * (x + number / x)
        if abs(next_x - x) < tolerance: 
            return next_x
        x = next_x


try:
    num = float(input(""))
    sqrt_result = newton_sqrt(num)
    if(sqrt_result>3):
        print("Square root of the number:",sqrt_result)
    else:
        print("Square root of the number: %.1f"%sqrt_result)
except ValueError as e:
    print(e)

## Output:
![alt text](<Screenshot 2024-12-07 185550.png>)




## Result:
Thus the program to find the square root for the given number(newton's method) using function is written and verified using python programming.
