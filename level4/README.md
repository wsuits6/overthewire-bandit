## Bandit Level 4 Walkthrough

### Overview

In **Bandit Level 4**, the password is hidden inside **one human‑readable file** located in the `inhere` directory. The challenge is identifying which file actually contains readable text.

---

### Step 1: Log in

Successfully logged into the Bandit Level 4 server.

---

### Step 2: List files in the home directory

To check what’s available, run:

```bash
ls -la
```

This reveals a directory called `inhere`, which contains the challenge files.

---

### Step 3: Enter the directory

Move into the directory using:

```bash
cd inhere
```

---

### Step 4: List all files inside `inhere`

To view every file (including hidden ones), run:

```bash
ls -la
```

This displays several files named:

```
-file00
-file01
-file02
...
-file09
```

All files appear similar, but only **one contains human‑readable text**.

---

### Step 5: Identify the human‑readable file

Because the filenames start with `-`, they must be handled carefully. The safest method is using the `file` command:

```bash
file ./*
```

Output:

```bash
./-file00: data
./-file01: OpenPGP Public Key
./-file02: OpenPGP Public Key
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```

This confirms that **`-file07`** contains readable ASCII text.

---

### Step 6: Read the correct file

Use the following command to view its contents:

```bash
cat ./-file07
```

Output:

```bash
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

---

### ✅ Result

**Password for the next level:**

```
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

---

### Key Notes

* Files starting with `-` must be accessed using `./` to avoid command confusion.
* The `file` command is essential for identifying readable content.
* Only one file contains the actual password.
* Always inspect files before opening them blindly.
