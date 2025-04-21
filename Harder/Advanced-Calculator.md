# 12.6 Advanced Calculator

## The task
Create a calculator. That will be able to take user input of an math operation and perform it.

But it would be a little advanced from other python calculator projects those you usually see. 

It will take the calculation directly from the user and then perform it, without asking user to choose operation type( addition, multiplication etc.). 

## Solution strategy
Create a bunch of functions to perform add, subtract, multiply, division or modulo. 

Then take the calculation from the user. 

As the calculator can perform only two number's calculations, you can use the built in ``split()`` method to make the input a list containing three elements.

The input list's first element would be the first number, second element the operator( +,*,/,-,%) and last one the second number.

Then put the numbers in separate variables and call the appropriate function based on the operator.

> The `split()` method is a built in function in python, which splits a string into a list where the string has a space.
> Exmp: split("2 + 3") will return ["2","+","3"] as result.

Think for a few minutes and try it yourself first.

## The solution
```python
def add(num1, num2):
 return num1 + num2
 
def subtract(num1, num2):
 return num1 - num2
 
def multiply(num1, num2):
 return num1 * num2
 
def divide(num1, num2):
 return num1 / num2
 
def modulo(num1, num2):
 return num1 % num2

# Inform user that each element in the input should be separated by space.
print("Give space among the numbers and operator, like: 24 - 5 ")

# Take input from the user
calc = input("Enter your calculation: ")
calclist = calc.split()
num1 = int(calclist[0])
operation = calclist[1]
num2 = int(calclist[2])

 
result = 0
if operation == '+':
 result = add(num1,num2)
elif operation == '-':
 result = subtract(num1,num2)
elif operation == '*':
 result = multiply(num1,num2)
elif operation == '/':
 result = divide(num1,num2)
elif operation == '%':
 result = modulo(num1,num2)
else:
 print("Please enter: +, -, *, / or %")
 
print(num1, operation, num2, '=', result)
```
**[Try it on Programming Hero](https://play.google.com/store/apps/details?id=com.learnprogramming.codecamp)**


## How it works
You saw five functions to add, subtracts, etc. Those are easy.

Then we are taking user input. Then using `split()` we are splitting that and getting two numbers and the operator.

Then we have if-elif-else, based on the operation, we call the right method to perform the task.

That’s it. 


&nbsp;
[![Next Page](../assets/next-button.png)](Password-generator.md)
&nbsp;

tags:  `programming-hero`  `python`  `python3`  `problem-solving`  `programming`  `coding-challenge`  `interview`  `learn-python`  `python-tutorial`  `programming-exercises`  `programming-challenges`  `programming-fundamentals`  `programming-contest`  `python-coding-challenges`  `python-problem-solving`
