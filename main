from datetime import datetime

books = {}
def add_book():
    print("\n     *ADD BOOK*      ")
    name = input("Enter book name: ").strip()

    if name in books:
        print(" Book already exists.")
    else:
        books[name] = {
            "available": True,
            "student": None,
            "issue_date": None,
            "days": 0
        }
        print(f" '{name}' added successfully!")

def show_books():
    print("\n      *BOOK LIST*      ")

    if not books:
        print("No books available.")
        return

    for book, info in books.items():
        if info["available"]:
            print(f" {book} → Available")
        else:
            print(f" {book} → Issued to {info['student']}")


def issue_book():
    print("\n*       ISSUE BOOK*      " )
    show_books()

    name = input("\nEnter book name: ").strip()

    if name not in books:
        print("Book not found.")
        return

    if not books[name]["available"]:
        print(" Book already issued.")
        return

    student = input("Enter student name: ").strip()

    try:
        days = int(input("Enter number of days: "))
    except ValueError:
        print(" Invalid number.")
        return

    books[name]["available"] = False
    books[name]["student"] = student
    books[name]["issue_date"] = datetime.now()
    books[name]["days"] = days

    print(f" Book issued to {student} for {days} days.")

def calculate_fine(late_days):
    fine = 0

    for i in range(1, late_days + 1):
        fine += 10 * i  

    return fine

def return_book():
    print("\n====== RETURN BOOK ======")
    name = input("Enter book name: ").strip()

    if name not in books:
        print(" Book not found.")
        return

    if books[name]["available"]:
        print(" Book was not issued.")
        return

    issue_date = books[name]["issue_date"]
    allowed_days = books[name]["days"]

    used_days = (datetime.now() - issue_date).days

    print(f"\n Allowed Days: {allowed_days}")
    print(f" Used Days: {used_days}")

    if used_days > allowed_days:
        late_days = used_days - allowed_days
        fine = calculate_fine(late_days)

        print(f" Late by {late_days} days.")
        print(f" Fine: ₹{fine}")
    else:
        print(" Returned on time. No fine.")

    # 
    books[name] = {
        "available": True,
        "student": None,
        "issue_date": None,
        "days": 0
    }

    print("📗 Book returned successfully!")


def show_notice():
    print("""
LIBRARY FINE POLICY 

1st Week  → ₹10/day/book
2nd Week  → ₹20/day/book
3rd Week  → ₹60/day/book
... continues increasing

 Late returns will be fined accordingly.
""")

def library():
    while True:
        print("""     *LIBRARY MENU*

1. Add Book
2. Show Books
3. Issue Book
4. Return Book
5. Fine Policy
6. Exit
""")

        try:
            choice = int(input("Enter choice (1-6): "))
        except ValueError:
            print(" Enter a valid number.")
            continue

        if choice == 1:
            add_book()
        elif choice == 2:
            show_books()
        elif choice == 3:
            issue_book()
        elif choice == 4:
            return_book()
        elif choice == 5:
            show_notice()
        elif choice == 6:
            print("\n🙏 Thank you for using the Library System!")
            break
        else:
            print("Invalid choice.")


# Run program
library()
