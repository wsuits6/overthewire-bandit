## Bandit Level 4 Walkthrough

### Overview

According to the Bandit Level 4 documentation, the password is stored in **one human-readable file** inside the `inhere` directory. The challenge is identifying which file contains readable text.

---

### Step 1: Log in

Successfully logged into the Bandit Level 4 server.

---

### Step 2: List files in the home directory

To see all available files and directories, I ran:

```bash
ls -la
```

Output showed a directory named `inhere`, which is where the files of interest are located.

---

### Step 3: Enter the directory

I moved into the directory using:

```bash
cd inhere
```

---

### Step 4: List all files inside `inhere`

To view all files (including hidden ones), I ran:

```bash
ls -la
```

This displayed multiple files named like:

```
-file00
-file01
-file02
...
-file09
```

All files appeared similar, but only **one** of them contains human-readable text.

---

### Step 5: Identify the human-readable file

Since the filenames start with `-`, they must be accessed carefully. The correct approach is to use the `file` command:

```bash
file ./*
```

This command checks the file type and reveals which one contains readable text.

---

### Step 6: Read the correct file

Once the readable file is identified, its contents can be viewed using:

```bash
cat ./<filename>
```

---

### Result

The readable file contains the password for the next level.

---

### Key Notes

* Files starting with `-` must be accessed using `./` to avoid command confusion.
* The `file` command is essential for identifying readable content.
* Only one file contains the actual password.
* Always inspect before opening blindly.
