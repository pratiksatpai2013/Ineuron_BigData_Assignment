Q1. Why do we call Python as a general purpose and high-level programming language?
Ans1. Python is called general purpose because it can used to design and develop a wide variety of applications, across multiple domain. High-level programming language means it's more user-friendly.

Q2. Why is Python called a dynamically typed language?
Ans2. Dynamically typed language means that variables are checked against types only when the program is executing. We don't need to declare the variable type, the interpreter automatically interprets it.

Q3. List some pros and cons of Python programming language?

Ans3.
Pros:
  - Easy to use
  - Easy to integrate
  - High library support
  Cons:
  - Slow speed of execution compared to C,C++


Q4. In what all domains can we use Python?

Ans4.
- Graphic design, image processing applications, Games
- Web frameworks and applications
- Language Development
- Prototyping
- Software Development
- Data Science and Machine Learning
- Scripting

Q5. What are variable and how can we declare them?

Ans5. A variable is a symbolic name that is a reference or pointer to an object.
```python
var = 17  #Example
```

Q6. How can we take an input from the user in Python?

Ans6. using input()

Q7. What is the default datatype of the value that has been taken as an input using input() function?
Ans7. string datatype

Q8. What is type casting?
Ans8. Type casting means changing the datatype of the variable.

Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?
Ans9. Yes.
```python
x = [int(x) for x in input("Enter multiple value: ").split(",")]
print("Number of list is: ", x)
```
Q10. What are keywords?
Ans10. Keywords in Python are reserved words that can not be used as a variable name, function name, or any other identifier.

Q11. Can we use keywords as a variable? Support your answer with reason.
Ans11. Yes we can but there is a risk of overriding the keyword.

Q12. What is indentation? What's the use of indentaion in Python?
Ans12. Indentation is the whitespace used in Python. Indentation is used to create blocks of executable code in python.

Q13. How can we throw some output in Python?
Ans13. print()

Q14. What are operators in Python?
Ans14. Symbols or keywords used to perform certain operations on values or variable are known as operators.
- Arithmetic operators
- Comparison Operators
- Logical Operators
- Bitwise Operators
- Assignment Operators


Q15. What is difference between / and // operators?
Ans15. / is used for float division and // is used of floor (integer) division.

Q16. Write a code that gives following as an output.
```
iNeuroniNeuroniNeuroniNeuron
```
Ans16.
```python
"iNeuron"*3
```
or
```python
"iNeuron"+"iNeuron"+"iNeuron"
```

Q17. Write a code to take a number as an input from the user and check if the number is odd or even.
Ans17.
```python
num = input("Enter a number: ")
num = int(num)
if num%2 == 0:
  print(f"{num} is even")
else:
  print(f"{num} is odd")
```

Q18. What are boolean operator?
Ans18. 'True , False , not , and , or' are the only built-in Python Boolean operators.

Q19. What will the output of the following?
```python
1 or 0

0 and 0

True and False and True

1 or 0 or 0
```
Ans.19 Output of the following code will be
```python
1 or 0 -> 1
0 and 0 -> 0
True and False and True -> False
1 or 0 or 0 -> 1
```

Q20. What are conditional statements in Python?
Ans20. Conditional statements are used we want to execute some set of statements only if the given condition is satisfied, and a different set of statements when it’s not satisfied.


Q21. What is use of 'if', 'elif' and 'else' keywords?
ns21. if is the first condition check for the condition.

if "if" is False then elif's condition is checked.

else is checked when all the upper condition fails.


Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".
Ans22.
```python
age = int(input("Enter you age: "))
if age >= 18:
    print("I can vote")
else:
    print("I can't vote")
```

Q23. Write a code that displays the sum of all the even numbers from the given list.
```python
numbers = [12, 75, 150, 180, 145, 525, 50]
```
Ans23.
```python
numbers = [12, 75, 150, 180, 145, 525, 50]
add = 0
for i in numbers:
  if i%2 == 0:
    add = add+i
  else:
    pass
print(add)
```

Q24. Write a code to take 3 numbers as an input from the user and display the greatest no as output.
Ans24.
```python
x, y, z = input("Enter 3 numbers seprated by comma: ").split(",")
if int(x) > int(y) and int(x) > int(z):
  print(f"{x} is greatest")
elif int(y) > int(z):
  print(f"{y} is greatest")
else:
  print(f"{z} is greatest")

```



Q25. Write a program to display only those numbers from a list that satisfy the following conditions

- The number must be divisible by five

- If the number is greater than 150, then skip it and move to the next number

- If the number is greater than 500, then stop the loop
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
Ans25.
```python
numbers = [12, 75, 150, 180, 145, 525, 50]
list = []
for num in numbers:
  if num > 150:
    if num > 500:
      break
  elif num%5==0:
    list.append(num)
print(list)
