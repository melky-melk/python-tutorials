# FIRST TUTORIAL
goes through printing, input, variables, string concatination, why string + int doesnt work 

## set up vscode, go through the pretty themes :D
windows users need to download wsl. both need to download python. 

## how to use basic terminal shit
`using cd commands to find file, or (which is better) using vscode and finding file through the directory `
python3 <filename.py>
cd basic running commands 

## print hello world using the terminal. 
`once printing Hello, world! for the first time, you like many others will start the path down coding`
print("Hello, World!")

***do it urself print other random shit, stringing together prints. different types of quotation marks "" '' '''''' """"""***
print("+-------+")
print("|       |")
print("|       |")
print("|       |")
print("+-------+")

## setting variables using = sign. printing the variables. concatination of strings together (the thing with spaces that you need to remember)
first_name = Santa
last_name = Claus
full_name = first_name + last_name
print(full_name)

`will print SantaClaus. computers need to be told EVERY specification, even if it feels like those specifications are implied, you still need to manually add those spaces`

full_name = first_name + ' ' + last_name
print(full_name)
`will print 'Santa Claus'`

## using inputs and strings
`inputs (intutitively,) take the input the user puts in, and saves that input as a variable (although you don't *need* to save it as a variable)`
first_name = input("What is your first name? ")
last_name = input("What is your last name? ")
full_name = first_name + ' ' + last_name

print("Hello," + full_name + "nice to meet you! ")
`remember the spaces!`
print("Hello, " + full_name + " nice to meet you! ")

***do it yourself***
$ python favourite_show.py
Hello!
What is your favourite show? __Steins Gate__
What type of show is it? __Anime__
Your favourite show, Steins Gate, is a Anime!

## putting numbers into the inputs, declaring data types and how inputs assume a string
num_1 = input("input the first number: ")
num_2 = input("input the second number: ")

sum = num_1 + num_2 

print("Sum is " + sum + "!")

ask what you think it prints? and why

print(type(num)) # will print a string

**input immdiately converts to strings**

`teach em that whenever you ask for input, it assumes and converts to strings`
`you need to change the data type to an integer to make it act like a number rather than a string that has a number (you can do the whole ctrl + alt)`

num_1 = int(input("input the first number: "))
num_2 = int(input("input the second number: ")) 

sum = num_1 + num_2 

print("Sum is " + sum + "!")

`this still makes an error`

### cha cha into concatination why int + string doesnt work. this will print an error

`see if i were to do`
message = 'twenty-four' + ' ' + 'dollars' 
print(message)
'twenty-four dollars'

`it would make sense`
message = 20 + 4 
print(message)
24

`but if i were to try`
message = 24 + ' dollars'
print(message)

`it would return an error`
`how can a computer ad a number to a string? it doesnt make sense, what is banana + 4? what does that mean. you need to declare that the 24 is a string`
message = '24' + ' dollars'

***alternatively can do this, (a little redundant but its useful in the future)***

money_amount = str(24)
message = money_amount + ' dollars'

`then prints the correct one, in the case of sum, you need to declare the two variables`
num_1 = 20
num_2 = 4
sum = num_1 + num_2

`again will not work because cant add an integer to a thing`
print("Sum is " + sum)

sum = str(num_1 + num_2)

print("Sum is " + sum + "!")

`Sum is sum! which, is not helpful. it may be hard to understand but a lot of code just feels right, intutitively`

sum = 24 contains the number 24 
'sum' is simply a string containing nothing but string
print("Sum is " + sum + "!")

## do it yourself

$ python3 hello_there.py
Hello!
What is your first name? __Naruto__
What is your last name? __Uzumaki__
Nice to meet you, Naruto Uzumaki.

What is your age? __21__
Amazing! Just another 79 years before you turn 100.

### ROUNDING
round(82.3)
can round to the nearest int
can later use round to do other shit

***they do this one***

$ python3 fah_to_cel.py
What degrees in Fahrenheit would you like to convert to Celsius? __180__
That is roughly equivalent to 82 degrees Celsius.

$ python3 fah_to_cel.py
What degrees in Fahrenheit would you like to convert to Celsius? __181__
That is roughly equivalent to 83 degrees Celsius.

***do it urself with getting the average of 5 numbers then print the answer***
num_1 = int(input("Input the first number: "))
num_2 = int(input("Input the second number: "))
num_3 = int(input("Input the third number: "))
num_4 = int(input("Input the fourth number: "))
num_5 = int(input("Input the fifth number: "))

average = (num_1 + num_2 + num_3 + num_4 + num_5)/5

print("The average for the numbers is " + straverage)

### can cha cha into format and f strings
`tbh its almost painful to continue doing string concatination in this way so i might teach you do basic formatting because on god i hate string concatination, its so incredibly fiddily`
print("Hello, {} nice to meet you!".format(full_name))
`it will print the spaces and the variable you provide in the brackets, it corresponds to the thing`

## homework if you so choose

***make a cowsay thing. input something and print it out more interesting. google cowsay***

***do it urself making a celcius to farenheit converter :D***
make it so it asks for the input for something in celcius, then apply things to it to convert it to to farenheit
make it print a statement saying 
"{} celcius is {} farenheit".format(celcius, farenheit)

***dot product***
get 6 numbers and times them together
one = int(input())
two = int(input())
three = int(input())
four = int(input())
five = int(input())
six = int(input())

print("V = {" + " {}, {}, {} ".format(one, two, three) + "}")
print("U = {" + " {}, {}, {} ".format(four, five, six) + "}")
dot = str(one*four + two*five + three*six)
print("V . U = " + dot)
