# Simple Python Calculator

A simple Python-based calculator that allows users to perform basic arithmetic operations such as addition, subtraction, multiplication, and division. The program runs in a continuous loop, prompting users for input until they choose to exit.

## Features

- Perform basic arithmetic operations:
  - Addition
  - Subtraction
  - Multiplication
  - Division (with error handling for division by zero)
- Easy-to-use command-line interface.
- Continuously asks for inputs until the user chooses to exit.

## Requirements

- Python 3.x (Tested on Python 3.8+)

## Installation

To use this project, follow the steps below:

1. Clone the repository or download the `calculator.pu` file:

   ```bash
   git clone https://github.com/pasindujayakodi77/simple-python-calculator.git

   
Select operation:
1. Add
2. Subtract
3. Multiply
4. Divide
5. Exit
Enter choice(1/2/3/4/5): 1
Enter first number: 10
Enter second number: 5
10.0 + 5.0 = 15.0

Select operation:
1. Add
2. Subtract
3. Multiply
4. Divide
5. Exit
Enter choice(1/2/3/4/5): 5
Exiting calculator. Goodbye!

# Function for addition
def add(x, y):
    return x + y

# Function for subtraction
def subtract(x, y):
    return x - y

# Function for multiplication
def multiply(x, y):
    return x * y

# Function for division
def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Error! Division by zero."

# Function to print the menu
def print_menu():
    print("\nSelect operation:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")
    print("5. Exit")

# Main calculator function
def calculator():
    while True:
        print_menu()

        # Take input from the user
        choice = input("Enter choice(1/2/3/4/5): ")

        # If the user chooses to exit
        if choice == '5':
            print("Exiting calculator. Goodbye!")
            break

        # Check if the user entered a valid choice
        if choice in ['1', '2', '3', '4']:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))

            if choice == '1':
                print(f"{num1} + {num2} = {add(num1, num2)}")
            elif choice == '2':
                print(f"{num1} - {num2} = {subtract(num1, num2)}")
            elif choice == '3':
                print(f"{num1} * {num2} = {multiply(num1, num2)}")
            elif choice == '4':
                print(f"{num1} / {num2} = {divide(num1, num2)}")
        else:
            print("Invalid input. Please try again.")

# Run the calculator
if __name__ == "__main__":
    calculator()
