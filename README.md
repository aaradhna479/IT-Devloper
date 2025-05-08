# IT-Devloper

TASK-1

Generate a random number: random.randint(lower_bound, upper_bound) generates the secret number.
Prompt for user's guess: input() is used to get the user's guess.
Repeat until correct: The while attempts_left > 0: loop continues until the user guesses correctly or runs out of tries.
Limit attempts: max_attempts controls the number of tries.
Multiple rounds: The outer while True: loop allows for multiple rounds until the user chooses to stop.
Display score: The score variable keeps track of the user's performance (higher score is better in this implementation), and it's displayed after each round and at the end of the game. The scoring is based on the number of attempts remaining when the user guesses correctly.
Input validation: The code includes a try-except block to handle non-integer input and checks if the guess is within the valid range.
Feedback: The program provides feedback ("Too high", "Too low") after each incorrect guess.
To run this game, simply save the code as a Python file (e.g., number_game.py) and execute it from your terminal using python number_game.py.



TASK-2  

Input: It prompts the user to enter marks for each subject (out of 100) until they type 'done'. It also includes input validation to ensure marks are within the valid range (0-100) and handles non-numeric input.
Calculate Total Marks: sum(subject_marks) calculates the sum of all entered marks.
Calculate Average Percentage: total_marks / num_subjects calculates the average percentage.
Grade Calculation: It uses if-elif-else statements to assign a grade based on the following criteria:
A+: >= 90%
A: >= 80%
B: >= 70%
C: >= 60%
D: >= 50%
F: < 50%
Display Results: It neatly displays the Total Marks, Average Percentage (formatted to two decimal places), and the calculated Grade.
To run this calculator, save the code as a Python file (e.g., grade_calculator.py) and execute it using python grade_calculator.py in your terminal. You'll then be prompted to enter the marks for each subject.



TASK-3

BankAccount Class:
__init__(self, account_number, pin, balance=0.0): Initializes a bank account with an account number, PIN, and initial balance (default is 0.0).
deposit(self, amount): Adds a positive amount to the balance and displays a confirmation. It includes validation for a positive deposit amount.
withdraw(self, amount): Subtracts a positive amount from the balance if sufficient funds are available and displays a confirmation. It includes validation for a positive withdrawal amount and checks for sufficient balance.
check_balance(self): Prints the current balance.
get_account_number(self): Returns the account number of the account.
verify_pin(self, entered_pin): Compares the entered_pin with the account's pin and returns True if they match, False otherwise.
ATM Class:

__init__(self): Initializes an ATM with an empty dictionary self.accounts to store BankAccount objects, using the account number as the key.
add_account(self, account): Adds a BankAccount object to the self.accounts dictionary. It prevents adding duplicate accounts.
authenticate_user(self): Prompts the user for their account number and PIN. It retrieves the corresponding BankAccount object and verifies the PIN with a maximum of 3 attempts. If authentication fails after 3 attempts, it locks the account (in this simplified version, it just prevents further interaction).
display_menu(self): Prints the ATM menu options to the user.
run(self): This is the main method that starts the ATM interface.
It welcomes the user and calls authenticate_user() to log in.
If authentication is successful, it enters a loop to display the menu and process user choices.
Based on the user's choice (1-4), it calls the appropriate methods of the user_account object (withdraw, deposit, check_balance).
It includes basic error handling for invalid input (e.g., non-numeric amounts).
Option 4 allows the user to exit the ATM.
If authentication fails, it displays an appropriate message.
Connecting the Classes: The ATM class's self.accounts dictionary holds instances of the BankAccount class. When the user interacts with the ATM (e.g., chooses to withdraw), the run() method calls the corresponding method (withdraw()) on the specific BankAccount object associated with the authenticated user.

User Interface: The display_menu() method provides a simple text-based user interface with numbered options. The input() function is used to get user input.

Input Validation: The code includes basic try-except blocks to handle ValueError if the user enters non-numeric input when prompted for amounts. The withdraw() method in BankAccount also checks for sufficient balance and positive withdrawal amounts.

Display Messages: The code provides feedback to the user for successful and unsuccessful transactions, incorrect PIN attempts, invalid input, and insufficient balance.

How to Run:
Save the code as a Python file (e.g., atm_interface.py).
Run it from your terminal using python atm_interface.py.
You will be prompted to enter an account number ("123456" or "789012") and the corresponding PIN ("1234" or "5678").
Follow the on-screen menu to perform transactions.
