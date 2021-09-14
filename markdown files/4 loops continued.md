# floats
`floats are hella sketchy, try doing print(0.1 + 0.2 == 0.3)`

a = 0.1
b = 0.2
c = a + b

print(c)
print(c == 0.3)

***show how rounding works***
c = round(a + b, 2)

print(c)
print(c == 0.3)

# more operators
We have seen the following four operators: +, -, * and /.

Here we will introduce two new ones:

// Floor divide. (Divide and round down)
how many times something can go into something. whole numbers

% Modulo. (Divide and return the remainder)
a way that i remember is that it takes the amount of times something can be minused and the remainder

so 
5 - 2 = 3 - 2 = 1 - 2 != 0. so the answer is 1 

but 
4 - 2 = 2 - 2 = 0 so the answer is 0

## make them do this one and explain

$ python day.py
Enter a number of days: __45__
That is 6 weeks and 3 days!

days = int(input("Enter a number of days: "))

`it gets how many times 7 can go into the days, and thus how many weeks there are`
weeks = days//7

`then gets the remaining days`
rdays = days%7

print("That is {} weeks and {} days!".format(weeks, rdays))

# continuation of lists and loops

***Melk make a thing that keeps requesting input***
make a program that keeps requesting inputs. and checks if it is an integer. if it is not an integer it asks for input again
%2 if odd will return 1 if even will return 0

real_number = False

while not real_number:
    n = input("Input a number: ")
    if n.isdigit() != True:
        print("Please input an integer")
        print()
        continue
    
    n = int(n)
    real_number = True

    if n % 2 == 0:
        print("Number is even")
    if n % 2 == 1:
        print("Number is odd")

`better version`

n = input("Input a number: ")

while n.isdigit() == False:
    n = input("Incorrect input, please input an integer: ")

if n % 2 == 0:
    print("Number is even")
else:
    print("Number is odd")

`a lot of nice code occurs through iteration, seeing it and then going can i shorten this? can i make things more clear?`

## you can use the number incrementing too to do things

n = input("Enter a number: ")
odd_numbers = []
even_numbers = []
i = 0 
while i < n:
    if i % 2 == 0:
        even_numbers.append(i)
    else:
        odd_numbers.append(i)
    i += 1

print("Odd numbers are " + odd_numbers)
print("Even numbers are " + even_numbers)

## using the in keyword
`the in keyword checks if a variable is within the lists`

n = int(input("Input a number: "))
odd_numbers = []

even_numbers = []
i = 0 
while i < n:
    if i % 2 == 0:
        even_numbers.append(i)
    i += 1

i = 0
while i < n:
    if not i in even_numbers:
        odd_number.append(i)
    i += 1

print("Odd numbers are " + odd_numbers)
print("Even numbers are " + even_numbers)

# do urself

https://edstem.org/courses/5091/lessons/10049/slides/73238
$ python3 harder_idioms.py
Enter some integers: 1, 8, 5, 4, 8
Your integers were: [1, 8, 5, 4, 8]

# string methods 
https://edstem.org/courses/5091/lessons/10049/slides/73398
pass

## bouncy (maybe dont do this one)

**melk does this one**
https://edstem.org/courses/5091/lessons/10049/slides/73239
Write a program bouncy.py that prints the letters of a word, starting at index i and printing for N letters. Your program will be run using $ python3 bouncy.py <word> <i> <N>

After the program prints the last letter, it can keep printing more letters by "bouncing back" to the second-last letter. Similarly, it can also bounce back after printing the first letter.

$ python3 bouncy.py apple 0 9
applelppa

$ python3 bouncy.py quokkas 3 6
kkasak

$ python3 bouncy.py jimbo 4 9
obmijimbo

import sys

#Grab the command line arguments
word = sys.argv[1]
start = int(sys.argv[2])
end = int(sys.argv[3])

#Keep track of which letter we are at
i = start
#Keep track of how many letters have been done
counter = start
#Keep track of whether we are going forwards or backwards in the string
direction = 1

#Keep printing until our counter is done
while counter < end:
    # Print the letter
    print(word[i], end="")

    # If we have reached the end of a word, turn around
    if i == len(word) - 1 and direction == 1:
        direction = -1
    elif i == 0 and direction == -1:
        direction = 1

    # Update the letter and counter
    i += direction
    counter += 1
print()

## bouncy evens
https://edstem.org/courses/5091/lessons/10049/slides/73240 

import sys

#Grab argument
num = int(sys.argv[1])

#We need to have the first "num" even numbers
i = 0
while i < num:
    current_even = 2 + i * 2

    # We start at our even number, and print all even numbers below
    while current_even > 0:
        print(current_even)
        current_even -= 2

    i += 1


# nested loops

you might need the keyword in
and using a loop within another loop

***try and get them to do prime numbers, if unable then explain... maybe just explain***

n = int(input("Enter the number: "))

non_primes = []
primes = []

#goes through every number in the range 
for i in range(n + 1):
    
    #not inclusive of i itself
    for j in range (2, i):
    
        #when i can be divided by any number it is not a prime number
        if i % j == 0:
            non_primes.append(i)

#goes through every number
i = 2
while i < n:
    
    #if the number is not in the non_prime list, then it is a prime 
    if not (i in non_primes):
        primes.append(i)

    i += 1
print("Prime numbers:", primes)