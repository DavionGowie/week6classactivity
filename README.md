# List of student records stored as tuples (ID, Name, Grade)
students = [
    (101, "Alice", "A"),
    (102, "Bob", "B"),
    (103, "Charlie", "A"),
]

while True:
    print("\n1. Display Students")
    print("2. Search Student")
    print("3. Add Student")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":  # Display all students
        print("\nStudent Records:")
        print("-----------------")
        for student in students:
            print(f"ID: {student[0]}, Name: {student[1]}, Grade: {student[2]}")
        print("-----------------\n")

    elif choice == "2":  # Search student by ID
        search_id = input("Enter Student ID to Search: ")
        if search_id.isdigit():
            search_id = int(search_id)
            found = False
            for student in students:
                if student[0] == search_id:
                    print(f"\nStudent Found: ID: {student[0]}, Name: {student[1]}, Grade: {student[2]}\n")
                    found = True
                    break
            if not found:
                print("\nStudent Not Found!\n")
        else:
            print("\nInvalid Input! Please enter a valid numeric ID.\n")

    elif choice == "3":  # Add a new student
        student_id = input("Enter Student ID: ")
        if student_id.isdigit():
            student_id = int(student_id)
            name = input("Enter Student Name: ")
            grade = input("Enter Student Grade: ").upper()

            students.append((student_id, name, grade))  # Append a new tuple
            print("\nStudent Added Successfully!\n")
        else:
            print("\nInvalid Input! Student ID must be a number.\n")

    elif choice == "4":  # Exit the program
        print("Exiting Program...")
        break

    else:
        print("\nInvalid Choice! Try Again.\n")
        

employee_management = [
    ("akeem", "department"),
    ("Bobby", "department"),
    ("Charls", "department"),
    ]

while True:
    print("\n4. Employees")
    print("5. search by name")
    print("6. add empoyee")
    print("exit")
 
    selection = input("Enter your selection: ")

    if selection == "4":  # Display all employee
        print("\nEmployee Records:")
        print("-----------------")
        for employee in employee_management:
            print(f"ID: {employee[0]}, Name: {employee[1]}, Grade: {employee[1]}")
        print("-----------------\n")

    elif selection == "5":  # Search employee by ID
        search_name = input("Enter employee name to Search: ").strip().lower()
        found = False
        for employee in employee_management:
            if employee[0].lower() == search_id:
                print(f"\nEmployee Found: name: {Employee[0]}, Department: {employee[1]}\n")
                found = True
                break
        if not found:
            print("\nEmployee Not Found!\n")

    elif selection == "6":  # Add a new employee
        name = input("Enter employee Name: ")
        department = input("Enter employee department: ").upper()

        employee.append((employee_id, name, grade))  # Append a new tuple
        print("\nEmployee Added Successfully!\n")
    else:
        print("\nInvalid Input! Employee ID must be a number.\n")

    if selection == "end":  # Exit the program
        print("Exiting Program...")
        break

else:
    print("\nInvalid Choice! Try Again.\n")
