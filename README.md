class Superhero:
    """Represents a superhero with unique abilities and a mission."""

    def __init__(self, name, alias, power, weakness, catchphrase):
        """
        Constructor to initialize a Superhero object.

        Args:
            name (str): The superhero's real name.
            alias (str): The superhero's code name.
            power (str): The superhero's primary superpower.
            weakness (str): The superhero's main vulnerability.
            catchphrase (str): The superhero's signature saying.
        """
        self.name = name
        self.alias = alias
        self.power = power
        self.weakness = weakness
        self.health = 100  # Initial health points

    def use_power(self):
        """Prints a statement describing the superhero using their power."""
        return f"{self.alias} unleashes their incredible {self.power}!"

    def face_weakness(self):
        """Prints a statement describing the superhero being affected by their weakness."""
        self.health -= 20
        return f"{self.alias} is vulnerable to {self.weakness}! Health reduced to {self.health}."

    def speak_catchphrase(self):
        """Prints the superhero's catchphrase."""
        return f"{self.catchphrase}!"

    def is_conscious(self):
        """Checks if the superhero is still conscious."""
        return self.health > 0

    def __str__(self):
        """Returns a string representation of the Superhero object."""
        return f"Superhero: {self.alias} ({self.name}), Power: {self.power}, Weakness: {self.weakness}, Health: {self.health}"

# Creating instances of the Superhero class
kitale_defender = Superhero(name="Kiprono Sang", alias="Simba Shield", power="Super Strength and Agility", weakness="Meteoric Iron", catchphrase="For Kitale!")
forest_guardian = Superhero(name="Naomi Chebet", alias="Whisperwind", power="Nature Manipulation", weakness="Pollution", catchphrase="The Earth protects us!")

print(kitale_defender)
print(forest_guardian)

print(kitale_defender.use_power())
print(forest_guardian.speak_catchphrase())

print(kitale_defender.face_weakness())
print(kitale_defender.is_conscious())
