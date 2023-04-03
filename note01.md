# Object Oriented Progamming Notes 1

I think OOP is awesome!

```python
# Example class

class Person:
    def __init__(self, name):
        self.name = name 
    
    def __str__(self):
        return f"Person Object called: {self.name}"
       
    def __repr__(self): 
        return self.__str__()
```

## Definitions 
- Encapsulation → Information Hiding: Restricting the access to the classes/objects’ certain attributes and methods. 
__Note__: In Python, this isn’t really possible: hence we use a special system. → We hide attributes and methods by using a double underscore __ as a prefix. 

```python
# Example Emcapsulation
class Student:
  def __init__(self,nameF, nameL, num):
    self.firstName = nameF
    self.lastName = nameL
    self.__studentNumber = num
  
  def __getStudentNumber(self):
    return self.__studentNumber

#end of Student
s1 = Student("Mr.", "Park", 10)
print(s1.__getStudentNumber()) # Will cause an error
print(s1.__studentNumber) # Will also cause an error
```

- Polymorphism: A method that can be used across different classes and object that is dependent on the parameters.
__Ideas__: Different Classes (non-inherited) can have the same named methods (Simple) → Polymorphism. Within a set of inherited classes have the same methods

```python
class Bear:
    def sound(self):
        print("Groarrr")
 
class Dog:
    def sound(self):
        print("Woof woof!")
 
def makeSound(animalType):
    animalType.sound()
bearObj = Bear()
dogObj = Dog()
 
makeSound(bearObj)
makeSound(dogObj)
```
In Conclusion:
We can give two different classes same methods; hence, Polymorphism

- Override: Two methods with the same method name and parameters.

```python
# Example override
class Dog:
	def __init__(self,name):
		self.__name = name
	
	def __str__(self):
		return “Woof, I’m %s.” % self.__name

corgi = Dog(“Tobasco”)
print(corgi) → “Woof, I’m Tobasco.”
```

- Overloading: Two methods in one class that have the same method name, but different parameters


- Inheritance: When an object or class is based on another class; where its features are from a parent class
__Types__:
Single Inheritance: A subclass inheriting the features of a single superclass / parent class
Multiple Inheritance: A subclass inheriting the features of a multiple parent classes
Multilevel Inheritance: A subclass is inheriting from another subclass… A → B → C

Inheritance can have an hierarchy (branching like a tree) and/or be a hybrid: mixing the types of inheritances

```python
class ParentClassName:
	“”” Define Parent Class “””
	.
	.
	.

class InheritanceClass(ParentClassName):
	“”” Define Inherited Class “””

	def __init__(self, param, param2):
		ParentClassName.__init__(self, param)
		self.param2 = param2
```
