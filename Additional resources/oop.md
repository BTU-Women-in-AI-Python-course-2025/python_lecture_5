# Object-Oriented Programming (OOP) in Python

Object-Oriented Programming (OOP) is a programming paradigm that uses objects and classes to structure and organize code. It allows developers to create reusable and modular code by encapsulating data (attributes) and behavior (methods) into objects. Python is an object-oriented language, and it provides robust support for OOP concepts.

## Classes and Objects

### What is a Class?
A **class** is a blueprint or template for creating objects. It defines the properties (attributes) and behaviors (methods) that the objects created from the class will have. Think of a class as a cookie cutter, and objects as the cookies made from it.

### What is an Object?
An **object** is an instance of a class. It is a concrete entity created from the class blueprint, with its own unique data and behavior.

### Defining a Class in Python
In Python, you define a class using the `class` keyword. Here's an example of a simple class:

```python
class Dog:
    # Class attribute (shared by all instances)
    species = "Canis familiaris"

    # Constructor method (initializes the object)
    def __init__(self, name, age):
        # Instance attributes (unique to each object)
        self.name = name
        self.age = age

    # Instance method (behavior of the object)
    def bark(self):
        return f"{self.name} says woof!"

    def get_age(self):
        return f"{self.name} is {self.age} years old."
```

### Creating Objects (Instances)
Once a class is defined, you can create objects (instances) of that class. Here's how you can create and use objects of the `Dog` class:

```python
# Create two Dog objects
dog1 = Dog("Buddy", 3)
dog2 = Dog("Max", 5)

# Access attributes and call methods
print(dog1.name)  # Output: Buddy
print(dog2.age)   # Output: 5

print(dog1.bark())  # Output: Buddy says woof!
print(dog2.get_age())  # Output: Max is 5 years old.

# Access class attribute
print(dog1.species)  # Output: Canis familiaris
```

### Key Concepts in the Example
1. **Class Attribute (`species`)**: Shared by all instances of the class.
2. **Instance Attributes (`name`, `age`)**: Unique to each object.
3. **Constructor (`__init__`)**: A special method that initializes the object when it is created.
4. **Instance Methods (`bark`, `get_age`)**: Functions defined inside the class that describe the behavior of the object.

### Why Use OOP?
- **Reusability**: Classes can be reused to create multiple objects.
- **Modularity**: Code is organized into logical units (classes and objects).
- **Encapsulation**: Data and behavior are bundled together, making code easier to manage.
- **Abstraction**: Complex implementation details are hidden, exposing only necessary functionality.
