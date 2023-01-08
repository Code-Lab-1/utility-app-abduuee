#Code-Lab 1 Utility App



#Importing python modules
from tabulate import tabulate
import random

#Printing the Logo of the vending machine
print("""
    \t\t ___     ___   ____   __ __  ______  _____
    \t\t|   \   /   \ |    \ |  |  ||      |/ ___/
    \t\t|    \ |     ||  _  ||  |  ||      (   \_
    \t\t|  D  ||  O  ||  |  ||  |  ||_|  |_|\__  |
    \t\t|     ||     ||  |  ||  :  |  |  |  /  \ |
    \t\t|     ||     ||  |  ||     |  |  |  \    |
    \t\t|_____| \___/ |__|__| \__,_|  |__|   \___|
                                          """)

print("\t\t\t   Oh Nuts! Donuts!")
print("\t\t\tGo Nuts with our Donuts!")

#Printing the MENU text
print()
print()
print('''
\t\t\t       ___           
\t\t\t |\/| |__  |\ | |  | 
\t\t\t |  | |___ | \| \__/ ''')  
print('--------------------------------------------------------------------------------')

#Storing the MENU in a list
data=[["[0] Original Donut -- $5.00","[10] Iced Latte -- $13.00"],
      ["[1] Glazed Donut -- $6.00", "[11] Iced Mocha -- $13.00"],
      ["[2] Chocolate Iced Donut -- $7.00", "[12] Hot Chocolate -- $11.00"],
      ["[3] Strawberry Iced Donut -- $7.00","[13] Frappé -- $16.00"],
      ["[4] Custard Cream Donut -- $8.00", "[14] Espresso -- $15.00"],
      ["[5] Red Velvet Donut -- $9.00", "[15] Americano -- $12.00"],
      ["[6] Boston Cream Donut -- $8.00", "[16] Cappuccino -- $16.00"],
      ["[7] Powdered Donut -- $6.00", "[17] Spanish Latte -- $18.00"],
      ["[8] Glazed Chocolate Donut -- $6.00", "[18] Caramel Macchiato -- $18.00"],
      ["[9] Sugar Coated Donut -- $7.00", "[19] Tea -- $10.00"],]

#Storing the SIDES MENU in a list
data2=[["[20] Water -- $2.00"],
       ["[21] Soft Drinks -- $5.00"],
       ["[22] Cookie -- $4.00"],
       ["[23] Cinnamon Roll -- $4.00"],
       ["[24] Glazed Mini -- $3.00"],
       ["[25] Croissant -- $5.00"]]
       
  
#Defining header names for the tabulate module
headers1 =["DONUTS", "HOT OR ICED DRINKS"]
headers2 =["SIDES"]

#To display the MENU table
print(tabulate(data, headers=headers1, tablefmt="fancy_grid"))
print()
print('________________________________________________________________________________')

#Storing all the available items in a dictionary 
stock = [
    {"item_code":0,
    "name":"Original Donut",
    "price":5.00,},
    
    {"item_code": 1,
     "name":"Glazed Donut",
     "price":6.00,},
    
    {"item_code": 2,
     "name":"Chocolate Iced Donut",
     "price":7.00,},
    
    {"item_code": 3,
     "name":"Strawberry Iced Donut",
     "price":7.00,},
    
    {"item_code": 4,
     "name":"Custard Cream Donut",
     "price":8.00,},
    
    {"item_code": 5,
     "name":"Red Velvet Donut",
     "price":9.00,},
    
    {"item_code": 6,
     "name":"Boston Cream Donut",
     "price":8.00,},
    
    {"item_code": 7,
     "name":"Powdered Donut",
     "price":6.00,},
    
    {"item_code": 8,
     "name":"Glazed Chocolate Donut",
     "price":6.00,},
    
    {"item_code": 9,
     "name":"Sugar Coated Donut",
     "price":7.00,},
    
    {"item_code": 10,
     "name":"Iced Latte",
     "price":13.00,},
    
    {"item_code": 11,
     "name":"Iced Mocha",
     "price":13.00,},
    
    {"item_code": 12,
     "name":"Hot Chocolate",
     "price":11.00,},
    
    {"item_code": 13,
     "name":"Frappé",
     "price":16.00,},
    
    {"item_code": 14,
     "name":"Espresso",
     "price":15.00,},
    
    {"item_code": 15,
     "name":"Americano",
     "price":12.00,},
    
    {"item_code": 16,
     "name":"Cappucciono",
     "price":16.00,},
    
    {"item_code": 17,
     "name":"Spanish Latte",
     "price":18.00,},
    
    {"item_code": 18,
     "name":"Caramel Macchiato",
     "price":18.00,},
    
    {"item_code": 19,
     "name":"Tea",
     "price":10.00,},
    
    {"item_code": 20,
     "name":"Water",
     "price":2.00,},
    
    {"item_code": 21,
     "name":"Soft Drinks",
     "price":5.00,},
    
    {"item_code": 22,
     "name":"Cookie",
     "price":4.00,},
    
    {"item_code": 23,
     "name":"Cinammon Roll",
     "price":4.00,},
    
    {"item_code": 24,
     "name":"Glazed Mini",
     "price":3.00,},
    
    {"item_code": 25,
     "name":"Croissant",
     "price":5.00,}]

#Storing a list of compliments in a list, so they randomly generate
compliments=["Lovely","Great","Irresistible","Splendid","Fantastic","Tremendous","Fair","Nice","Solid"]

#A list to store the user's orders 
items = []
totalcost = 0

#A function to take the order from the user
def choice(stock, items):
    while True:
        purchase = eval(input("\nEnter the item code of your choice: "))
        #Adding to the user's order list
        if purchase < len(stock):
            items.append(stock[purchase]) #Randomly generating nice comments 
            print("\nA {} Choice! Do you wish to add more?".format(random.choice(compliments)))
        else:
            print("\n\tINVALID ITEM CODE!") #The user gets to retry if there was a mistake
            retry = eval(input("\nEnter the item code of your choice: "))
            if retry < len(stock):
                items.append(stock[retry])
                print("\nA {} Choice! Do you wish to add more?".format(random.choice(compliments)))
        #Asking the user if they want to add more items or to proceed with billing
        more = input("Enter y if Yes, Enter n to Proceed: ")
        if more == "n":
            break
    #Displaying what the user has ordered so far    
    print('_____________________________________________________')
    print("\nYour Order is: ")
    for i in items:
        print(f"""
          --> {i["name"]} -- ${i['price']}""")
    #Displaying the total amount
    print(f"\nThe Total amount is == ${totalcost(items)}")
    
    print("\nWe Also Recommend...") #Recommending the user side items 
    print(tabulate(data2, headers=headers2, tablefmt="fancy_grid")) #Using tabulate to display the side menu
    print("\nWould you like to get anything?")
    purchase_side = input("Enter y if Yes, Enter n to Proceed: ")
    if purchase_side == "y":
        side = int(input("\nEnter the item code of your choice: "))
        if side < len(stock):
            items.append(stock[side]) #Ordering a side will print this text with a random compliment
            print("\nA {} Choice! Will be added to your order.".format(random.choice(compliments)))
        else:
            print("\n\tINVALID ITEM CODE!")
   
    if purchase_side == "n":
        print("\nAlrighty! Let's move on!")
    else:
        run = False
    #Asking the user to insert the sufficient amount considering the total         
    print(f"\n\nThe Total amount is == ${totalcost(items)}") 
    amount = eval(input(("\nPlease insert the sufficient amount: ")))
    change = amount-totalcost(items)
    #Displaying a text saying whether the payment was successful or not
    if amount >= totalcost(items):
        print("_____________________________________________________")
        print("\nPayment Successful!!")
        print("\nThe Purchased Items are ready to collect!") #Displaying a text saying that the items are dispensed 
        print("The Total change is: $",change) #Displaying a text telling the user how much change they have received
        print("\nThankyou! Visit Us Again!")
    else:
        print("\nPayment Unsuccessful! Insert Sufficient Amount!")
        quit()
        
    #To print the bill
    print("_____________________________________________________")
    print("\nWould you like to print the receipt?")
    check = input("Enter y if Yes, Enter n if No: ")
    if check == "y":
        print("_____________________________________________________")
        print(bill(items, invoice)) #Calling the bill function
        print(f"          Inserted Amount -- ${amount}")
        print(f"          Change -- ${change}")
        print("\n\t>-|->-|->-|-> THANK YOU! <-|-<-|-<-|-<\n")
        print("_____________________________________________________")
    elif check == "n": #If the user wishes to be environment friendly
        print("\nStay Environment friendly and Enjoy your Donuts ;)")
    else:
        print("\nINVALID ATTEMPT!")
    
def totalcost(items): #A function to sum the total of the entire order
    totalcost = 0
    for i in items:
        totalcost += i["price"]
    return totalcost

#Printing the logo of the vending machine on the receipt
invoice = """
\t
                 __  __         ___ __ 
                |  \/  \|\ ||  | | (_  
                |__/\__/| \|\__/ | __) \n
          ----------------------------------

"""
def bill(items, invoice): #A function to display the order in the form of a receipt
    
    for i in items:
        invoice += f"""
          {i["name"]} --- ${i['price']}
          """
    
    invoice += f"""
          ----------------------------------
          TOTAL ==== ${totalcost(items)}"""
    return invoice


#Calling the main function 
choice(stock, items) 
    




