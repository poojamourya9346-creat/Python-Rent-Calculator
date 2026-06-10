# Python-Rent-Calculator
This is my code to calculate rent.
# Rent Calculator
# Input
# Expenses = ??
# Calculate 
# Per person name wise divide kar denge 


#*********** INPUT ****************

rent = int(input("Please enter the rent of your flat/room: "))
food = int(input("Please enter your food expenses per month: "))
electricity_units = int(input("Please enter your electricity unit per month: "))
charge_per_unit = int(input("Please enter charge per unit rate of your area: "))
persons = int(input("Please enter the number of persons staying in your flat: "))


#************* TAKING NAMES *****************

names = []

for i in range(persons):
    name = input(f"Enter name of a person{i+1}: ")
    names.append(name)
    
    
#************ Calculating Electricity Bill **********

electricity_bill = electricity_units * charge_per_unit

#********** Total expense Calculation *************

total_expense = rent + food + electricity_bill

#********* PER PERSON BILL *****************

per_person = total_expense / persons

#*********** PRINTING SUMMARY *****************

print("\n--------EXPENSE SUMMARY----------")
print(f"Rent: ",{rent})
print(f"Food Expense: ",{food})
print(f"Electricity bill: ",{electricity_bill})
print(f"Total Expense: ",{total_expense})


#********* PRINTING NAMES ***********
print()
for name in names:
    print(f"{name} has to pay : {per_person}")

#*********** OUTPUT ***********
