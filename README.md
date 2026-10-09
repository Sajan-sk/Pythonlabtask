# Pythonlabtask
lab1
Q1
name = input("Enter your name: ")
print("Hello,", name)
Q2
hours = float(input("Enter hours worked: "))
rate = float(input("Enter hourly rate: "))

gross_pay = hours * rate

print("Gross Pay:", gross_pay)
Q3
celsius = float(input("Enter temperature in Celsius: "))

fahrenheit = (celsius * 9 / 5) + 32

print("Temperature in Fahrenheit:", fahrenheit)
Q4
a = float(input("Enter first number: "))
b = float(input("Enter power: "))

result = a ** b

print("Result:", result)
Q5
age = 20
item = 5

print("Age:", age)
print("Items:", item)

age = float(age)
item = float(item)

print("Age:", age)
print("Items:", item)

print("Age type:", type(age))
print("Item type:", type(item))

Labtask2
Q1
hours = float(input("Enter hours worked: "))
rate = float(input("Enter hourly rate: "))

if hours <= 40:
    pay = hours * rate
else:
    regular_pay = 40 * rate
    overtime_hours = hours - 40
    overtime_pay = overtime_hours * rate * 1.5
    pay = regular_pay + overtime_pay

print("Total Pay:", pay)

Q2
name = input("Enter student name: ")
roll_no = input("Enter roll number: ")

marks = []

for i in range(1, 6):
    mark = float(input(f"Enter marks for subject {i}: "))
    marks.append(mark)

total = sum(marks)
percentage = total / 500 * 100

if percentage >= 80:
    grade = "A+"
elif percentage >= 70:
    grade = "A"
elif percentage >= 60:
    grade = "B"
elif percentage >= 50:
    grade = "C"
elif percentage >= 40:
    grade = "D"
else:
    grade = "F"

if percentage >= 40 and all(mark >= 40 for mark in marks):
    result = "Pass"
else:
    result = "Fail"

print("\n===== STUDENT MARKSHEET =====")
print("Name:", name)
print("Roll Number:", roll_no)

for i, mark in enumerate(marks, start=1):
    print(f"Subject {i}: {mark}")

print("Total Marks:", total, "/ 500")
print("Percentage:", percentage, "%")
print("Grade:", grade)
print("Result:", result)

Labtask3
Q1
marks = []

for i in range(1, 6):
    mark = float(input(f"Enter marks for subject {i}: "))
    marks.append(mark)

total = sum(marks)
percentage = total / 500 * 100

if percentage >= 80:
    grade = "A+"
elif percentage >= 70:
    grade = "A"
elif percentage >= 60:
    grade = "B"
elif percentage >= 50:
    grade = "C"
elif percentage >= 40:
    grade = "D"
else:
    grade = "F"

if all(mark >= 40 for mark in marks):
    result = "Pass"
else:
    result = "Fail"

print("Total Marks:", total)
print("Percentage:", percentage, "%")
print("Grade:", grade)
print("Result:", result)

Q2
name = input("Enter your name: ")

print("Uppercase:", name.upper())
print("Lowercase:", name.lower())
print("Number of characters:", len(name))

if len(name) > 0:
    print("First character:", name[0])
    print("Last character:", name[-1])

    Q3
    numbers = []

for i in range(10):
    number = int(input(f"Enter number {i + 1}: "))
    numbers.append(number)

total = sum(numbers)
average = total / 10
largest = max(numbers)
smallest = min(numbers)

even = 0
odd = 0

for number in numbers:
    if number % 2 == 0:
        even += 1
    else:
        odd += 1

print("Sum:", total)
print("Average:", average)
print("Largest:", largest)
print("Smallest:", smallest)
print("Even numbers:", even)
print("Odd numbers:", odd)

Q4
balance = 50000

while True:
    print("\n===== ATM MENU =====")
    print("1. Check Balance")
    print("2. Deposit")
    print("3. Withdraw")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        print("Current Balance:", balance)

    elif choice == "2":
        amount = float(input("Enter deposit amount: "))

        if amount > 0:
            balance += amount
            print("Deposit successful.")
            print("New Balance:", balance)
        else:
            print("Enter a valid amount.")

    elif choice == "3":
        amount = float(input("Enter withdrawal amount: "))

        if amount <= 0:
            print("Enter a valid amount.")
        elif amount <= balance:
            balance -= amount
            print("Withdrawal successful.")
            print("Remaining Balance:", balance)
        else:
            print("Insufficient balance.")

    elif choice == "4":
        print("Thank you for using the ATM.")
        break

    else:
        print("Invalid choice. Try again.")

        Q5
        
n = int(input("Enter a number: "))

for i in range(1, n + 1):
    print("\nTable of", i)

    for j in range(1, 11):
        print(i, "x", j, "=", i * j)

        Labtask4
        Q1
         my_list = [3, 1, 0, 9, 5, 2, 6, 4, 9, 8, 7]

smallest = my_list[0]

for number in my_list:
    if number < smallest:
        smallest = number

print("Smallest number:", smallest)

Q2
my_list = [3, 1, 0, 9, 5, 2, 6, 4, 9, 8, 7]

total = 0

for number in my_list:
    total += number

average = total / len(my_list)

print("Sum:", total)
print("Average:", average)

Q3
students = ["Ali", "Ahmed", "Sara", "Ayesha", "Bilal"]

name = input("Enter student name: ")

if name.lower() in [student.lower() for student in students]:
    print("Student Found")
else:
    print("Student Not Found")

    Q4
    shopping = []

for i in range(5):
    item = input(f"Enter shopping item {i + 1}: ")
    shopping.append(item)

print("\nShopping List:")

for item in shopping:
    print(item)

    Labtask5
    Q1
    name = input("Enter student name: ")
age = int(input("Enter age: "))
program = input("Enter program: ")
marks = float(input("Enter marks: "))

student = (name, age, program, marks)

print("\nStudent Information")
print("Name:", student[0])
print("Age:", student[1])
print("Program:", student[2])
print("Marks:", student[3])
print("Complete Tuple:", student)

Q2
sentence = input("Enter a sentence: ")

characters = len(sentence)
words = len(sentence.split())
spaces = sentence.count(" ")
digits = sum(1 for ch in sentence if ch.isdigit())

vowels = 0

for ch in sentence.lower():
    if ch in "aeiou":
        vowels += 1

print("Number of characters:", characters)
print("Number of words:", words)
print("Number of vowels:", vowels)
print("Number of spaces:", spaces)
print("Number of digits:", digits)

Q3employees = []

for i in range(3):
    print("\nEmployee", i + 1)

    name = input("Enter name: ")
    age = int(input("Enter age: "))
    salary = float(input("Enter salary: "))

    employee = (name, age, salary)
    employees.append(employee)

print("\n===== EMPLOYEE RECORDS =====")

for employee in employees:
    print("Name:", employee[0])
    print("Age:", employee[1])
    print("Salary:", employee[2])
    print("--------------------")

    Q3
    numbers = (10, 15, 20, 25, 30, 35, 40)

even = 0
odd = 0

for number in numbers:
    if number % 2 == 0:
        even += 1
    else:
        odd += 1

print("Even numbers:", even)
print("Odd numbers:", odd)


