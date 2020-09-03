# Crash Course of Python - Week 5 - Object Oriented Programming

## Practice Quiz: Object-oriented Programming 
Q2. Creating new instances of class objects can be a great way to keep track of values using attributes associated with the object. The values of these attributes can be easily changed at the object level. The following code illustrates a famous quote by George Bernard Shaw, using objects to represent people. Fill in the blanks to make the code satisfy the behavior described in the quote.

```Python
# “If you have an apple and I have an apple and we exchange these apples then
# you and I will still each have one apple. But if you have an idea and I have
# an idea and we exchange these ideas, then each of us will have two ideas.”
# George Bernard Shaw

class Person:
    apples = 0
    ideas = 0

johanna = Person()
johanna.apples = 1
johanna.ideas = 1

martin = Person()
martin.apples = 2
martin.ideas = 1

def exchange_apples(you, me):
#Here, despite G.B. Shaw's quote, our characters have started with       #different amounts of apples so we can better observe the results. 
#We're going to have Martin and Johanna exchange ALL their apples with #one another.
#Hint: how would you switch values of variables, 
#so that "you" and "me" will exchange ALL their apples with one another?
#Do you need a temporary variable to store one of the values?
#You may need more than one line of code to do that, which is OK. 
    temp = you.apples
    you.apples = me.apples
    me.apples = temp
    return you.apples, me.apples
    
def exchange_ideas(you, me):
    #"you" and "me" will share our ideas with one another.
    #What operations need to be performed, so that each object receives
    #the shared number of ideas?
    #Hint: how would you assign the total number of ideas to 
    #each idea attribute? Do you need a temporary variable to store 
    #the sum of ideas, or can you find another way? 
    #Use as many lines of code as you need here.
    you.ideas = me.ideas + you.ideas
    me.ideas = you.ideas
    return you.ideas, me.ideas

exchange_apples(johanna, martin)
print("Johanna has {} apples and Martin has {} apples".format(johanna.apples, martin.apples))
exchange_ideas(johanna, martin)
print("Johanna has {} ideas and Martin has {} ideas".format(johanna.ideas, martin.ideas))
```
```
Johanna has 2 apples and Martin has 1 apples
Johanna has 2 ideas and Martin has 2 ideas
```

Q3. The City class has the following attributes: name, country (where the city is located), elevation (measured in meters), and population (approximate, according to recent statistics). Fill in the blanks of the max_elevation_city function to return the name of the city and its country (separated by a comma), when comparing the 3 defined instances for a specified minimal population. For example, calling the function for a minimum population of 1 million: max_elevation_city(1000000) should return "Sofia, Bulgaria".

```Python
# define a basic city class
class City:
	name = ""
	country = ""
	elevation = 0 
	population = 0

# create a new instance of the City class and
# define each attribute
city1 = City()
city1.name = "Cusco"
city1.country = "Peru"
city1.elevation = 3399
city1.population = 358052

# create a new instance of the City class and
# define each attribute
city2 = City()
city2.name = "Sofia"
city2.country = "Bulgaria"
city2.elevation = 2290
city2.population = 1241675

# create a new instance of the City class and
# define each attribute
city3 = City()
city3.name = "Seoul"
city3.country = "South Korea"
city3.elevation = 38
city3.population = 9733509

def max_elevation_city(min_population):
	# Initialize the variable that will hold 
	# the information of the city with 
	# the highest elevation 
	highest_elevation = 0
	return_city = ""

	# Evaluate the 1st instance to meet the requirements:
	# does city #1 have at least min_population and
	# is its elevation the highest evaluated so far?
	if (city1.population > min_population):
		if(highest_elevation < city1.elevation):
			highest_elevation=city1.elevation
			return_city = ("{}, {}".format(city1.name, city1.country))
	# Evaluate the 2nd instance to meet the requirements:
	# does city #2 have at least min_population and
	# is its elevation the highest evaluated so far?
	if (city2.population > min_population):
		if(highest_elevation<city2.elevation):
			highest_elevation=city2.elevation
			return_city = ("{}, {}".format(city2.name, city2.country))
	# Evaluate the 3rd instance to meet the requirements:
	# does city #3 have at least min_population and
	if (city3.population > min_population):
		if(highest_elevation < city3.elevation):
			highest_elevation = city3.elevation
			return_city = ("{}, {}".format(city3.name, city3.country))

	#Format the return string
	if return_city != "":
		return return_city
	else:
		return ""

print(max_elevation_city(100000)) # Should print "Cusco, Peru"
print(max_elevation_city(1000000)) # Should print "Sofia, Bulgaria"
print(max_elevation_city(10000000)) # Should print ""
```
```
Cusco, Peru
Sofia, Bulgaria

```

Q5. We have two pieces of furniture: a brown wood table and a red leather couch. Fill in the blanks following the creation of each Furniture class instance, so that the describe_furniture function can format a sentence that describes these pieces as follows: "This piece of furniture is made of {color} {material}"

```Python
class Furniture:
	color = ""
	material = ""

table = Furniture()
table.color = "brown"
table.material = "wood"

couch = Furniture()
couch.color = "red"
couch.material = "leather"

def describe_furniture(piece):
	return ("This piece of furniture is made of {} {}".format(piece.color, piece.material))

print(describe_furniture(table)) 
# Should be "This piece of furniture is made of brown wood"
print(describe_furniture(couch)) 
# Should be "This piece of furniture is made of red leather"
```
```
This piece of furniture is made of brown wood
This piece of furniture is made of red leather
```

---

## Practice Quiz: Methods and Classes
In [6]
```Python
class Elevator:
    def __init__(self, bottom, top, current):
        """Initializes the Elevator instance."""
        self.bottom = bottom
        self.top = top
        self.current = current
    def __str__(self):
        """Information about current floor"""
        return "Current floor: {}".format(self.current)
    def up(self):
        """Makes the elevator go up one floor."""
        if self.current < 10:
            self.current += 1
    def down(self):
        """Makes the elevator go down one floor."""
        if self.current > 0:
            self.current -= 1
    def go_to(self, floor):
        """Makes the elevator go to the specific floor."""
        if floor >= self.bottom and floor <= self.top:
            self.current = floor
        elif floor < 0:
            self.current = 0
        else:
            self.current = 10

elevator = Elevator(-1, 10, 0)
```

---

## Practice Quiz: Code Reuse
In [5]

```Python
class Turtle(Animal):
    category = "reptile"
```
In [7]

```Python
class Snake(Animal):
    category = "reptile"
```
In [8]

```Python
class Zoo:
    def __init__(self):
        self.current_animals = {}
    
    def add_animal(self, animal):
        self.current_animals[animal.name] = animal.category
    
    def total_of_category(self, category):
        result = 0
        for animal in self.current_animals.values():
            if animal == category:
                result += 1
        return result

zoo = Zoo()
```
