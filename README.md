# Pet Inventory Application
The aim of this application is to utilize classes in buidling an application program that can store pet data in a file . It was part of a Python programming assignment

## Project Details
The program is designed with a menu that allows the following:
  1. Add a new Pet
  2. Compute and print current weight of all pets in the file
  3. Print all pet information for every pet in the file
  4. Exit the application
 
To add a pet the user is prompted fro the pet's name, age, birth weight, pet's owner's name and address. There are 3 classes of animals - Mammal, Fish and Amphibian. The user is asked specific questions for each class.

## Technology Used
Python

## Example Code

class Amphibian(Pet):
    
    #initialize instance variables
    def __init__(self,n,a,w,pr,v):
        super().__init__(n,a,w,pr)
        self.__name = n
        self.__age = a
        self.__weight = w
        self.__isvenomous = v
     
    #initialize the acessor methods
    def get_isvenomous(self):
        return self.__isvenomous
        
    #initialize the mutator methods
    def set_isvenomous(self):
        self.__isvenomous = v
            
    def __str__(self):
        stv = super().__str__()
        stv += " \n is Venomous: {} ".format(self.__isvenomous)
        return stv
    

    def weight_gain(self):
        if self.__age < 120:
            return "{} is to young too have gain weight".format(self.__name)
        else:
            if self.__age < 360:
                wg = ((self.__age // 120) * (0.03 * self.__weight))+ self.__weight
            else:
                wg = (3 * (0.03 * self.__weight))+ self.__weight
            return "{}'s weight gain is {}".format(self.__name,wg)
            
 
 ## Future Updates
 The following improvements will be made:
 1. Expand the program to include any type of pets
 2. Store data in MySQL
 3. Have a GUI and Web Interface
