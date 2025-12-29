# Bandit Level 1

## Objective

The goal of this level is to retrieve the password for **Level 2**. The password is stored in the home directory of the Level 1 user.

---

## Plan

Since the password is stored in the home directory, the task is to:

1. Log in using the credentials from Level 0.
2. Inspect the files in the home directory.
3. Identify and read the file containing the password.

---

## Approach

After logging in successfully using the credentials obtained from Level 0, I listed the files in the home directory.

At first glance, the only visible item was a file named `-`. This looked unusual, so I verified whether it was an actual file using a detailed listing.

Because filenames starting with special characters can cause issues with standard commands, I needed to explicitly specify the file path when reading it.

---

## Commands Used

### List files

```bash
ls
```

### Verify file details

```bash
ls -la
```

### Read the file named `-`

```bash
cat ./-
```

---

## Result

The file contained the password for the next level.

**Flag:**

```
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

---

## Key Takeaways

* Filenames starting with special characters require explicit paths.
* `./` helps distinguish filenames from command options.
* Paying attention to small details prevents unnecessary confusion.
