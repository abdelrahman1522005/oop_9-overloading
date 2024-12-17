# oop_9-overloading
"""
    Method Overloading in Python
    
    Two or more methods have the same name but different numbers of parameters or different types 
    of parameters, or both. These methods are called overloaded methods and this is called method 
    overloading. 
    
    Like other languages (for example, method overloading in C++) do, python does not support method 
    overloading by default. But there are different ways to achieve method overloading in Python. 
"""



# First product method.
# Takes two argument and print their
# product


def product(a, b):
	p = a * b
	print(p)

# Second product method
# Takes three argument and print their
# product


def product(a, b, c):
	p = a * b*c
	print(p)

# Uncommenting the below line shows an error
# product(4, 5)


# This line will call the second product method
product(4, 5, 5)


print('####################################################')

"""
Solution : Method 1 (Not The Most Efficient Method):
"""
# Function to take multiple arguments
def add(datatype, *args):

	# if datatype is int
	# initialize answer as 0
	if datatype == 'int':
		answer = 0

	# if datatype is str
	# initialize answer as ''
	if datatype == 'str':
		answer = ''

	# Traverse through the arguments
	for x in args:

		# This will do addition if the
		# arguments are int. Or concatenation
		# if the arguments are str
		answer = answer + x

	print(answer)


# Integer
add('int', 5, 6)

# String
add('str', 'Hi ', 'Geeks')

print('####################################################')

"""
Solution : Method 2 (Not the efficient one):
"""
# code
def add(a=None, b=None):
	# Checks if both parameters are available
	# if statement will be executed if only one parameter is available
	if a != None and b == None:
		print(a)
	# else will be executed if both are available and returns addition of two
	else:
		print(a+b)


# two arguments are passed, returns addition of two
add(2, 3)
# only one argument is passed, returns a
add(2)
