# Bandit Level 2

## Objective

The goal of this level is to retrieve the password for **Level 3**. The password is stored in a file with spaces in its name, located in the home directory of the Level 2 user.

---

## Plan

Since the password is stored in a file with spaces in its name, the task is to:

1. Log in using the credentials from Level 1.
2. List the files in the home directory.
3. Identify and read the file containing the password using proper handling for spaces and special characters.

---

## Approach

After logging in successfully using the credentials obtained from Level 1, I listed the files in the home directory.

One of the files had spaces in its name: `spaces in this file name ahaha`. Because filenames with spaces cannot be read directly with standard commands, I needed to enclose the filename in double quotes.

Additionally, using `./` before the filename ensures the command interprets it as a file path rather than an option.

---

## Commands Used

### List files

```bash
ls
```

### Read the file with spaces in its name

```bash
cat "spaces in this file name ahaha"
```

---

## Result

The file contained the password for the next level.

**Flag:**

```
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

---

## Key Takeaways

* Filenames with spaces must be enclosed in quotes.
* Using `./` clarifies that the target is a file, not a command option.
* Paying attention to filenames prevents errors and simplifies file access.
