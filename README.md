# 🔗 Blockchain Implementation Using Van Emde Boas (vEB) Tree

## 📘 Overview

This project implements a **blockchain system** integrated with a **Van Emde Boas (vEB) Tree** for efficient key management. Each block stores user-specific details and is uniquely identified using a key stored in the vEB tree. The vEB tree enables **fast key lookups**, allowing users to:

- Search and verify their information
- Add new entries to the blockchain
- Detect any tampering of existing data

---

## 👨‍💻 Authors

- **Adarsh Chaudhary** – `2023CSB1321`  
- **Rishabh Rawat** – `2023MCB1377`  
- **Aditya Kumar** – `2023CSB1096`

---

## ⚙️ Prerequisites

Before running the project, ensure the following are set up:

- **C Compiler:** Install GCC or any standard C compiler.
- **Uthash Library:** Required for hash table implementation.
  - Include `uthash.h` in the same directory as the code, or ensure it’s accessible from the compiler’s include path.
- **CSV Data File:** A file named `random_entries.csv` should exist in the project root.  
  Format:  
  ```csv
  roll_no,name,dob,block_key
  ```

---

## 🛠️ How to Compile and Run

### 🔧 Compilation

```bash
gcc CS201.c
```

### ▶️ Run the Program

```bash
./a
```

---

## 🧾 Usage Guide

The program runs through an **interactive menu**, offering the following options:

### 1️⃣ Check Your Data

**Input:**  
- `Roll Number`: Your assigned roll number  
- `Block Key`: Your unique 8-digit block key  

**Output:**  
- If the key is valid:
  - Decrypted **Name** and **Date of Birth**
  - Corresponding **Hash** and **Encrypted Block Key**
- If the key is invalid:
  - Only encrypted data will be shown

---

### 2️⃣ Enter a New Block

**Input:**  
- `Name`: Up to 100 characters  
- `Date of Birth`: Format `YYYY-MM-DD`  
- `Block Key`: A unique 8-digit number  

**Output:**  
- The system assigns the **next available roll number**
- Stores the data into the blockchain and updates `random_entries.csv`
- Displays a confirmation with your assigned roll number

---

### 3️⃣ Check If Blockchain Is Tampered

**Output:**  
- Verifies the integrity of each block by checking **hash consistency**
- Identifies whether any block has been **tampered or remains valid**

---

### 4️⃣ Exit

- Exits the program gracefully
- Frees all allocated memory

---

## 🧠 Key Concepts

- **Van Emde Boas Tree:** Allows O(log log U) operations for fast key search, insert, and delete.
- **Hashing with uthash:** Ensures efficient mapping and validation.
- **Blockchain Integrity:** Each block contains a hash that validates the data's authenticity and order.

---

## 📂 Project Structure

```
├── CS201.c                 # Main C source code
├── uthash.h                # Hash table implementation (external header)
├── random_entries.csv      # User data in CSV format
└── README.md               # Project documentation
```

---

## ✅ Sample CSV Format

```csv
roll_no,name,dob,block_key
1001,John Doe,2001-12-25,12345678
1002,Jane Smith,2002-05-14,87654321
```

---
