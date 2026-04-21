# PES-VCS Lab Report

**Name:** Kushagra Bhandari
**SRN:** PES1UG24CS245
**Repository:** [PES1UG24CS245-pes-vcs](https://github.com/18kbhandari/PES1UG24CS245-pes-vcs)

---

## 📌 Overview

This project implements a basic **Version Control System (VCS)** in C.
It demonstrates how files are tracked, stored, and managed similar to real-world systems like Git.

---

## 🎯 Features

* Object storage using hashing (SHA-256)
* File indexing system
* Commit tracking
* Version management
* File integrity verification

---

## 🛠️ Technologies Used

* C Programming
* File Handling
* Makefile

---

## 📂 Project Structure

```id="5f6r1g"
.
├── commit.c
├── commit.h
├── index.c
├── index.h
├── Makefile
├── README.md
└── images/
```

---

## ⚙️ How to Run

### 1️⃣ Clone the repository

```bash id="3ndp3a"
git clone https://github.com/18kbhandari/PES1UG24CS245-pes-vcs.git
cd PES1UG24CS245-pes-vcs
```

### 2️⃣ Compile the program

```bash id="6plw2z"
make
```

### 3️⃣ Run the program

```bash id="2k0m6d"
./a.out
```

---

## 🧪 Implementation Details

### 🔹 Phase 1: Object Storage

* `object_write` → Creates object, computes SHA-256 hash, stores data in `.pes/objects/`
* `object_read` → Reads stored objects, verifies integrity, retrieves data

---

### 🔹 Phase 2: Indexing System

* Tracks added files
* Maintains an index file
* Updates file status efficiently

---

### 🔹 Phase 3: Commit System

* Creates commits with metadata
* Maintains commit history
* Links commits with stored objects

---

## 📸 Screenshots

<p align="center">
  <img src="images/1A.jpeg" width="300"/>
  <img src="images/1B.jpeg" width="300"/>
</p>

<p align="center">
  <img src="images/2A.jpeg" width="300"/>
  <img src="images/2B.jpeg" width="300"/>
</p>

<p align="center">
  <img src="images/3A.jpeg" width="300"/>
  <img src="images/3B.jpeg" width="300"/>
</p>

<p align="center">
  <img src="images/4A.jpeg" width="300"/>
  <img src="images/4B.jpeg" width="300"/>
  <img src="images/4C.jpeg" width="300"/>
</p>

---

## 📖 Screenshot Description

* **1A–1B:** Object creation and storage
* **2A–2B:** File indexing and tracking
* **3A–3B:** Commit operations
* **4A–4C:** Final output and verification

---

## 🚀 Future Improvements

* Add branching functionality
* Improve user interface
* Add rollback support
* Optimize storage efficiency

---

## 👨‍💻 Author

**Kushagra Bhandari**
PES1UG24CS245

---
