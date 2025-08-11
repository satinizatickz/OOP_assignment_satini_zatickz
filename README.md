# OOP Assignment
# Author: Satini Zatickz
# Date: August 2025

# ========================
# Assignment 1: Superhero Class with Inheritance
# ========================

class Superhero:
    def __init__(self, name, power, city):
        self.name = name
        self.power = power
        self.city = city
    
    def introduce(self):
        return f"I am {self.name}, my power is {self.power}, and I protect {self.city}!"

    def use_power(self):
        return f"{self.name} uses {self.power}! 💥"


# Inheritance example
class FlyingHero(Superhero):
    def __init__(self, name, power, city, max_height):
        super().__init__(name, power, city)
        self.max_height = max_height
    
    # Method overriding (polymorphism)
    def use_power(self):
        return f"{self.name} soars up to {self.max_height} meters while using {self.power}! 🦅"


# ========================
# Activity 2: Polymorphism Challenge
# ========================

class Vehicle:
    def move(self):
        pass  # This will be overridden by subclasses


class Car(Vehicle):
    def move(self):
        return "Driving 🚗"


class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"


class Boat(Vehicle):
    def move(self):
        return "Sailing 🚢"


# ========================
# Main Program
# ========================
if __name__ == "__main__":
    # Superhero examples
    hero1 = Superhero("Shadow Strike", "Invisibility", "Night City")
    hero2 = FlyingHero("Skyblazer", "Fire Blast", "Cloud Town", 5000)

    print("=== Superhero Demonstration ===")
    print(hero1.introduce())
    print(hero1.use_power())
    print(hero2.introduce())
    print(hero2.use_power())

    # Polymorphism example
    print("\n=== Vehicle Polymorphism Demonstration ===")
    vehicles = [Car(), Plane(), Boat()]
    for v in vehicles:
        print(v.move())
