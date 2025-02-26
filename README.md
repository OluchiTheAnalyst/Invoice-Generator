# Invoice-Generator

### Project Overview
I want build a Python program that takes user input such as name, item purchased, quantity, price per unit, and date and generate a formatted invoice using f-strings and other string formatting techniques.

### Tools
- Python - Jupyter [Click here](http://localhost:8888/notebooks/Invoice%20Project.ipynb)

### Code
```Python
# I want build a Python program that takes user input (such as name, item purchased, quantity, price per unit, and date)
# and generates a formatted invoice using f-strings and other string formatting techniques.
#  GET USER INPUT
name = input("What is your name? ")
item = input("What did you buy? ")

while True:
    try:
        quantity = int(input("Enter quantity: "))
        if quantity > 0:
            break
        else:
            print("Quantity must be a valid positive number.")
    except ValueError:
        print("Please enter a valid number.")

while True:
    try:
        price = float(input("Enter price per unit ($): "))
        if price > 0:
            break
        else:
            print("Price must be a positive number.")
    except ValueError:
        print("Please enter a valid number.")

# CALCULATIONS
total_cost = price * quantity
sales_tax = total_cost * 0.07
total_amount = total_cost + sales_tax

purchase_date = input("Enter date of purchase (DD-MMM-YYYY): ")

invoice = f'''

Customer Name: {name}
Item Purchased: {item}
Quantity: {quantity}
Price per Unit: ${price:.2f}
Tax: ${sales_tax:.2f}
Total Cost: ${total_cost:.2f}
Amount Payable: ${total_amount:.2f}
Date: {purchase_date}

'''

print(invoice)

```

