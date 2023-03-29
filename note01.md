# Object Oriented Progamming Notes 1

I think OOP is awesome :D

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
