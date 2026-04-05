## **CISSP Security Domains (5-8)**

## **Domain 5: Identity and Access Management (IAM)**

**Focus:** Ensuring the right people have the right access to the right data.

- **Main Goal:** Reduce risk by limiting user access to only what is necessary for their job.
- **The Four Components of IAM:**
    1. **Identification:** A user claiming an identity (e.g., typing a username or swiping a badge).
    2. **Authentication:** Proving that identity (e.g., passwords, PINs, or fingerprints).
    3. **Authorization:** Setting the permission level (e.g., an intern has "read-only" access while a manager has "edit" access).
    4. **Accountability:** Tracking and logging actions (e.g., recording who logged in at 2:00 AM).
    - *Example:* If a company uses one shared "admin" password, they lose **accountability** because they can't tell which specific person accessed a file during a breach.

---

## **Domain 6: Security Assessment and Testing**

**Focus:** Checking if your security actually works through audits and data analysis.

- **Security Control Testing:** Evaluating if current tools (like firewalls) are meeting the organization's goals.
- **Analyzing Data:** Regularly reviewing security reports to spot vulnerabilities before they are exploited.
- **Audits:** Formal reviews to monitor for new risks or threats.
    - *Example:* After a test shows that passwords are being guessed easily, a security team might implement **Multi-Factor Authentication (MFA)** as a new control.

---

## **Domain 7: Security Operations**

**Focus:** Reacting to incidents and investigating what went wrong.

- **Incident Response:** Acting with urgency to stop an active attack and prevent it from getting worse.
- **Forensic Investigation:** Once the threat is gone, collecting digital evidence to find out the "how, when, and why" of the breach.
- **Preventative Measures:** Using the investigation results to update defenses against future attacks.
    - *Example:* After a virus hits a network, an analyst performs a **digital forensic investigation** to trace the virus back to a specific infected USB drive.

---

## **Domain 8: Software Development Security**

**Focus:** Building security into software from the very beginning.

- **Secure Coding Practices:** Following guidelines to ensure applications aren't born with "holes" or bugs.
- **Software Development Lifecycle (SDLC):** Integrating security checks into every phase of building software, not just at the end.
    - **Design Phase:** Perform a secure design review.
    - **Development Phase:** Conduct code reviews to find errors.
    - **Deployment Phase:** Use **Penetration Testing** (authorized "hacking" of your own app) to find weaknesses.
    - *Example:* Checking a new mobile banking app for security flaws *while* it's being coded, rather than waiting until it's already in the App Store.
