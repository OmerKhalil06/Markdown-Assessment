# Object Oriented Programming Notes 
---
##  Definitions and Theory 
### Class
* Classification of a group 
* Classes have attributes and methods (data and abilities)
* An object is an instance of class 

### Object 
* Combination of data and functional code (States & Behavior/ Attributes & Methods)
* Location of memory with value 
* Intance of **class**
* Refered to as an "Identifier" 

### OOP Paradigm (Model)
* designing modular reusable software systems 
* Design programs with the creation of objects 
* Approach that focuses on data definition 
  *EX. (data such as name or age, or methods/function)
* Goal: Object that is defined and used to solve problems 

### Encapsulation 
* Restricting accesss to classes/object's attributes and methods 
* Why? Data protection and restricting methods to be called 
* Isnt really possible in python, but can be done by using __ prefix 

### Overrides 
Types:
* Overloading: Two methods in the same class with same name but different parameters 
  * No overloading in python 
* Overriding: Two methods with the same name and same parameters 
  * Different classes (one in parent, one in child) 
  
### Polymorphism
* A Method that can be used in many classes and object depends on the parameters
  * Different classes (not-inhereited) can have the same named method 

--- 
## Coding 
### Creating a class 

```python
class ClassName: #class keyword to define a class 
                 #ClassName always starts with a capital 
```

### Attributes: An objects accessable tools/data 
```python
class Dog: #Creating class of Dog 
#side note: pass can be used to pass an empty block 
  def __init__(self, name, age):#defining the initialization of the class & setting required arguments 
    self.name = name #self refers to the object running the class and is a local value 
    self.age = age #applying the value of age to the self.age method  
  def bark(self):
    print ("Bark")

#using the Class 
dog1=Dog(Josh, 3) 
print(dog1.age) #returns 3 
```

### Encapsulation
```python
class Account:
  def __init__(self, username, password):
    self.user = username 
    self.__pass = password #double underscore prefix 
    
  def __password(self):
  return self.__pass #will result in error as self.__pass only exists in __init__ 
  
  #important as values wont be changed, EX.
  account1=Account(okhalil_1, password1)
  
  account1.user = "HAHA I CHANGED YOUR USERNAME" #changes the original value which could ruin code
```

### Setting and Getting 
```python
def setMethod(self, variable): #define the setter with the argument replacemnt 
  self.__encap=variable: #setting the new argument 
  
def getMethod(self): #get method 
  return self.__encap #return first name 
 
 
### Polymorphism 
```python
class Bear:
  def sound(self):
    print("Groar")
class Dog:  
  def sound(self):
    print("Bark")

def makeSound(animaltype): #function that can apply to more than one class 
  animalType.sound()
  
b_obj=Bear()
d_obj=Dog()

makeSound(b_obj)
#returns "Groar 
makeSound(d_obj) 
#returns "Bark"
```

### __repr__ and __str__ functions 
- add later 
