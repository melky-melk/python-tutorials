# ----------------while loops----------------

## explaination of how they work
`loops work essentially like a perpetural if statement and keeps doing the code underneath as long as that condition is True`
while True:
    print("this will print infinately")

`use ctrl + C to break the loop in a terminal if it goes infinately`

## worked examples and do urself

***Write a program odds.py that prints all odd numbers in the range [1, 100] in ascending order, with each number on its own line.***

`melk goes through and explains this one`
i = 1
while i + 2 < 100:
    i += 2
    print(i)

correct_age = False
#sets the inital value to True, not False. while it is not correct
while not correct_age:

    #it asks for the input
    age = int(input("What is your age? "))
    
    if (age > 0 and age < 200):
        correct = True
    else:
        # got_good_input will remain False
        print("Please put in a reasonable age!\n")

print("Your age is: {}".format((age)))

***Write a program odds.py that prints all odd numbers in the range [1, 100] in descending order, with each number on its own line.***

`they write this one`
i = 99
while i > 1:
    i -= 2
    print(i)

***Convert flowchart into code. theres a picture***
https://edstem.org/courses/5091/lessons/9564/slides/69479 

***melk you convert this flowchart and explain as you go along***
https://edstem.org/courses/5091/lessons/9564/slides/69481 

## using break and continue

`break exits the loop early, it "breaks" the loop`
`continue makes the loop start again from the begining. I can further explain good uses for continue later, because right now any useful use for it can be replaces. Its more useful for more complex shit`

***melk writes this one. this is an example of break, this will continue to loop until a certain condition is reached***

`explain by removing and putting the break back in`
while True:
    input("What is the password? ")

    if name == "yeeto skeeto burrito":
        print("Valid password. Welcome")
        break
    
    print("Incorrect password, try again")

`here it doesnt exit because there is no break and it keeps asking for input`
while True:
    input("What is the password? ")

    if name == "yeeto skeeto burrito":
        print("Valid password. Welcome")
    
    print("Incorrect password, try again")

## little bit of a tangent on different ways to solve the same thing

`example on how to notice how in this it doesnt exit the loop and it still prints the Incorrect password because it isnt exited`
asking_for_password = True
while asking_for_password:
    input("What is the password? ")

    if name == "yeeto skeeto burrito":
        print("Valid password. Welcome")
        asking_for_password = False
    
    print("Incorrect password, try again")

`whereas the break exits before this next line can occur. breaks can be exited before the print statement is reached.`

`using else statements can also circumvent using a break altogether`
asking_for_password = True
while asking_for_password:
    input("What is the password? ")

    if name == "yeeto skeeto burrito":
        print("Valid password. Welcome")
        asking_for_password = False
    else:
        print("Incorrect password, try again")

# --------------------lists--------------------

## what are lists
`lists are a data type that can hold multiple different types within it inside of it like strings and integers. lists are saved as a variable and used later on`

ls = ["yeeto", "skeeto", "burrito"]

print(ls) is ["yeeto", "skeeto", "burrito"]
print(ls[0]) yeeto
print(ls[1]) skeeto
print(ls[2]) burrito

`the list hold multiple things within it. and you can access the things within the list. Because code is weird lists always start from 0`
ls[0] == "yeeto"
whereas ls[1] is skeeto

## import sys and using sys argv
`it enables you to get things from the command line and then use them as a list`

import sys

python3 filename.py yeeto skeeto burrito

print(sys.argv) #["filename.py", "yeeto", "skeeto", "burrito"]
print(sys.argv[1])
will print "yeeto"

## list can hold different kinds of data types within it
like
[24, "dollars"]

`lists can hold variables within it`
name = "Chiara"

[name, 18] is ["Chiara", 18]

`lists can even hold more lists within it`
[24, "dollars", ["yeeto", "skeeto", "burrito"]]

accessing ls[2] will give the list ["yeeto", "skeeto", "burrito"]
can even go ls[2][0] == "yeeto"

## using len
`len() takes something then prints how long it is`

len("yeeto") gives the integer 5

ls = ["yeeto", "skeeto", "burrito"] gives the integer 3

print(len(ls)) == 3

## can add things to a list using append

ls.append("bandila")
print(ls)

## looping through lists 
`looping through the list is one of the more important things loops can do later on ill teach you a better way to loop through but for now- while loops`

`remembering the odd counter`
#initially you set the variable for i to 0
i = 0
#while the i is less than the length of the list
while i < len(ls):
    #prints the item in the list the cooresponds to the thing
    print(ls[i])
    #increments i by 1, so the i increases every time till it finally reaches the length of the list
    i += 1

`if i were to write this each individually. it would go`
if 0 < 3:
    print(ls[0])

if 1 < 3:
    print(ls[1])

if 2 < 3:
    print(ls[2])

if 3 < 3:
does nothing because its False

***make em do this one then show em the solutions***
make a program that has a list of integers then takes the sum of everything inside the list then prints the answer
i = 0
answer = 0

# extra practice
https://edstem.org/courses/5091/lessons/9629/slides/69854 

***if you wanna be REALLY extra***
https://edstem.org/courses/5091/lessons/9629/slides/69855 