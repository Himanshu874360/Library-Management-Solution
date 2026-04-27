# Library-Management-Solution

## 📌 Description
This is a simple **Library Management System** built using Python.  
It allows users to manage books efficiently by adding, issuing, and returning books while also calculating fines for late returns.

---

## 🚀 Features

- ➕ Add new books  
- 📖 View available and issued books  
- 📤 Issue books to students  
- 📥 Return books with fine calculation  
- 💰 Automatic fine calculation for late returns  
- 📅 Tracks issue date and duration  
- 📜 Displays library fine policy  

---

## 🛠️ Technologies Used

- Python
- `datetime` module

---

## 📂 Project Structure

- Single Python file containing:
  - Book management logic
  - Menu-driven interface
  - Fine calculation system

---

## ▶️ How to Run

1. Make sure Python is installed on your system  
2. Copy the code into a `.py` file (e.g., `library.py`)  
3. Run the file:

```bash
python library.py
```

---

## 📋 Menu Options

```
1. Add Book
2. Show Books
3. Issue Book
4. Return Book
5. Fine Policy
6. Exit
```

---

## 💡 How It Works

- Books are stored in a **dictionary**
- Each book contains:
  - Availability status
  - Student name
  - Issue date
  - Number of allowed days
- Fine is calculated based on late days using an increasing rate

---

## 💰 Fine Policy

```
1st Week  → ₹10/day/book
2nd Week  → ₹20/day/book
3rd Week  → ₹60/day/book
... continues increasing
```

---

## 🧠 Example

- Issue a book for 5 days  
- Return after 8 days  
- Late by 3 days → Fine calculated automatically  

---

## 🔮 Future Improvements

- Save data to file (persistent storage)
- Add login system (Admin/User)
- GUI using Tkinter
- Search functionality
- Book categories

---

## 🙏 Acknowledgment

This project is created for learning purposes to understand:
- Python dictionaries
- Functions
- Date & time handling
- Menu-driven programs


---

⭐ If you like this project, consider improving it further!
