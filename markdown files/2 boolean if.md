# Boolean

a = True
print(a)

b = False
print(b)

Create two variables called a and b whose initial values are both 'test'.
a = 'test' 
b = 'test' 
c = (a == b)
print(c)

## using "==" and "="
c stored something called a boolean, they are coloured different and are not actually strings, they are things that represent True and False

What do you think == is?

== is an equality operator, it checks if one thing is equal to another things and returns True or False

Try changing the value of b so that it is not equal to a. What is now printed?

a = "test"
b = "yeeto skeeto burrito" 
c = (a == b)
print(c)
returns False

## The 3 boolean operators
There are 3 Boolean operators: not, and and or.

not inverts a boolean
E.g. not(False) -> True, not True -> False

and evaluates to True if both arguments are True, else it evaluates False
E.g. True and True -> True , True and False -> False

or evaluates to True if either arguments are True
E.g. True or False -> True, False or False -> False

## Order of operations:
If there are no brackets interfering, Python will perform the operations in the following order: 

1. Not
2. And
3. Or

I remember it by thinking NAO (now!).
LOOOOOOOOOL I FORGOT THERE IS A SEQUENCE but most of the time i use brakets for readability, and its good practice to make things are readable as possibe 

a = True
b = False

a and b
not (not (a)) or b 
a and not b or not a
(b and not(b)) or (a or not(a))

# if statements, elif, else 
if statements work by checking if the value next to if is True

name = "Chiara"

#name holds the variable. then checks if the name is "Chiara". it is! so then the value name == Chiara evaluates to True. 
when something next to an if statment is true, then the code underneath is then carried out. The code that is held underneath an if statment is denoted by a tab
in this case printing hello melk :D is what will happen
if name == "Chiara":
    print("Hello melk :D")

if the name == "lol this isnt a real name" (use the people ur teaching's real name lol to throw em off) however, the lines under the if statement will not be printed
in this case, it will not print anything and the code print("Hello melk :D") will never be seen

## setting variables within if statments
setting variables within if statements is pretty neato :D and very useful in the future

*#setting the variable to whatever the user inputs, as it's name*
name = input("What is your name? ")

message = "Hello {}!".format(name)

if name == "Chiara":
    message = "Ur melk :D! Nice to see you my dude!"

print(message)

here, the is statement setting the message to something new, **overrides** the previous value for message and if Chiara is entered, then 

## else
else is the catchall term, if it doesnt equal any of the things given it goes to the other one. 

it can be rewritten as 

if name == "Chiara":
    message = ":D Ur melk! Nice to see you my dude!"
else:
    message = "Hello {}!".format(name)

in this case, if it doesnt equal Chiara it will print the same thing the "Hello name!"

### mini rant about why i love code
this is what i love about code two different solutions exact same thing, and the styles can indicate and reading someone's very different solution to the same end goal is immensly satisfying
see like for me personally i prefer to not have as many if statements and set my variables initially because:

1. it saves room for lines
2. to me, it makes easier to understand. This thing is always this thing, unless something happens to change it. The path is linear, it can deviate from the path, but otherwise it feels linear. When you have an else statement, for me it feels a little more cluttered it splits and then converges on the same.
3. looks so FUCKING *cleaaaan*
4. makes if statements better, sometimes when you write and if statement and then an else it does the else block too. You can just use elif (which i will bring up in a bit) to bypass this but this also just adds to the list of why i like this solution better

but this is just my opinion, i dont mind other people's ways of solving it. if it uses else then it uses else. i just prefer this because it *feels* right. but different things feel different to other people. i also use else but when i can, i use the first option. because it just feels so fucking ***clean.***

## if statements can be chained together
name = input("What is your name? ")

message = "Hello {}!".format(name)

if name == "Chiara":
    message = ":D Ur melk! Nice to see you my dude!"
if name == "Alisa":
    message = "hewwo lem"
if name == "Emily":
    message = "beab? beab :)"

does what you expect it to, HOWEVER, if adding an else statement

## difference between if and elif. why i prefer elif

name = input("What is your name? ")

if name == "Chiara":
    message = ":D Ur melk! Nice to see you my dude!"
if name == "Alisa":
    message = "hewwo lem"
if name == "Emily":
    message = "beab? beab :)"
if name == "Taisia":
    message = "ew melk"
else:
    message = "lol ur not part of the ASS gang"

print(message)

in this case, if you typed Chiara, Alisa or Emily it would also print "lol ur not part of the ASS gang"
this is because it checks all the variables prints the code underneath. But then sees that the name Chiara is not Taisia, because of this it goes to the else statement "lol ur not part of the ASS gang"
whereas if i were to go

if name == "Chiara":
    message = ":D Ur melk! Nice to see you my dude!"
elif name == "Alisa":
    message = "hewwo lem"
elif name == "Emily":
    message = "beab? beab :)"
elif name == "Taisia":
    message = "ew melk"
else:
    message = "lol ur not part of the ASS gang"

elif essentially goes linearly and means else if. so if its not the initial it goes to the next chunk, else if its not that- then so on

# ending notes
overall, i think, if statements are the meat of coding, most of code comes from if statements and the blocks underneath it and the pathways it 

# Do it yourself :D

## traffic lights
https://edstem.org/courses/5091/lessons/9564/slides/69475
$ python traffic_lights.py
What colour is the light? green
Go!

$ python traffic_lights.py
What colour is the light? yellow
Brake!

$ python traffic_lights.py
What colour is the light? red
STOP!

$ python traffic_lights.py
What colour is the light? a
Invalid input :(

colour = input("What colour is the traffic light? ")
if colour == "green":
    print("Go!")
elif colour == "yellow":
    print("Brake!")
elif colour == "red":
    print("STOP!")
else:
    print("Invalid input :(")

## check if raining then recommend a course of action
https://edstem.org/courses/5091/lessons/9629/slides/69851 

`prompt`
The first step in this decision is based on the weather. If it is currently raining, you should take the bus.

If it is not currently raining, your method of transport should be determined by the distance you need to travel. If the distance is greater than 10km, you should take the bus. If it is between 2km and 10km (inclusive), you should ride your bike, and if it less than 2km, you should walk. You can assume the distance to always be a whole number.

Your program should only ask for the distance if it is relevant to the answer. That is, if it is raining, it shouldn't ask you how far you need to travel.

`example input statements`
Is it currently raining? Yes
You should take the bus.

Is it currently raining? No
How far in km do you need to travel? 4
You should ride your bike.

Is it currently raining? No
How far in km do you need to travel? 4
You should take the bus.

`example code`
rain = input("Is it currently raining? ") 
if rain == "Yes":
    print("You should take the bus.")
else:
    km = int(input("How far in km do you need to travel? "))
    if km < 2:
        print("You should walk.")
    elif 10 >= km >= 2:
        print("You should ride your bike.")
    elif km > 10:
        print("You should take the bus.")

make something enter something then print a statement if it is 

## Shopping and checking which is cheaper
https://edstem.org/courses/5091/lessons/9564/slides/69474

`prompt`
For example, it is cheaper to buy 12 pens for $11 rather than 10 pens for $10.
(12 pens for $11 → 91c per pen, 10 pens for $10 → $1 per pen)

The program should print Option A, then ask Quantity:  and Price:, which the user will fill out. The same should happen for Option B. It program then tells us which item was cheaper.

`example outputs`
$ python shopping.py
Option A
Quantity: 10
Price: 10

Option B
Quantity: 12
Price: 11

Option B is cheaper!

***$ python shopping.py***
Option A
Quantity: 1
Price: 5

Option B
Quantity: 2
Price: 13

Option A is cheaper!

***$ python shopping.py***
Option A
Quantity: 100
Price: 100

Option B
Quantity: 50
Price: 50

They're the same!

`answer code`
print("Option A")
quantitya = int(input("Quantity: "))
pricea = int(input("Price: "))
individualap = quantitya/pricea

print()
print("Option B")

quantityb = int(input("Quantity: "))
priceb = int(input("Price: "))
individualbp = quantityb/priceb

print()
if individualap > individualbp:
    print("Option A is cheaper!")
elif individualap < individualbp:
    print("Option B is cheaper!")
elif individualap == individualbp:
    print("They're the same!")