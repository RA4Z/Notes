A class in programming is a blueprint or template used in [[Object-Oriented Programming]] to define the structure and behavior of objects.

It encapsulates **attributes** (data) and **methods** (functions)  that operate on that data, enabling code re-usability, abstractions and maintainability.

A class itself does not store data until an [[Object]] (instance) is created from it.

### Key Components of a Class
- **Attributes (Fields/Properties):** Variables that hold object data;
- **Methods:** Functions that define object behavior;
- **Constructor:** Special method to initialize new objects;
- **Encapsulation:** Bundling data and methods together;
- **Inheritance & Polymorphism:** Mechanisms to extend and customize behavior;

### Python Example:
```Python
class Car:
   def __init__(self, make, model, color):
       self.make = make
       self.model = model
       self.color = color
   def drive(self):
       print(f"The {self.color} {self.make} {self.model} is driving.")
# Creating objects
car1 = Car("Toyota", "Corolla", "Blue")
car2 = Car("Tesla", "Model S", "Red")
car1.drive() # Output: The Blue Toyota Corolla is driving
car2.drive() # Output: The Red Tesla Model S is driving
```