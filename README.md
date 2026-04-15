# Linux-System-Security
A collection of the first 12 hands-on Linux security and system administration labs, covering user management, sudo privileges, password policies, PAM, file permissions, and SELinux configuration across AlmaLinux, CentOS, and Ubuntu.
# 🛡️ Linux Security Hands-On Labs (1–12)

## 📌 Overview

In this repository, I document my hands-on journey through the first 12 Linux security and system administration labs. Each lab pushed me to move beyond theory and actually *do the work*—configuring systems, breaking things, fixing them, and understanding how Linux behaves under different security scenarios.

I worked across environments like AlmaLinux, CentOS, and Ubuntu, focusing on real-world administrative tasks such as privilege control, password security, access management, and SELinux enforcement.

---

## 🧪 Lab 1 – Assigning Limited Sudo Privileges

I started by creating multiple users and assigning them different levels of sudo access. Instead of giving everyone full control, I learned how to fine-tune permissions using `visudo`.

By testing each account, I clearly saw the difference between full administrative rights and restricted command access. This lab made it obvious why least privilege is critical in real systems.

---

## 🧪 Lab 2 – Disabling the Sudo Timer

Here, I explored how sudo remembers authentication for a short period. I disabled that timer so that every command required re-authentication.

At first, it felt annoying—but that was the point. It showed me how small usability tweaks can significantly improve security, especially on shared systems.

---

## 🧪 Lab 3 – Encrypted Home Directories

In this lab, I created a user with an encrypted home directory. I then accessed and examined how the encryption behaves behind the scenes.

This gave me a deeper appreciation for protecting user data at rest. Even if someone gains disk access, the data remains unreadable.

---

## 🧪 Lab 4 – Password Complexity Policies

I configured strict password rules by editing system security files. Then I tested weak and strong passwords to see how the system reacts.

Watching the system reject bad passwords in real time made the concept of password policies much more concrete. It’s not just theory—it actively enforces discipline.

---

## 🧪 Lab 5 – Account and Password Expiry

Here, I controlled how long user accounts and passwords remain valid. I set expiration dates, forced password changes, and configured warning periods.

This lab showed me how administrators can enforce security over time—not just at account creation.

---

## 🧪 Lab 6 – Detecting Compromised Passwords

I used an API to check whether passwords had been exposed in known data breaches.

This was eye-opening. Even passwords that seem “strong” can already be compromised. It reinforced why uniqueness matters more than complexity alone.

---

## 🧪 Lab 7 – Configuring Account Lockouts (pam_tally2)

In this lab, I configured login attempt limits to lock accounts after repeated failures.

I simulated failed logins until the account locked, then reset it manually. This felt very real—like handling a support ticket in an actual IT environment.

---

## 🧪 Lab 8 – Distributed Identity Management

This lab introduced centralized identity tools like FreeIPA and Adsys.

Although more conceptual and setup-heavy, it showed me how organizations manage users across multiple systems instead of handling them one by one.

---

## 🧪 Lab 9 – Finding SUID and SGID Files

I searched the entire system for special permission files and saved the results.

Then I created my own test file with elevated permissions and compared outputs. This made it clear how these permissions can be useful—but also dangerous if misused.

---

## 🧪 Lab 10 – File Attributes and Protection

I experimented with file attributes like immutable (`i`) and append-only (`a`).

Trying (and failing) to modify protected files was actually satisfying—it proved that these controls are effective against accidental or malicious changes.

---

## 🧪 Lab 11 – Shared Group Directory

In this lab, I created a shared directory with proper permissions, group ownership, and ACLs.

I simulated multiple users interacting with the same files, testing what each user could and couldn’t do. This felt like managing a real team workspace.

---

## 🧪 Lab 12 – SELinux Type Enforcement

This was one of the most interesting labs. I installed a web server and then intentionally broke access using incorrect SELinux contexts.

When the page stopped working, I had to diagnose and fix it. That moment really drove home how powerful—and strict—SELinux can be.

---

## 🧠 What I Learned

Across these labs, I learned that:

* Security is not one big feature—it’s many small controls working together
* Misconfigurations are often the biggest risk
* Testing is just as important as configuring
* Linux provides powerful tools—but expects you to use them correctly

---

## ⚙️ Technologies Used

* AlmaLinux / CentOS / Ubuntu
* Linux CLI tools (`sudo`, `chmod`, `chattr`, `find`, etc.)
* PAM (Pluggable Authentication Modules)
* SELinux
* Basic networking and system utilities

---

## 🚀 Final Thoughts

This wasn’t just a set of labs—it was practical training. I didn’t just read about Linux security; I implemented it, tested it, and sometimes broke it.

And honestly, that’s where the real learning happened.

---
