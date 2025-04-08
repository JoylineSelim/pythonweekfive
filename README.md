# pythonweekfive
assignment one
# Base class: Device
class Device:
    def __init__(self, brand, model, release_year):
        self.brand = brand
        self.model = model
        self.release_year = release_year
    
    def device_info(self):
        return f"{self.brand} {self.model}, released in {self.release_year}"

# Derived class: Smartphone (inherits from Device)
class Smartphone(Device):
    def __init__(self, brand, model, release_year, os, screen_size):
        # Calling the constructor of the parent class (Device)
        super().__init__(brand, model, release_year)
        self.os = os
        self.screen_size = screen_size
    
    def phone_info(self):
        device_info = self.device_info()
        return f"{device_info}, OS: {self.os}, Screen Size: {self.screen_size} inches"

# Create an object of the Smartphone class
phone = Smartphone("Apple", "iPhone 14", 2022, "iOS", 6.1)

print(phone.phone_info())

Activity 2
# Base class: Vehicle
class Vehicle:
    def move(self):
        pass  # Placeholder method to be overridden by child classes

# Derived class: Car (inherits from Vehicle)
class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

# Derived class: Plane (inherits from Vehicle)
class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

# Create objects of the Car and Plane classes
car = Car()
plane = Plane()

# Call the move method for each
car.move()  # Output: Driving 🚗
plane.move()  # Output: Flying ✈️
