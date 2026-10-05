🔐 Python Account Login System
A simple command-line account creation and login system built with Python. This program lets users create an account with a username and password, then log in using those saved credentials. It's a great beginner project for learning about file handling, functions, input validation, and loops in Python.

📖 Python Account Login System
The Python Account Login System is a console-based application that simulates a basic account system. When the program starts, a menu appears with options to create an account, log in, or exit.

When creating an account, the program checks that the username isn't already taken by reading from a file called accounts.txt, and it ensures both the username and password are at least 3 characters long. Valid accounts are saved to the file in the format username,password.

When logging in, the program reads through accounts.txt line by line, splitting each entry into a username and password, and checks whether the entered credentials match any saved account.

This project is ideal for anyone learning the fundamentals of Python file I/O and authentication flow.

✨ Features
Account creation – Users can register with a unique username and password.

Duplicate username check – Prevents creating an account with a username that already exists.

Minimum length validation – Usernames and passwords must be at least 3 characters long.

Persistent storage – Accounts are saved to accounts.txt, so they remain after the program closes.

Login system – Verifies entered credentials against saved accounts.

Menu-driven interface – Simple numbered menu for navigating the program.

Looping menu – Keeps running until the user chooses to exit.

Exit option – Quit the program cleanly at any time.

Safe file handling – Uses try/except to handle the case where accounts.txt doesn't exist yet.

🛠️ What It Uses
Language & Library
Python 3 – No external libraries required (pure standard library).

File Used
File	Purpose
accounts.txt	Stores accounts in the format username,password — one per line. Created automatically when the first account is registered.
Key Functions
Function	Purpose
create_account()	Prompts for a username and password, validates them, and saves the new account to accounts.txt.
login()	Prompts for a username and password and checks them against saved accounts in accounts.txt.
Python Concepts Demonstrated
File handling – Opening files in read ("r") and append ("a") modes.

with open(...) – Ensures files are properly closed after use.

Exception handling – try/except FileNotFoundError for the missing accounts file.

String methods – .strip(), .split(","), and .read() for parsing file contents.

Functions – Organizing logic into reusable blocks.

Conditional logic – Validating length and checking for duplicate usernames.

Loops – while True for the main menu and for loops for reading file lines.

for...else – The else block runs only if the loop completes without break.

F-strings – Formatting the saved account line.

exit() – Ends the program after a successful login.

Built-in Functions Used
input() – Reads user input from the console.

print() – Displays menus and messages.

open() – Opens accounts.txt for reading or appending.

len() – Checks username and password lengths.

exit() – Terminates the program after login.

break – Exits the main menu loop.

📥 Download
You can download the source file from this repository and save it as a .py file:

text
login_system.py
No installation or dependencies are needed — just Python.

▶️ How to Run
Make sure you have Python 3 installed (python.org).

Save the code as login_system.py.

Open a terminal or command prompt in the folder containing the file.

Run:

bash
python login_system.py
Use the menu to create an account or log in.

🐍 Made with Python
This project is written entirely in Python 3 using only the standard library. It's a clean and practical example of how file handling and conditional logic can be combined to build a simple authentication system.

Whether you're a beginner practicing file I/O or someone who wants a simple login simulation, this project is a great starting point.

💡 Possible Future Improvements
Hash passwords using hashlib instead of storing them in plain text.

Limit login attempts – Lock out after a few failed tries.

Add a "change password" option for existing accounts.

Save usernames and passwords as separate fields or use JSON for cleaner storage.

Add an admin account with special privileges.

Strip whitespace from username input to prevent duplicates like "alex" and "alex ".

Fix the duplicate username check – Currently it uses if username in file.read(), which matches substrings (e.g., "al" would match "alex"). Splitting by line and comparing exact usernames would be safer.

Build a Tkinter GUI version for a graphical interface.

📄 License
This project is free to use, modify, and distribute for personal or educational purposes.
