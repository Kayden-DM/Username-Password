## Login System
A command-line account system written in Python. It stores usernames and passwords in a local text file and provides an interactive menu for creating accounts and logging in.

## Features
Create Account — Prompts for a username and password, then appends them to accounts.txt.

Duplicate Check — Rejects usernames that already exist in the file.

Length Validation — Requires both usernames and passwords to be at least 3 characters long.

Login — Reads accounts.txt line by line and checks the entered username and password against saved entries.

Missing File Handling — Uses try/except FileNotFoundError so account creation works even if the file doesn't exist yet.

Menu Loop — Runs until the user selects option 3 to exit.

## Technologies Used
text
| Technology | Purpose |
|---|---|
| Python | Application logic |
| File handling (`open`) | Reads and writes `accounts.txt` |
| `with` statement | Ensures files are closed automatically |
| `split(",")` | Separates usernames and passwords |
| `input()` / `print()` | Console interaction |
| `try / except` | Handles a missing accounts file |
| `while True` loop | Keeps the menu running until exit |
<!-- -->
## How to Use It
Install Python 3.6 or newer from python.org and make sure it's added to your PATH.

Save the code as login.py.

Open a terminal in the folder containing the file.

Run python login.py.

Use the menu: 1 to create an account, 2 to log in, 3 to exit. Accounts are saved in accounts.txt in the same folder.

## Improvements
Store hashed passwords — passwords are saved in plain text, which is insecure; use the hashlib module to store a hash (e.g. hashlib.sha256(password.encode()).hexdigest()) instead.

Fix the duplicate check — if username in file.read() does a substring match, so bob would be rejected if bobby already exists; split each line and compare usernames exactly instead.
