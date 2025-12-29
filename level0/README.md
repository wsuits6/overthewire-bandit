# Bandit Level 0

## Objective

The goal of this level is to connect to the Bandit SSH server for the first time using the provided username and password.

---

## Server Information

* **Domain:** `bandit.labs.overthewire.org`
* **IP Address:** `51.21.210.216`
* **SSH Port:** `2220`

---

## Approach

To connect to the Bandit server, I first verified that the server was reachable by sending ICMP packets using the `ping` command. This confirmed that the host was online and accessible.

After confirming connectivity, I attempted to log in using SSH.
On my first attempt, the connection failed because the default SSH port (`22`) was used.

After reviewing the challenge instructions, I realized that OverTheWire uses a **custom SSH port (2220)**. Once I specified the correct port, the connection was successful.

---

## Commands Used

### Ping the server

```bash
ping bandit.labs.overthewire.org
```

### Connect via SSH (with custom port)

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

---

## Finding the Flag

After logging in successfully:

1. I listed the contents of the home directory:

   ```bash
   ls -la
   ```

2. I found a file named `readme`.

3. I displayed its contents using:

   ```bash
   cat readme
   ```

4. The file contained the password for the next level.

---

## Result

**Flag:**

```
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

---

## Credentials Used

* **Username:** `bandit0`
* **Password:** `bandit0`

---

## Key Takeaways

* Always check for custom SSH ports.
* Basic Linux commands (`ls`, `cat`) are essential.
* Reading instructions carefully prevents unnecessary mistakes.
