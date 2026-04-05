## Understanding Brute Force Attacks and Prevention

A **brute force attack** is a trial-and-error method used by attackers to discover private information, such as usernames and passwords. Since many people use simple or common passwords, these credentials are a weak point in a network's defense.

---

## 1. Types of Brute Force Attacks

While some attacks are done manually, most are performed using automated software tools to speed up the process.

- **Simple Brute Force Attack:** The attacker tries to guess a login by entering different combinations of characters, usernames, and passwords until one works.
- **Dictionary Attack:** The attacker uses a pre-made list of common words, phrases, or stolen passwords from previous data breaches. It is called a "dictionary" attack because it originally relied on words found in a literal dictionary.

---

## 2. Assessing Vulnerabilities Safely

Security analysts use isolated environments to test for weaknesses or study malware without risking the actual company network.

- **Virtual Machines (VMs):** A **VM** is a software version of a physical computer. It is an "isolated environment," meaning if malware ruins the VM, you can simply delete it and replace it with a clean "image" without hurting your real computer.
- **Sandbox Environments:** A **Sandbox** is a testing area separate from your main network. It is used to test **Patches**, find bugs, or run suspicious files to see how they behave.
    - *Note:* Some advanced malware can "detect" if it is in a sandbox and will act like harmless software to trick the analyst.

---

## 3. How to Prevent Brute Force Attacks

Organizations use a combination of "locking" the account and making the data unreadable to stop these attacks.

### A. Protecting Stored Passwords

- **Hashing:** This turns a password into a unique string of characters. It is a **one-way function**, meaning it cannot be turned back into the original text.
- **Salting:** This adds random characters to a password *before* it is hashed. This makes the hash much longer and more complex, making it much harder for attackers to crack.

### B. Verification Measures

- **MFA and 2FA:** **Multi-Factor Authentication** requires two or more ways to prove who you are (like a password + a fingerprint). **2FA** is the same but uses exactly two forms.
- **CAPTCHA / reCAPTCHA:** These are tests designed to tell humans and computers apart (like clicking on all the photos of buses). Since brute force software cannot easily solve these, it stops automated "bots" from guessing passwords.

### C. Password Policies

Organizations set rules to keep passwords strong, such as:

- Minimum length and complexity.
- Required password updates every few months.
- **Account Suspension:** Locking an account after too many failed login attempts.

---

## 4. Real-World Context: The Hashed Database

**Case Study: The Stolen File**
Imagine a company in **Chennai** has its database stolen by a hacker.

1. **Without Salting/Hashing:** The hacker opens the file and sees every employee's password in plain text. They can now log in as anyone.
2. **With Salting/Hashing:** The hacker only sees long strings of gibberish. Because the company used **Salting**, even employees with the same simple password (like "Password123") have completely different-looking hashes.
3. **The Result:** The hacker cannot easily use the stolen information, giving the company time to reset everyone's credentials.
