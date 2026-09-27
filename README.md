# Password-Cracking-with-John-the-Ripper-and-NetworkWalks-tools-
This project demonstrates how John the Ripper (JTR) can be used in an authorized cybersecurity lab to test the strength of a password-protected PDF also using browser based security tools provided by NetworkWalks.

# Overview
This project demonstrates two approaches to password auditing and recovery against an authorized password-protected PDF.

The objective is to understand how password-protected files can be analyzed, how password-auditing hashes are extracted, and how password-recovery tools attempt to identify the original password.

The two approaches used in this project are:

1.John the Ripper (JTR) with the Johnny GUI

2.NetworkWalks Hash Calculator and Password Cracker


#  Cybersecurity & Ethical Hacking — Week 3 Project
Modules Covered

Module 1 : Password Cracking with John the Ripper (JTR)

Module 2 : Password Cracking with NetworkWalks Tools

This project demonstrates two approaches to password auditing and recovery against an authorized password-protected PDF.

The goal is to understand how password-protected files can be analyzed, how password-auditing hashes are extracted, and how password-recovery tools attempt to identify passwords.


## Learning Objectives

By completing this project, I learned how to:

Understand the fundamentals of password cracking.

Understand the role of hashes in password auditing.

Extract password-auditing information from a protected PDF.

Use John the Ripper and Johnny for password recovery.

Use browser-based password-auditing tools.

Verify a recovered password against a protected PDF.

Understand the importance of strong passwords.

## Tools Used

John the Ripper	Password auditing and recovery
Johnny	GUI for John the Ripper
NetworkWalks Hash Calculator	PDF hash extraction
NetworkWalks Password Cracker	Password recovery
Windows / Kali Linux	Lab environment
Web Browser	Access online tools
Notepad	Create hash input file

Lab Target:

My Locked PDF1.pdf

# Module 1 — John the Ripper (JTR)

John the Ripper (JTR) is a password-security auditing and password-recovery tool. Johnny provides a graphical interface for interacting with JTR.

### Step 1 — Installing JTR

Downloading John the Ripper from the official Openwall website:

https://www.openwall.com/john/

After extracting the Windows package, locate:

john/<br>
└── run/<br>
    └── john.exe<br>

### Step 2 — Configure Johnny

Open Johnny and configure the location of:

"john.exe"

<img width="1919" height="1016" alt="Screenshot 2026-09-26 180444" src="https://github.com/user-attachments/assets/45d9382c-94e8-42d5-915e-6877c754fb7a" />

### Step 3 — Extract the PDF Hash

Use an authorized PDF hash-extraction tool to obtain a JTR-compatible hash.

<img width="1919" height="1016" alt="image" src="https://github.com/user-attachments/assets/9d530aab-55c2-4cf3-8607-edb5301ad0f3" />

The resulting hash may begin with:

$pdf$...

### Step 4 — Save the Hash

Save the complete hash in:

hash1.txt

## Step 5 — Load Hash in Johnny

Open Johnny → Open password file → select:

hash1.txt

## Step 6 — Start Password Recovery

Select:

Start new attack


JTR will attempt to recover the password.

The recovery time depends on password length, complexity, attack method, and available computing resources.

<img width="1919" height="1016" alt="Screenshot 2026-09-26 185600" src="https://github.com/user-attachments/assets/680d4b61-e0cc-42e1-9541-3840fcfddeb8" />

## Step 7 — Verify

Use the recovered password to open:

My Locked PDF2.pdf

<img width="1919" height="1016" alt="Screenshot 2026-09-27 145202" src="https://github.com/user-attachments/assets/00075648-a8f7-4d4c-aa04-7a7b4e02de3a" />


# Module 2 — NetworkWalks Tools

This module uses browser-based NetworkWalks tools to perform the same general password-auditing workflow without installing JTR.

## Step 1 — Obtain the Lab PDF

NetworkWalks project page:

https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/

Target:

My Locked PDF1.pdf

## Step 2 — Extract the Hash

Open the NetworkWalks Hash Calculator:

https://networkwalks.com/hash-calculator/

Upload the authorized PDF and obtain the generated hash.

<img width="1916" height="964" alt="Screenshot 2026-09-27 150239" src="https://github.com/user-attachments/assets/f09c52ae-ea69-4f99-883f-b9fd97922cf5" />

## Step 3 — Copy the Hash

Copy the complete hash without modifying it.

## Step 4 — Password Recovery

Open the NetworkWalks Password Cracker:

https://networkwalks.com/password-cracker/

Paste the hash and start the password-recovery process.

<img width="1903" height="961" alt="Screenshot 2026-09-27 150619" src="https://github.com/user-attachments/assets/ee156d7e-9b24-4376-a301-34edfd7ed8f7" />

## Step 5 — Verify

If a password is recovered, use it to open:

My Locked PDF1.pdf

<img width="1910" height="923" alt="Screenshot 2026-09-27 150900" src="https://github.com/user-attachments/assets/0c58858c-1747-4b93-95a2-a2f75a9fc56a" />

&

<img width="1919" height="1079" alt="Screenshot 2026-09-27 145933" src="https://github.com/user-attachments/assets/7d0cc875-08b1-4010-918b-8a6ec4bdf282" />

Successful opening confirms the recovered password.

### JTR vs NetworkWalks

Feature	JTR + Johnny	NetworkWalks
Installation	Required	Not required
Interface	GUI	Web browser
Hash extraction	External tool	Hash Calculator
Password recovery	John the Ripper	Password Cracker
Main learning focus	Local password auditing	Browser-based password recovery
Password-Auditing Workflow

Both modules follow the same basic concept:

Password-Protected PDF
          ↓
     Hash Extraction
          ↓
       $pdf$ Hash
          ↓
   Password-Auditing Tool
          ↓
   Password Recovery
          ↓
   Password Verification

### Key Concepts
1. Password Hashes

A hash is a representation of password-related data used during password verification. Password-auditing tools can test candidate passwords against an appropriate hash format.

2. Password Recovery

Password-recovery tools generally test candidate passwords and compare the resulting verification data against the target.

Candidate Password
       ↓
Verification / Hash
       ↓
Compare with Target
       ↓
Match?

3. Password Complexity

Long, unique, and unpredictable passwords are generally more resistant to automated password guessing than short and predictable passwords.

### For this project:

Target:      Authorized lab PDF
Purpose:     Cybersecurity education
Environment: Controlled lab
Objective:   Understand password auditing

## References

1.John the Ripper

Openwall — John the Ripper
https://www.openwall.com/john/

Johnny GUI
https://openwall.info/wiki/john/johnny

PDF Hash Extraction Tool
https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php

2.NetworkWalks

Project Lab
https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/

Hash Calculator
https://networkwalks.com/hash-calculator/

Password Cracker
https://networkwalks.com/password-cracker/

## Conclusion

In this Week 3 project, I explored two approaches to password auditing using an authorized password-protected PDF.

Module 1:

PDF → Hash → John the Ripper → Password Recovery → Verification


Module 2:

PDF → NetworkWalks Hash Calculator → Password Cracker → Verification


This project improved my understanding of password hashes, password auditing, automated password guessing, password complexity, and ethical cybersecurity testing.

# 👤 Author

## Vraj Patel

### 🔗 LinkedIn

[LinkedIn Profile](https://www.linkedin.com/in/vraj-patel-vp8816/)

---
