# -Project1
#write a code to calculate pythagoras theorem

import math
def find_missing_side():
    missing = input("Which side is missing? (a, b, or c)").lower()
         
    if missing == 'c':  #Hypothanus missing
         a = float(input("Enter the value of side a: "))
         b = float(input("Enter the value of side b: "))
         c = math.sqrt(a**2 + b**2)
         print("The hypothanus is:", c)

    elif missing == 'a': #Adjacent missing
         b = float(input("Enter the value of side b: "))
         c = float(input("Enter the value of side c:, "))

    #incase error value is input
        
         if c <= b:
          print("Error:Hypothanus must be greater than the other sides. ")
          return
         a = math.sqrt(c**2 - b**2) #formula for Adjacent
         print("The adjacent side is:", a)
    
    elif missing == 'b':
         a = float(input("Enter the value of side a: "))
         c = float(input("Enter the value of side c:, "))

    #incase error value is input
         if a >= c:
           print("Error:Hypothanus must be greater than the other sides ")
           return
         b = math.sqrt(c**2 - a**2) #formula for hypothanus
         print("The opposite side is:", b)
 
     # Run the function
find_missing_side()
