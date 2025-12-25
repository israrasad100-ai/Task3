# Task3

# 1
class Person():
    def __init__(self,name,age,gender):
        self.name = name 
        self.age = age 
        self.gender = gender
    
    def person_info(self):
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")
        print(f"Gender: {self.gender}")
             
p1 = Person("Sarim","16","Male")
p1.person_info()
p2 = Person("Ali","12","Male")
p2.person_info()


#2
class Rectangle():
    def __init__(self,length,width):
        self.length = length
        self.width = width
    def area(self):
        print (self.length*self.width)
                    
r1 = Rectangle(20,10)
r1.area()

#3
class vehicle():
    def __init__(self,make,model,brand,color):
        self.make = make
        self.model = model
        self.brand = brand
        self.color = color
    def car_detail(self):
        print(f"Make: {self.make}")
        print(f"Model: {self.model}")
        print(f"Brand : {self.brand}")
        print(f"Color : {self.color}")
c1 = vehicle("2009", "2014","Sonata","Red")

class car(vehicle):
    def __init__(self,make,model,brand,color,door):
        super().__init__(make,model,brand,color,door)
        self.door = door
    def car_detail(self):
        print(f"Make: {self.make}")
        print(f"Model: {self.model}")
        print(f"Brand : {self.brand}")
        print(f"Color : {self.color}")
        print(f"Door : {self.door}")
c1 = car("2009", "2014","Sonata","Red",4)
c1.car_detail()

#4
class BankAccount:
    def __init__(self, account_number, balance):
        self.account_number = account_number
        self.balance = balance

    def deposit(self, amount):
        self.balance = self.balance + amount
        print("Money deposited:", amount)

    def withdraw(self, amount):
        self.balance = self.balance - amount
        print("Money withdrawn:", amount)

account1 = BankAccount("123456789", 1000)

#5
class shape():
    def __init__(self):
        print("CAlculate ARea")
        
class circle(shape):
    def __init__(self,radius):
        super().__init__(radius)
        self.radius = radius
    def areaofcircle(self):
        print(f"Area of cricle : {3.14*self.radius**2}")
        
class triangle(shape):
    def __init__(self,base,height):
        super().__init(self,base,height)
        self.base = base
        self.height = height
    def areaoftriangle(self):
        print(f"Area of triangle : {0.5*self.base*self.height}")
        
c1 = circle(5)
c1.areaofcircle()
t1 = triangle(5,10)
t1.areaoftriangle()

#6
class employee():
    def __init__(self,name,salary):
        self.name = name
        self.salary = salary
    def annual_salary(self):
        print(f"Name : {self.name} \n Annual Salary : {self.salary*12}")
class manager(employee):
    def __init__(self,name,salary,department):
        super().__init__(name,salary,department)
        self.department = department
    def annual_salary(self):
        bonus = 3000
        return (self.salary*12)+ bonus
m1 = manager("Sarim","7000","HR")
m1.annual_salary()

#7
class book():
    def __init__(self,title,author):
        self.title = title
        self.author = author
    def book_info(self):
        print(f"Title : {self.title} \n Author : {self.author}")
        
class e_books(book):
    def __init__(self,title,author,price):
        super().__init__(title,author,price)
        self.price = price
    def book_info(self):
        print(f"Title : {self.title} \n Author : {self.author} \n Price : {self.price}")
        

#8
class Animal():
    def __init__(self,species,sound):
        self.species = species
        self.sound = sound
    def sound(self):
        print(f"Sound : {self.sound}")
        
class Dog(Animal):
    def __init__(self,species,sound,color):
        super().__init__(species,sound,color)
        self.color = color
    def sound(self):
        print(f"Sound : {self.sound} \n Color : {self.color}")
        
d1 = Dog("dog","bark","black")
d1.sound()

#9

#10
class product():
    def __init__(self,name,product_id,price):
        self.name = name
        self.product_id = product_id
        self.price = price
    def total_price(self):
        print(f"Total price = {self.price*self.quantity} ")
class personalcareproduct(product):
    def __init__(self,name,product_id,price,warranty_card):
        super().__init__(name,product_id,price,warranty_card)
        self.warranty_card = warranty_card
    def total_price(self):
        print(f"Total price = {self.price*self.quantity + self.warranty_card} ")


#11
class BankAccount:
    def __init__(self, acc_no, name, balance):
        self.acc_no = acc_no
        self.name = name
        self.balance = balance

    def deposit(self, amount):
        self.balance = self.balance + amount
        print(f"Deposited:{self.amount}")

    def withdraw(self, amount):
        self.balance = self.balance - amount
        print(f"Withdrawn:{self.amount}")

    def get_balance(self):
        return self.balance

    def transfer(self, amount, other_account):
        self.balance = self.balance - amount
        other_account.balance = other_account.balance + amount
        print(f"Money transferred: {self.amount}")

    def show_balance(self):
        print(f" {self.name} Balance: {self.balance}")
        
#12
