password = input("Enter the Password")

length = len(password) >= 8
lower = any(ch.islower() for ch in password)
upper = any(ch.isupper() for ch in password)
digit = any(ch.isdigit() for ch in password)
special = any(ch in "!@#$%^&*()_+-=" for ch in password)

strength = length + lower + upper + digit + special

if strength <= 2:
    code = "Weak Password"
elif strength == 3 or strength == 4:
    code = "Moderate Password"
elif strength == 5:
    code = "Strong Password"
else:
    code = "Invalid Input"

print("Password comes under the category of", code)
# Password Strength Checker

This is a simple Python CLI (Command Line Interface) project that checks the strength of a password based on the following rules:

- Password should be at least 8 characters long
- Should contain at least one lowercase letter
- Should contain at least one uppercase letter
- Should include at least one digit
- Should have at least one special character (e.g., @, #, $, etc.)

## How it works

The script checks all 5 conditions and gives output like:

- **Weak Password** (if 2 or fewer rules are matched)
- **Moderate Password** (if 3 or 4 rules are matched)
- **Strong Password** (if all 5 rules are matched)

## Usage

```bash
$ python3 password_checker.py
Enter the Password: Piyush@123
Password comes under the category of Strong Password
```

## Author

Piyush Hemant Gangurde
