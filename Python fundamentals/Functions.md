In Python function is a reusable block of code that we can run when we call it. A functions makes tasks easier because the code can be reused and we do not have to write the same code each time we want to.
Example :
def who_am_i():
     name = "irfan"
     age = 18
     print("My name is "  +  name  +  "  and i am "  +  str(age) +  "  years old.)
who_am_i()

OUTPUT :
My name is irfan and i am 18 years old.

* This is a no argument function meaning we don't have to input anything we just have to call it when we want to use it.

Another example :
def subtract(x,y):
     print(x - y)

subtract(7,3)	 

OUTPUT : 
4

* This function takes two arguments when we want to subtract.Also known as function with parameters.