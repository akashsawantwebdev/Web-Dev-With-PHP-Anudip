Anudip - Domain Training - Code explanation help



File : atm-machine.html 

✅ ATM Machine Project – Short Explanation

1. HTML Structure
A box is created using <div class="box"> to show ATM UI.
A dropdown (<select>) allows user to choose 4 operations:
Deposit
Withdraw
Change PIN
Check Balance


A dynamic area <div id="inputs"> displays different textboxes depending on the selected option.
A Proceed button runs the main function.
A <p id="msg"> displays messages (success or error).


✅ 2. CSS Styling
.box centers the ATM card shape and adds shadow, padding, border-radius.
All inputs, select, buttons have same width using width:100%.
Hover effect added on button for UI improvement.
background: #f4f4f4 for clean light theme.


✅ 3. JavaScript Logic (Main Part)
Variables
balance → stores user account balance
pin → default PIN ("1234")

A) renderFields() – Dynamic Input Loading
Triggered when user selects an option.
Uses switch case to insert required input boxes:
Deposit → amount + PIN
Withdraw → amount + PIN
Change PIN → old PIN, new PIN, confirm PIN
Check Balance → only PIN
This avoids unnecessary fields and keeps UI clean.


B) digitOnly() – PIN Validation Helper
Removes all non-numeric characters.
Ensures PIN textboxes accept digits only.



C) proceed() – Performs ATM Operations
Uses switch case for each option:
1. Deposit
Validates PIN.
Ensures minimum ₹100.
Adds amount to balance.
Clears both textboxes after operation.


2. Withdraw
Validates PIN.
Checks sufficient balance.
Ensures max withdrawal = ₹10,000.
Deducts amount from balance.
Clears both textboxes always.


3. Change PIN
Validates old PIN.
Checks new PIN matches confirm PIN.
Updates stored PIN.
Shows success message.


4. Check Balance
Validates PIN.
Shows current balance.
Clears PIN textbox every time.



✅ 4. Key Features
switch case used for both UI loading and logic processing.
Dynamic inputs based on operation.
PIN restricted to 4 digits only.
Validation added everywhere for secure flow.
Textboxes auto-clear after each operation.
Simple, clean, professional UI.

