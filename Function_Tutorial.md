# Girl Scout - Coding for Good
**Creating Function Using Numpy Tutorial**


```python
import numpy
```

## Introduction to Function


```python
#Create the function
def happyBirthday(name): #program does nothing as written
    print("Happy Birthday to you!")
    print("Happy Birthday to you!")
    print("Happy Birthday, dear",name+".")
    print("Happy Birthday to you!")
    
#Create an input variable
your_name = "Abcd"

#Test the function
happyBirthday(your_name)    
```

    Happy Birthday to you!
    Happy Birthday to you!
    Happy Birthday, dear Abcd.
    Happy Birthday to you!



```python
#Create an empty function (function that does not require an input variable)
def f():
    print('In function f')
    print('When does this print?')
    
#test the empty function    
f()
```

    In function f
    When does this print?



```python
#Create an Interactive Function
def happyBirthday(person):
    print("Happy Birthday to you!")
    print("Happy Birthday to you!")
    print("Happy Birthday, dear " + person + ".")
    print("Happy Birthday to you!")

def main():
    userName = input("Enter the Birthday person's name: ")
    happyBirthday(userName)

main()
```

    Enter the Birthday person's name: Jennifer
    Happy Birthday to you!
    Happy Birthday to you!
    Happy Birthday, dear Jennifer.
    Happy Birthday to you!



```python
def square_function(x):
    return x*x

print(square_function(3))
print(square_function(3) + square_function(4)) 
```

    9
    25



```python
def lastFirst(firstName, lastName):
    separator = ', '
    result = lastName + separator + firstName
    return result

print(lastFirst('Benjamin', 'Franklin'))
print(lastFirst('Andrew', 'Harrington'))
```

    Franklin, Benjamin
    Harrington, Andrew



```python
def sumProblemString(x, y):
    sum = x + y
    return 'The sum of {} and {} is {}.'.format(x, y, sum)

def main():
    print(sumProblemString(2, 3))
    print(sumProblemString(1234567890123, 535790269358))
    a = int(input("Enter an integer: "))
    b = int(input("Enter another integer: "))
    print(sumProblemString(a, b))

main() 
```

    The sum of 2 and 3 is 5.
    The sum of 1234567890123 and 535790269358 is 1770358159481.
    Enter an integer: 3
    Enter another integer: 4
    The sum of 3 and 4 is 7.



```python
#example function, magic_calc
def magic_calc(x,y):
    z = (x * y) + (x / y)
    print(x,"multiplied and divided by",y,"equals to", z)
    return z
    
a = 5
b = 12
magic_calc(a,b)
```

    5 multiplied and divided by 12 equals to 60.416666666666664





    60.416666666666664



## Cookie Profit Function Version 1 (Level - Beginner)

This function is used to calculate the profit collected from selling a certain number of cookie.
The following conditions must be met to use this function :
- We have sold the cookies, therefore we know the number of cookies sold already
- We know the cost of making each cookie
- We know the selling price for each cookie


```python
def cookie_profit(n_cookies, cost, selling_price):
    revenue = selling_price*n_cookies
    total_cost = cost*n_cookies
    profit = revenue-total_cost
    print("============= Cookie Profit Calculator ==============")
    print("Number of Cookies Sold         :", n_cookies)
    print("Total Cost                     :", total_cost)
    print("Total Money Collected          :", revenue)
    print("Total Profit Received          :", profit)
    print("=====================================================")
    return(profit)

def input_box():
    print("Number of Cookies Sold :")
    n_cookies = float(input())
    print("Cost to Make Each Cookie :")
    cost = float(input())
    print("Selling Price per Cookie :")
    revenue = float(input())
    cookie_profit(n_cookies,cost,revenue)
```

**Let's try the function! Calculate the profit of selling 20 Cookies with Cost of 75 Cents to make each cookie and selling price of 2 Dollars each.**


```python
input_box()
```

    Number of Cookies Sold :
    20
    Cost to Make Each Cookie :
    .75
    Selling Price per Cookie :
    2
    ============= Cookie Profit Calculator ==============
    Number of Cookies Sold         : 20.0
    Total Cost                     : 15.0
    Total Money Collected          : 40.0
    Total Profit Received          : 25.0
    =====================================================


## Cookie Profit Function Version 2 (Level - Intermediate)

Now, let's consider the following scenario:
- We have not sold the cookie yet but would like to set a target of how many cookies to sell to achieve a certain amount of Profit (a target profit must be known)

With the above scenario, can we use the above function? 

No, but we can modify the function.


```python
def cookie_profit(n_cookies, cost, selling_price, target_profit):
    if (n_cookies > 0 & target_profit <= 0):
        revenue = selling_price*n_cookies
        total_cost = cost*n_cookies
        profit = revenue-total_cost
    else:
        target_n = target_profit/(selling_price-cost)
        n_cookies = target_n
        revenue = selling_price*n_cookies
        total_cost = cost*n_cookies
        profit = target_profit
    print("============= Cookie Profit Calculator ==============")
    print("Number of Cookies Sold or Targeted    :", n_cookies)
    print("Total Cost                            :", total_cost)
    print("Total Money Collected                 :", revenue)
    print("Total Profit Received or Targeted     :", profit)
    print("=====================================================")
    return(profit)


def input_box():
    print("Number of Cookies Sold :")
    n_cookies = int(input())
    print("Cost to Make Each Cookie :")
    cost = float(input())
    print("Selling Price per Cookie :")
    revenue = float(input())
    print("Target Profit to Achieve :")
    target_profit = int(input())
    cookie_profit(n_cookies,cost,revenue,target_profit)
```

**Let's try the modified function! Calculate the target number of cookies to sell with a target profit of 30 Dollars and the same cost and selling price per cookie!**
(cost per cookie = $0.75 , 

selling price per cookie = $2.00)


```python
input_box()
```

    Number of Cookies Sold :
    0
    Cost to Make Each Cookie :
    .75
    Selling Price per Cookie :
    2
    Target Profit to Achieve :
    25
    ============= Cookie Profit Calculator ==============
    Number of Cookies Sold or Targeted    : 20.0
    Total Cost                            : 15.0
    Total Money Collected                 : 40.0
    Total Profit Received or Targeted     : 25
    =====================================================


### That's it! Great Job!
