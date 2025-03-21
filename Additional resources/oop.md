# Object-Oriented Programming (OOP) in Python

Object-Oriented Programming (OOP) is a programming paradigm that uses **objects** and **classes** to structure and organize code. It allows developers to create reusable and modular code by encapsulating data (attributes) and behavior (methods) into objects. Python is an object-oriented language, and it provides robust support for OOP concepts.

---

## Classes and Objects

### What is a Class?
A **class** is a blueprint or template for creating objects. It defines the properties (attributes) and behaviors (methods) that the objects created from the class will have. Think of a class as a cookie cutter, and objects as the cookies made from it.

### What is an Object?
An **object** is an instance of a class. It is a concrete entity created from the class blueprint, with its own unique data and behavior.

---

## Defining a Class in Python

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

---

## Creating Objects (Instances)

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

---

## Changing Values in Objects

One of the key features of OOP is the ability to modify the attributes of an object after it has been created. Let's see how we can change the values of an object's attributes.

### Example: Modifying the `Dog` Object

```python
# Create a Dog object
dog = Dog("Rex", 4)

# Print initial values
print(dog.name)  # Output: Rex
print(dog.age)   # Output: 4

# Change the name and age
dog.name = "Rocky"
dog.age = 5

# Print updated values
print(dog.name)  # Output: Rocky
print(dog.age)   # Output: 5
```

### Example: Modifying the `Car` Object

Let’s revisit the `Car` class and modify its attributes:

```python
class Car:
    # Class attribute
    wheels = 4

    # Constructor
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.speed = 0  # Default speed

    # Instance method to accelerate
    def accelerate(self, increment):
        self.speed += increment
        return f"The {self.make} {self.model} is now going {self.speed} km/h."

    # Instance method to brake
    def brake(self, decrement):
        self.speed -= decrement
        return f"The {self.make} {self.model} slowed down to {self.speed} km/h."

    # Instance method to describe the car
    def describe(self):
        return f"This is a {self.year} {self.make} {self.model} with {self.wheels} wheels."
```

#### Modifying the `Car` Object

```python
# Create a Car object
my_car = Car("Toyota", "Corolla", 2022)

# Print initial values
print(my_car.describe())  # Output: This is a 2022 Toyota Corolla with 4 wheels.

# Change the year and model
my_car.year = 2023
my_car.model = "Camry"

# Print updated values
print(my_car.describe())  # Output: This is a 2023 Toyota Camry with 4 wheels.
```

---

## Why Use OOP?

- **Reusability**: Classes can be reused to create multiple objects.
- **Modularity**: Code is organized into logical units (classes and objects).
- **Encapsulation**: Data and behavior are bundled together, making code easier to manage.
- **Abstraction**: Complex implementation details are hidden, exposing only necessary functionality.

---

## Inheritance: A Sneak Peek

Inheritance is a powerful OOP concept that allows you to create a new class based on an existing class. The new class (child class) inherits attributes and methods from the existing class (parent class). Here's a quick example:

```python
# Parent class
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return f"{self.name} makes a sound."

# Child class
class Cat(Animal):
    def speak(self):
        return f"{self.name} says meow!"

# Create an object of the child class
my_cat = Cat("Whiskers")
print(my_cat.speak())  # Output: Whiskers says meow!
```

In this example, the `Cat` class inherits from the `Animal` class and overrides the `speak` method.

---

## Conclusion

OOP is a fundamental concept in Python that helps you write clean, modular, and reusable code. By understanding **classes**, **objects**, and how to **modify object attributes**, you can build complex programs with ease. Practice creating your own classes and objects to get comfortable with these concepts!
