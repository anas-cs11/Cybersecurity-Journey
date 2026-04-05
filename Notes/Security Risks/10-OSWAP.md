**OWASP** stands for the **Open Worldwide Application Security Project** (formerly the Open Web Application Security Project).

It is a global, nonprofit organization dedicated to one mission: **improving the security of software.**

**OWASP Security Principles**

**1. Minimize the Attack Surface Area**

• **Attack Surface:** The total sum of all possible entry points (vulnerabilities) a haker could use.

• **Attack Vectors:** The specific "pathways" used to get in (e.g., phishing emails, open ports, weak passwords).

• **The Goal:** Make the target as small as possible.
    ◦ *Action:* Disable unnecessary software features, restrict access, and use complex passwords.

**2. Principle of Least Privilege (PoLP)**

**Definition:** Giving users only the **minimum** level of access they need to do their job—nothing more.

**Purpose:** To limit the "blast radius" or damage if an account is hacked.
    ◦ *Example:* An entry-level analyst can **read** security logs but is not allowed to **change** user permissions. If their account is stolen, the hacker still can't change permissions.

**3. Defense in Depth**

• **Definition:** Using **multiple layers** of security controls so that if one fails, others are still there to stop the attacker.

**Layer Examples:**


  **Layer 1:** Multi-Factor Authentication (MFA).
  
  **Layer 2:** Firewalls.
  
  **Layer 3:** Intrusion Detection Systems (IDS).
  
  **Layer 4:** Strict permission settings.

**4. Separation of Duties**

• **Definition:** Splitting a sensitive task between two or more people so no single person has too much power.

• **Purpose:** To prevent fraud or illegal activity.
    ◦ *Example:* In a company, the person who **prepares** the paychecks should not be the same person who **signs** them.

**5. Keep Security Simple**

• **Definition:** Avoid overly complex security designs.

• **Why?** If a system is too complicated, it becomes "unmanageable," people make mistakes, and it’s harder for teams to work together.
    ◦ *Simple Rule:* If it's too hard to use, people will find ways to bypass it.

**6. Fix Security Issues Correctly**

• **Definition:** Don't just apply a "Band-Aid"; find the **root cause** of the problem.

• **Process:** Identify the core weakness $\rightarrow$ Fix it $\rightarrow$ **Test it** to make sure the fix actually worked.
    ◦ *Example:* Instead of just resetting a breached password, implement a stricter password policy across the whole company.
