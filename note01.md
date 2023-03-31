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

- Polymorphism: A method that can be used across different classes and object that is dependent on the parameters.
__Ideas__: Different Classes (non-inherited) can have the same named methods (Simple) → Polymorphism. Within a set of inherited classes have the same methods

- Override: Two different classes have a same attributes and methods

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

- Inheritance: When an object or class is based on another class; where its features are from a parent class
__Types__:
Single Inheritance: A subclass inheriting the features of a single superclass / parent class
Multiple Inheritance: A subclass inheriting the features of a multiple parent classes
Multilevel Inheritance: A subclass is inheriting from another subclass… A → B → C

Inheritance can have an hierarchy (branching like a tree) and/or be a hybrid: mixing the types of inheritances
