# windclass Wind:
    def __init__(self, speed, direction):
        self.speed = speed  # speed in km/h
        self.direction = direction  # direction as a string

    def get_details(self):
        return f"Wind details: Speed: {self.speed} km/h, Direction: {self.direction}"

    def get_category(self):
        if self.speed < 1:
            return "Calm"
        elif self.speed <= 5:
            return "Light Air"
        elif self.speed <= 11:
            return "Light Breeze"
        elif self.speed <= 19:
            return "Gentle Breeze"
        elif self.speed <= 28:
            return "Moderate Breeze"
        elif self.speed <= 38:
            return "Fresh Breeze"
        elif self.speed <= 49:
            return "Strong Breeze"
        elif self.speed <= 61:
            return "Near Gale"
        elif self.speed <= 74:
            return "Gale"
        elif self.speed <= 88:
            return "Strong Gale"
        elif self.speed <= 102:
            return "Storm"
        elif self.speed <= 117:
            return "Violent Storm"
        else:
            return "Hurricane"

# Create an instance of the Wind class
my_wind = Wind(speed=45, direction="NW")

# Print the details of the wind
print(my_wind.get_details())

# Print the wind category
print(f"Wind category: {my_wind.get_category()}")
