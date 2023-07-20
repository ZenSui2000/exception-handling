# exception-handling

1. An exception is a Python object that represents an error. 
   An Exception is an event that occurs during the program execution and disrupts the normal flow of the program's execution
   Errors mostly happen at compile-time like syntax error; however it can happen at runtime as well. Whereas an Exception occurs at runtime (checked exceptions can    be detected at compile time)

2. When an exception is not handled then the runtime system will abort the program (i.e. crash) and an exception message will print to the console.

  class purchase

  amount = 5000

  if amount > 2500

  print "you are eligible to purchase data science course"

3. The try and except block in Python is used to catch and handle exceptions.
  Python executes code following the try statement as a “normal” part of the program.

  class purchase

  amount = 5000

  if amount > 2500

  print "you are eligible to purchase data science course"

4. def divide(x, y):
	try:
		result = x // y
	except ZeroDivisionError:
		print("Sorry ! You are dividing by zero ")
	else:
		print("Yeah ! Your answer is :", result)

divide(3, 2)
divide(3, 0)

5.     x = 1
      if x < 2:
      raise Exception("one numbers below two")

6.  Like standard exception classes, custom exceptions are also classes.
We need custom exception in python because can make your code much more readable and robust, and reduce the amount of code you write later to try and figure out what exactly went wrong.


class MyError(Exception):

	def __init__(self, value):
		self.value = value

         def __str__(self):
	return(repr(self.value))
try:
	raise(MyError(3*2))

except MyError as error:
	print('A New Exception occurred: ', error.value)


7. class Error(Exception):
	"""Base class for other exceptions"""
	pass

class zerodivision(Error):
	"""Raised when the input value is zero"""
	pass

try:
	i_num = int(input("Enter a number: "))
	if i_num == 0:
		raise zerodivision
except zerodivision:
	print("Input value is zero, try again!")
	print()
