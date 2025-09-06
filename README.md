# Codemetric
A command-line calculator to perform basic arithmetic operations.(Task 1 of python programmer)

CODE:

 def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Error: Division by zero is not allowed!"

def show_keypad():
    print("\nCalculator Layout:")
    print("------------------")
    print("7   8   9   +")
    print("4   5   6   -")
    print("1   2   3   *")
    print("0   .   =   /")
    print("------------------")

def calculator():
    print("🔢 Welcome to the Command-line Calculator 🔢")

    while True:
        show_keypad()

        try:
            num1 = float(input("\nEnter first number: "))
            op = input("Enter operation (+, -, *, /): ")
            num2 = float(input("Enter second number: "))

            if op == "+":
                result = add(num1, num2)
            elif op == "-":
                result = subtract(num1, num2)
            elif op == "*":
                result = multiply(num1, num2)
            elif op == "/":
                result = divide(num1, num2)
            else:
                print("❌ Invalid operation! Please enter +, -, *, or /")
                continue

            print(f"\n✅ Result: {num1} {op} {num2} = {result}")

        except ValueError:
            print("❌ Invalid input! Please enter valid numbers.")
            continue

        choice = input("\nDo you want to perform another calculation? (y/n): ").lower()
        if choice != "y":
            print("Exiting... Goodbye! 👋")
            break

# Run the calculator
calculator()


OUTPUT:

🔢 Welcome to the Command-line Calculator 🔢

Calculator Layout:
------------------
7   8   9   +
4   5   6   -
1   2   3   *
0   .   =   /
------------------

Enter first number: 6
Enter operation (+, -, *, /): -
Enter second number: 7

✅ Result: 6.0 - 7.0 = -1.0

Do you want to perform another calculation? (y/n): y

Calculator Layout:
------------------
7   8   9   +
4   5   6   -
1   2   3   *
0   .   =   /
------------------

Enter first number: 9
Enter operation (+, -, *, /): /
Enter second number: 0

✅ Result: 9.0 / 0.0 = Error: Division by zero is not allowed!

Do you want to perform another calculation? (y/n): N
Exiting... Goodbye! 👋
