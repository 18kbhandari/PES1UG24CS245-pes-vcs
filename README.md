# PES-VCS Lab Report

**Name:** Kushagra Bhandari
**SRN:** PES1UG24CS245
**Repository:** [PES1UG24CS245-pes-vcs](https://github.com/18kbhandari/PES1UG24CS245-pes-vcs)

---

# 📌 Phase 1: Object Storage Foundation

### Concepts

Content-addressable storage, hashing, atomic writes, directory sharding

### Implementation

* Implemented `object_write`
* Implemented `object_read`
* Used SHA-256 hashing
* Stored objects using sharded directory structure

### Testing

* Successfully ran:

```
make test_objects
./test_objects
```

### 📸 Screenshots

<p align="center">
  <img src="images/1.A.png" width="300"/>
  <img src="images/1.B.png" width="300"/>
</p>

---

# 📌 Phase 2: Tree Objects

### Concepts

Directory hierarchy, recursive structures, file modes

### Implementation

* Implemented `tree_from_index`
* Built tree hierarchy from index
* Supported nested paths

### Testing

```
make test_tree
./test_tree
```

### 📸 Screenshots

<p align="center">
  <img src="images/2.A.png" width="300"/>
  <img src="images/2.B.png" width="300"/>
</p>

---

# 📌 Phase 3: Index (Staging Area)

### Concepts

File tracking, metadata comparison, atomic writes

### Implementation

* Implemented `index_load`
* Implemented `index_save`
* Implemented `index_add`

### Output Example

```
./pes status
```

### 📸 Screenshots

<p align="center">
  <img src="images/3.A.png" width="300"/>
  <img src="images/3.B.png" width="300"/>
</p>

---

# 📌 Phase 4: Commits and History

### Concepts

Linked structures, commit history, HEAD reference

### Implementation

* Implemented `commit_create`
* Linked commits using parent reference
* Updated HEAD

### Testing

```
./pes log
make test-integration
```

### 📸 Screenshots

<p align="center">
  <img src="images/4.A.png" width="300"/>
  <img src="images/4.B.png" width="300"/>
  <img src="images/4.C.png" width="300"/>
</p>

---

# 📌 Final Integration

<p align="center">
  <img src="images/integration_test1.png" width="300"/>
  <img src="images/integration_test2.png" width="300"/>
</p>

---

# 📌 Phase 5 & 6: Analysis Questions

## 🔹 Q5.1 Checkout Implementation

To implement checkout, update `.pes/HEAD` to target branch, load commit tree, update working directory, and sync index. Complexity arises from handling untracked and modified files safely.

## 🔹 Q5.2 Dirty Working Directory Detection

Compare working directory files with index metadata and hashes. If modified and differs from target commit, abort checkout.

## 🔹 Q5.3 Detached HEAD

Commits are created but not referenced by any branch. They become dangling unless a branch is created pointing to them.

---

## 🔹 Q6.1 Garbage Collection

Use mark-and-sweep algorithm:

* Traverse reachable objects from HEAD and refs
* Store hashes in HashSet
* Delete unreachable objects

## 🔹 Q6.2 GC Race Condition

GC may delete newly created objects before commit links them. Git avoids this using a grace period before deletion.

---

# 📌 Conclusion

This project successfully demonstrates the core working principles of a Version Control System including object storage, indexing, commits, and history tracking.

---

# 👨‍💻 Author

Kushagra Bhandari
PES1UG24CS245

---
