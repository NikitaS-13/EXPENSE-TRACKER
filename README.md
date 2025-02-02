# EXPENSE-TRACKER

# Expense tracker in Python

# Function to add an expense
def add_expense(expenses, date, description, amount):
    expenses.append({'date': date, 'description': description, 'amount': amount})

# Function to view all expenses
def view_expenses(expenses):
    for expense in expenses:
        print(f"Date: {expense['date']}, Description: {expense['description']}, Amount: {expense['amount']}")

# Function to get the total amount of expenses
def total_expenses(expenses):
    total = sum(expense['amount'] for expense in expenses)
    return total

# Main program
expenses = []

while True:
    print("\nExpense Tracker")
    print("1. Add Expense")
    print("2. View Expenses")
    print("3. Total Expenses")
    print("4. Exit")

    choice = input("Choose an option: ")

    if choice == '1':
        date = input("Enter date (YYYY-MM-DD): ")
        description = input("Enter description: ")
        amount = float(input("Enter amount: "))
        add_expense(expenses, date, description, amount)
    elif choice == '2':
        view_expenses(expenses)
    elif choice == '3':
        total = total_expenses(expenses)
        print(f"Total Expenses: {total}")
    elif choice == '4':
        break
    else:
        print("Invalid choice. Please try again.")
