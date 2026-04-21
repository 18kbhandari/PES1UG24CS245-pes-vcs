# PES-VCS Lab Report

**Name:** Kushagra Bhandari  
**SRN:** PES1UG24CS245  
**Repository:** [PES1UG24CS245-pes-vcs](https://github.com/18kbhandari/PES1UG24CS245-pes-vcs)

---

## Phase 1: Object Storage Foundation

### What I Implemented

- `object_write` — builds the full object (header + data), computes SHA-256, deduplicates, shards into `.pes/objects/XX/`, and writes atomically using temp-file + rename pattern.

- `object_read` — reads the object file, parses the header, recomputes the hash to verify integrity, and returns the data portion.

---

## Phase 2: Index and Tree Structure

### What I Implemented

- Index structure to track files and metadata.  
- Tree objects to represent directory hierarchy.  
- Functions to serialize and deserialize index entries.  

---

## Phase 3: Commit System

### What I Implemented

- Commit object creation with metadata (author, message, timestamp).  
- Linking commits with parent references.  
- Storing commit history.  

---

## Phase 4: Checkout and Restore

### What I Implemented

- Restore files from object database.  
- Checkout specific commits.  
- Reconstruct working directory from stored objects.  

---

## Challenges Faced

- Handling file integrity using hashing.  
- Managing object storage paths.  
- Ensuring atomic writes to avoid corruption.  

---

## Learning Outcomes

- Understood how Git internally stores objects.  
- Learned about hashing (SHA-256) and deduplication.  
- Implemented a simplified version control system.  

---
## 📸 Screenshots

<p align="center">
  <img src="images/1.A.png" width="300"/>
  <img src="images/1.B.png" width="300"/>
</p>

<p align="center">
  <img src="images/2.A.png" width="300"/>
  <img src="images/2.B.png" width="300"/>
</p>

<p align="center">
  <img src="images/3.A.png" width="300"/>
  <img src="images/3.B.png" width="300"/>
</p>

<p align="center">
  <img src="images/4.A.png" width="300"/>
  <img src="images/4.B.png" width="300"/>
  <img src="images/4.C.png" width="300"/>
</p>

## Conclusion

This project helped in understanding the core concepts behind version control systems like Git, including object storage, commits, and file tracking.
