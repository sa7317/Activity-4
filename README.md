# Activity-4
Pizza Order System:

class Pizza:
    __slots__=["__cheese","__meat","__veggies"]

    def __init__(self):
        self.__cheese="cheese"
        self.__meat="meat"
        self.__veggies="veggies"


    def get_cheese(self):
        return self.__cheese

    def get_meat(self):
        return self.__meat

    def get_veggies(self):
        return self.__veggies

class Pizza:
    def __init__(self, meat,cheese, veggie, price):
        self.cheeses = cheese
        self.meats = meat
        self.veggies = veggie
        self.price = price

    def calculate_price(self):
        for i in (self.cheese):
            self.price += i.price
        for i in (self.meat):
            self.price += i.price
        for i in (self.veggie):
            self.price += i.price
        return self.price

    def name_list(self, list):
        names = []
        for i in list:
            names.append(i.name)
        return names
    
    def get_price(self):
        return self.price

    def __str__(self):
        self.calculate_price()
        names_Ch = self.name_list(self.cheese)
        names_Mt = self.name_list(self.meat)
        names_Vg = self.name_list(self.veggie)
        return f"cheese: {names_Ch}, meat: {names_Mt}, veggie: {names_Vg}, price: {self.price}"
        

class Topping:
    __slots__=["__Fresh_Mozzarella","__Shredded_Cheese","__Cheddar","__Pepperoni","__Sausage","__Bacon","__Meatball","__None","__Mushrooms","__Bell_Peppers","__Jalapeno_Peppers","__Pineapple"]

    def __init__(self):
        #cheese
        self.__Fresh_Mozzarella="Fresh Mozzarella"
        self.__Shredded_Cheese="Shredded Cheese"
        self.__Cheddar="Cheddar"
        #meat
        self.__Pepperoni="Pepperoni"
        self.__Sausage="Sausage"
        self.__Bacon="Bacon"
        self.__Meatball="Meatball"
        #none  for meat and veggies
        self.__None="None"
        #veggies
        self.__Mushrooms="Mushrooms"
        self.__Bell_Peppers="Bell Peppers"
        self.__Jalapeno_Peppers="Jalapeno Peppers"
        self.__Pineapple="Pineapple"

    def get_morzzarella(self):
        return self.__Fresh_Mozzarella

    def get_sheredded_chesse(self):
        return self.__Shredded_Cheese

    def get_cheddar(self):
        return self.__Cheddar

    def get_pepperoni(self):
        return self.__Pepperoni

    def get_sausage(self):
        return self.__Sausage

    def get_bacon(self):
        return self.__Bacon

    def get_meatball(self):
        return self.__Meatball

    def get_none(self):
        return self.__None

    def get_mushroom(self):
        return self.__Mushrooms

    def get_bell_peppers(self):
        return self.__Bell_Peppers

    def get_jalapeno_peppers(self):
        return self.__Jalapeno_Peppers

    def get_pineapple(self):
        return self.__Pineapple

import toppings as tp  
class main:     __slots__ = ["__pizza1Toppings", "__pizza2Toppings", "__pizza1Price", "__pizza2Price"]          
def __init__(self):        
    self.__pizza2Toppings = []         
    self.__pizza1Price = 5         
    self.__pizza2Price = 5                  
def Pizzaorder1(self):                 
    userToppings = tp.Toppings()         
    print("Welcome to Pizza Factory, where all orders include two pizzas")         
    print("For your first pizza....")                 
    cheeseType = 'O'         
    while (cheeseType in ['O', 'o', '0']):                         
                   
        print(userToppings.getToppingOptionPrintLine('cheese'))             
        cheeseType = input("Choose one type of cheese (O for options): ")            
           
        for cheeseOption in cheeseType.split():                  
            if cheeseOption not in ['O', 'o', '0']:                     
                name, price = userToppings.getCheeseToppingNamePrice(cheeseOption)                     
                self.__pizza1Toppings.append([name, price])                                                              
                meatType = 'O'         
                while (meatType in ['O', 'o', '0']):                    
                                 
                    print(userToppings.getToppingOptionPrintLine('meat'))             
                    meatType = input("Choose one type of meat (O for options): ")             
                                 
                    for meatOption in meatType.split():                 
                        if meatOption not in ['O', 'o', '0']:                     
                            name, price = userToppings.getMeatToppingNamePrice(meatOption)                     
                            self.__pizza1Toppings.append([name, price])                 
    else:                     
        print(userToppings.getToppingOptionPrintLine('meat'))                     
        meatType = input("Choose one type of meat (O for options): ")                                              
        vegType = 'O'         
        while (vegType in ['O', 'o', '0']):                        
                    
            print(userToppings.getToppingOptionPrintLine('veg'))             
            vegType = input("Choose one type of veg (O for options): ")             
                        
            for vegOption in vegType.split():                  
                if vegOption not in ['O', 'o', '0']:                     
                    name, price = userToppings.getVegToppingNamePrice(vegOption)                     
                    self.__pizza1Toppings.append([name, price])                                                       
def Pizzaorder2(self):                
    userToppings = tp.Toppings()                 
    print("For your second pizza....")                 
    cheeseType = 'O'        
    while (cheeseType in ['O', 'o', '0']):                       
                  
        print(userToppings.getToppingOptionPrintLine('cheese'))             
        cheeseType = input("Choose one type of cheese (O for options): ")             
              
        for cheeseOption in cheeseType.split():                  
            if cheeseOption not in ['O', 'o', '0']:                     
                name, price = userToppings.getCheeseToppingNamePrice(cheeseOption)                     
                self.__pizza2Toppings.append([name, price])                                                             
                meatType = 'O'      
                while (meatType in ['O', 'o', '0']):                         
                    print(userToppings.getToppingOptionPrintLine('meat'))             
                      
                    meatType = input("Choose one type of meat (O for options): ")           
                               
                    for meatOption in meatType.split():                 
                        if meatOption not in ['O', 'o', '0']:                     
                            name, price = userToppings.getMeatToppingNamePrice(meatOption)                     
                            self.__pizza2Toppings.append([name, price])                 
    else:                     
        print(userToppings.getToppingOptionPrintLine('meat'))                     
        meatType = input("Choose one type of meat (O for options): ")                                              
        vegType = 'O'        
        while (vegType in ['O', 'o', '0']):                         
            print(userToppings.getToppingOptionPrintLine('veg'))             
                         
            vegType = input("Choose one type of veg (O for options): ")             
                 
            for vegOption in vegType.split():                  
                if vegOption not in ['O', 'o', '0']:                     
                    name, price = userToppings.getVegToppingNamePrice(vegOption)                     
                    self.__pizza2Toppings.append([name, price])                                                          
                    print(Pizzaorder2)    
def pizzaorder3(self):        
    print(Pizzaorder1)         
    toppingsList = []         
    for toppings in self.__pizza1Toppings:                              
        name, price = toppings             
        if name not in ['None']:                                 
            self.__pizza1Price += float(price)                 
            toppingsList.append(name)         
            print("One Pizza with {}: {}".format(", ".join(toppingsList),  self.__pizza1Price))                  
            print(Pizzaorder2)        
            toppingsList = []         
            for toppings in self.__pizza2Toppings:                               
                name, price = toppings             
                if name not in ['None']:                             
                    self.__pizza2Price += float(price)                 
                    toppingsList.append(name)         
                    print("One Pizza with {}: {}".format(", ".join(toppingsList), self.__pizza2Price))         
                    print("Total due: ${}".format(str(self.__pizza1Price + self.__pizza2Price)))              
                    myPizza = main() 
                    myPizza.getPizza1Order() 
                    myPizza.getPizza2Order() 
                    myPizza.printOrder()
 

 
from toppings import Topping
from pizza import Pizza
toppings=Topping()
pizza=Pizza()

toppings_dict={toppings.get_morzzarella() : "Fresh Mozzarellea(f)" , toppings.get_sheredded_chesse() : "Shredded Cheese(s)" , 
               toppings.get_cheddar() : "Cheddar(c)" , toppings.get_pepperoni() : "Pepperoni(p)" , toppings.get_sausage() : "Sausage(s)" , 
               toppings.get_bacon() : "Bacon(b)" , toppings.get_meatball() : "Meatball(m)"}

pizza_dict={pizza.get_cheese() : "Cheese Pizza" , pizza.get_meat(): "Meat Pizza" , pizza.get_veggies() : "Veggies Pizza"}
