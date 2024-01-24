class Coffee:
    def grindCoffee(self):
        pass

    def makeCoffee(self):
        pass

    def pourIntoCup(self):
        pass


class Espresso(Coffee):
    def grindCoffee(self):
        print("Grinding espresso coffee beans")

    def makeCoffee(self):
        print("Making espresso")

    def pourIntoCup(self):
        print("Pouring espresso into cup")


class Cappuccino(Coffee):
    def grindCoffee(self):
        print("Grinding cappuccino coffee beans")

    def makeCoffee(self):
        print("Making cappuccino")

    def pourIntoCup(self):
        print("Pouring cappuccino into cup")


class Americano(Coffee):
    def grindCoffee(self):
        print("Grinding americano coffee beans")

    def makeCoffee(self):
        print("Making americano")

    def pourIntoCup(self):
        print("Pouring americano into cup")


class CoffeeFactory:
    def createCoffee(self, coffee_type):
        if coffee_type == "Espresso":
            return Espresso()
        elif coffee_type == "Cappuccino":
            return Cappuccino()
        elif coffee_type == "Americano":
            return Americano()
        else:
            raise ValueError("Invalid coffee type")


# Пример за използване на фабриката:
coffee_factory = CoffeeFactory()

# Създаване на Espresso
espresso = coffee_factory.createCoffee("Espresso")
espresso.grindCoffee()
espresso.makeCoffee()
espresso.pourIntoCup()

# Създаване на Cappuccino
cappuccino = coffee_factory.createCoffee("Cappuccino")
cappuccino.grindCoffee()
cappuccino.makeCoffee()
cappuccino.pourIntoCup()

# Създаване на Americano
americano = coffee_factory.createCoffee("Americano")
americano.grindCoffee()
americano.makeCoffee()
americano.pourIntoCup()
