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

## Conclusion

This project helped in understanding the core concepts behind version control systems like Git, including object storage, commits, and file tracking.
