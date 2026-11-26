# ATM Management System

**PS No.: 2**  
**Language:** Python 3  
**Project type:** Menu-driven console application

## Default login
- PIN: `1234`
- Opening balance: `10000`

## Features
1. PIN verification with a maximum of 3 attempts
2. Check balance
3. Deposit money
4. Withdraw money (prevents withdrawal beyond available balance)
5. Mini statement (last 5 transactions)
6. Saves balance and transaction history in `atm.txt`

## Folder structure
```text
ATM-Management-System/
├── Folder 1 - Source Code/
│   ├── atm_management.py
│   └── atm.txt
└── Folder 2 - Documentation/
    ├── ATM_Management_System_Project_Report.pdf
    └── ATM_Management_System_Presentation_White_Theme.pptx
```

## Run in VS Code
1. Install Python 3 on your computer.
2. Open VS Code.
3. Select **File → Open Folder** and open `Folder 1 - Source Code`.
4. Open `atm_management.py`.
5. Open the VS Code terminal (**Terminal → New Terminal**).
6. Run:

```bash
python atm_management.py
```

If `python` does not work on Windows, try:

```bash
py atm_management.py
```

No external Python packages are required.

## Demonstration sequence
1. Enter PIN `1234`.
2. Select `1` to display the opening balance.
3. Select `2`, enter `5000` to deposit; balance becomes `15000`.
4. Select `3`, enter `2000` to withdraw; balance becomes `13000`.
5. Select `4` to display the mini statement.
6. Select `5` to exit.
7. Run the program again and check that the saved balance remains `13000`.

## Test cases from the assignment
- **Test Case 1:** PIN `1234` → option `2` → amount `5000` → expected balance `15000`.
- **Test Case 2:** Reset the data file to the default values → PIN `1234` → option `3` → amount `10000` → expected balance `0`.
- **Test Case 3:** Reset the data file → enter PINs `1111`, `2222`, `3333` → account locked after 3 failed attempts.
- **Test Case 4:** Reset the data file → PIN `1234` → option `3` → amount `abc` → invalid amount message. Then enter `2000` for a valid withdrawal → balance `8000`; option `4` shows the transaction.

## Reset to assignment defaults before a test
Open `atm.txt` and replace its complete contents with:

```text
# ATM Management System data file
PIN=1234
BALANCE=10000.00
```

Save the file before starting the next test case. This matches the instruction that each test case starts with the default data.

## Important
This is an educational simulation. The PIN is stored as plain text to match the simple file-handling assignment; do not use real banking credentials or real financial information.
