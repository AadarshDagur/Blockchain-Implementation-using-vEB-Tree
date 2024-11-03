Blockchain Implementation Using Van Emde Boas (vEB) Tree
<br>
Project Overview:
<br>
This project is a blockchain implementation that uses a Van Emde Boas (vEB) tree for efficient key management. 
The blockchain maintains blocks containing user details, each with a unique key stored in a vEB tree for quick lookups. 
The vEB tree helps verify the existence of keys in the blockchain, allowing users to search for their information or add new entries.

Authors:
<br>
Adarsh Chaudhary (2023CSB1321)
<br>
Rishabh Rawat (2023MCB1377)
<br>
Aditya Kumar (2023CSB1094)

Prerequisites
<br>
Compiler: Ensure you have a C compiler (e.g., GCC) installed.
<br>
Uthash Library: This project uses the uthash.h library for hash table implementation. Include uthash.h in the same directory as the source code or ensure it is accessible from your compiler's include path.
<br>
CSV File: The program reads data from a CSV file named random_entries.csv. Ensure this file exists in the project directory. The CSV should follow this format:roll_no,name,dob,block_key

How to Compile and Run
<br>
Compilation: Use the following command to compile the code:
gcc CS201.c
<br>
Running the Program: After compilation, run the program with:
./a

Input and Usage Guide
<br>
The program offers an interactive menu for users, allowing for the following operations:

Menu Options
1.Check Your Data:
<br>
Input:
<br>
Roll Number: Enter your roll number as an integer.
<br>
Block Key: Enter your unique 8-digit block key.
<br>
Expected Output:
<br>
If your block key matches the encrypted stored key, your details (name and date of birth) will be decrypted and displayed. The hash and encrypted block key will also be shown.
If the block key is incorrect, only encrypted data will be shown.

2.Enter a New Block:
<br>
Input:
<br>
Name: Enter your name (up to 100 characters).
<br>
Date of Birth: Enter your date of birth in YYYY-MM-DD format.
<br>
Block Key: Enter an 8-digit key for your block.
<br>
Expected Output:
<br>
The program will automatically assign the first available roll number and save the block in the blockchain and random_entries.csv.
A confirmation message will display your roll number and a success notice.

3.Check If Blockchain Is Tampered:
<br>
Output:
<br>
The program verifies each block by comparing hash values, identifying if the blockchain has been altered. It will list whether each block is valid or tampered.

4.Exit:
<br>
Exits the program, releasing all allocated memory.
