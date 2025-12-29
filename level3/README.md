## Bandit Level 3 Walkthrough

### Overview

For Bandit Level 3, the password is stored in a **hidden file** inside a directory named `inhere`. The task is to locate that directory, reveal the hidden file, and read its contents.

---

### Step 1: List all files

After connecting to the server, I listed all files (including hidden ones):

```bash
ls -la
```

This revealed a directory called `inhere`, which looked suspicious.

---

### Step 2: Enter the directory

I moved into the directory using:

```bash
cd ./inhere
```

---

### Step 3: Reveal hidden files

Inside the directory, I listed all files again:

```bash
ls -la
```

This revealed a hidden file (its name starts with a dot).

---

### Step 4: Read the file contents

To read the file safely, I used quotes around the filename:

```bash
cat ".<hidden_file_name>"
```

---

### Result

The file contained the password for the next level:

```
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

---

### Key Notes

* `ls -la` is required to see hidden files.
* Hidden files start with a dot (`.`).
* Quoting filenames prevents command errors.
* Always inspect directories before assuming nothing is there.
