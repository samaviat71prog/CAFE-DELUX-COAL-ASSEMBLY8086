# Cafe Deluxe - 8086 Assembly Billing System
A fully functional cafe billing system built in x86 Assembly 
language (8086) using EMU8086.
## Features
- Dine In and Take Away ordering with separate GST rates
- 8 menu items across Burgers, Pizza, Pasta and Coffee
- Automatic GST calculation (8% Dine In / 5% Take Away)
- Bill generation with Order Number and Customer Name
- Real-time file writing to orders list of cafe.txt after each bill
- End of Day summary with total sales and most sold item detection
- Welcome screen and input validation
## How It Works
1. Program starts and creates the orders file
2. Cashier enters customer name and order type
3. Customer selects items and quantities from menu
4. Option 5 generates the bill on screen and writes to file
5. Repeat for next customer or select End Day to exit
## File Handling
- FW procedure writes strings to file using INT 21H AH=40H
- FW_NUM procedure converts numbers to ASCII and writes digit by digit
- WRITE_TO_FILE called after every customer bill
- WRITE_SUMMARY writes end of day report on exit
## GST Calculation
- Dine In: Subtotal x 8 / 100
- Take Away: Subtotal x 5 / 100
- Uses MUL and DIV instructions in 8086
## Most Sold Item
- Linear comparison chain across daySold1 to daySold8
- AX tracks current maximum, BX tracks winning item index
- JBE instruction used to skip if item did not beat current max
## Requirements
- EMU8086 Emulator
- Windows OS
## How to Run
1. Open EMU8086
2. Load coal cafe delux project.asm
3. Click Compile then Run
4. orders list of cafe.txt will be created in the same directory


## Course
Computer Organization and Assembly Language
