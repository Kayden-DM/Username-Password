Login System
A command-line Python program that lets users create accounts and log in, storing credentials in a text file.

Concepts Used
File Handling — open() with "r" and "a" modes reads and appends to accounts.txt.

Exception Handling — try/except FileNotFoundError handles a missing accounts file on first run.

String Methods — .strip() and .split(",") parse each saved username,password line.

Features
Account Creation — checks for duplicate usernames and enforces a 3-character minimum.

Login Verification — compares entered details against each line in the file.

Persistent Storage — accounts survive between program runs via the text file.

Improvements
Security — passwords are stored in plain text and username in file.read() can falsely match substrings; hash passwords and compare parsed fields exactly.

Use for/else Correctly — the else on the loop prints "Incorrect login" only if no break, but exit() is called instead; return a boolean and break properly.

Re-prompt on Failure — failed account creation returns to the menu; looping until valid input would be friendlier. Also, exit() on login closes the whole program rather than returning to a logged-in menu.
