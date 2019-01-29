def hotel_cost(hcnum, nignum):#create function to calculate cost of the hotel
    costHotel = hcnum * nignum#variable to store input from user
    return costHotel#return variable 
hcnum = int(input("What is the cost per night of the hotel?: "))#get user input
nignum = int(input("How many nigths are you going to stay in the hotel: ?"))#get user input

def plane_cost():#create function
    
    if choice == "A":#if statement to compare user input 
        costPlane = 1000
    elif choice == "B":
        costPlane = 2000
    elif choice == "C":
        costPlane = 3000
    else:
        costPlane = 4000
    return costPlane#store data in variable
print("A = Destination A cost R1000 to fly to")
print("B = Destination B cost R2000 to fly to")
print("C = Destination C cost R3000 to fly to")
print("D = Destination D cost R4000 to fly to")
choice =input("Please choose destination by typing A,B,C or D:").capitalize()#get user input

def car_cost(days):#create function to calculate the cost of car rental
    costCar = days * 100#variable to store data
    return costCar#return variable
days = int(input("How many days will you need a car for?: "))#get user input

print("Your hotel cost is: R"+ str(hotel_cost(hcnum,nignum)))
print("The cost of your plane ticket is: R" + str(plane_cost()))
print("The cost of renting a car for " + str(days) + " days will be: R" + str(car_cost(days)))

def holiday_cost(hotel,plane,car):#create function to calculate cost of holiday
    costHoliday = hotel + plane + car#create variable to store data
    return costHoliday#return varialbe

hotel = hotel_cost(hcnum, nignum)
plane = plane_cost()
car = car_cost(days)
print("The total cost of your holiday will be: R" + str(holiday_cost(hotel,plane,car)))
