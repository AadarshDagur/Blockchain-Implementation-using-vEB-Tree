Blockchain Implementation Using Van Emde Boas (vEB) Tree
Project Overview: 
This project is a blockchain implementation that uses a Van Emde Boas (vEB) tree for efficient key management. 
The blockchain maintains blocks containing user details, each with a unique key stored in a vEB tree for quick lookups. 
The vEB tree helps verify the existence of keys in the blockchain, allowing users to search for their information or add new entries.

Authors:
<br>
Adarsh Chaudhary (2023CSB1321)
Rishabh Rawat (2023MCB1377)
Aditya Kumar (2023CSB1094)

Prerequisites
Compiler: Ensure you have a C compiler (e.g., GCC) installed.
uthash Library: This project uses the uthash.h library for hash table implementation. Include uthash.h in the same directory as the source code or ensure it is accessible from your compiler's include path.
CSV File: The program reads data from a CSV file named random_entries.csv. Ensure this file exists in the project directory. The CSV should follow this format:roll_no,name,dob,block_key

How to Compile and Run
Compilation: Use the following command to compile the code:
gcc CS201.c
Running the Program: After compilation, run the program with:
./a

Input and Usage Guide
The program offers an interactive menu for users, allowing for the following operations:

Menu Options
1. Check Your Data:
Input:
Roll Number: Enter your roll number as an integer.
Block Key: Enter your unique 8-digit block key.
Expected Output:
If your block key matches the encrypted stored key, your details (name and date of birth) will be decrypted and displayed. The hash and encrypted block key will also be shown.
If the block key is incorrect, only encrypted data will be shown.

2.Enter a New Block:
Input:
Name: Enter your name (up to 100 characters).
Date of Birth: Enter your date of birth in YYYY-MM-DD format.
Block Key: Enter an 8-digit key for your block.
Expected Output:
The program will automatically assign the first available roll number and save the block in the blockchain and random_entries.csv.
A confirmation message will display your roll number and a success notice.

3.Check If Blockchain Is Tampered:
Output:
The program verifies each block by comparing hash values, identifying if the blockchain has been altered. It will list whether each block is valid or tampered.

4.Exit:
Exits the program, releasing all allocated memory.
