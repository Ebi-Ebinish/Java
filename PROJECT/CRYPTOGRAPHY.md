# CRYPTOGRAPHY
###### Imagine I am sending a letter to Lawrence with normal white paper without any secure box or something  just only the paper alone, now that paper while going to Lawrence in between the sender or that postman or the staff anyone can read that paper and anyone can change content in that paper not secure right.
###### now your sending that same paper with some some boxed with the locked that box has only two keys one  in your hand and another one is your Lawrence has.
###### now in between no one can read or change that content your data's is secure.

# So What Is Cryptography?

Cryptography is:

> The science of protecting information by converting it into a secret form so only authorized people can read it.

Simple definition:  
It turns **readable data → unreadable data**.

# Why Cryptography is needed 

In the real usage is your logging a bank website some details changing.
that request works with internet ---> routers ---> server.
If without cryptography means the hacker read your data and change your data.

#### When you:

- Log in to a website
- Use internet banking
- Send WhatsApp messages
- Pay using UPI
- Enter your ATM PIN

#### Your data travels through:

	Internet → routers → servers → multiple systems

#### Without protection:

- Hackers can read passwords
- Bank data can be stolen
- Messages can be modified

So we need cryptography.

# What Problems Does Cryptography Solve?

Cryptography solves 4 main problems:

---
## 1️⃣ Confidentiality (Privacy)

Ensures:  
Only intended person can read the data.

Example:  
Your password should not be readable by hackers.

---
## 2️⃣ Integrity (No Modification)

Ensures:  
Data is not changed during transmission.

Example:  
If you transfer ₹10,000  
It should not become ₹100,000.

---
## 3️⃣ Authentication (Identity Verification)

Ensures:  
You are really talking to the correct person/system.

Example:  
When you open a bank website,  
You must be sure it is the real bank, not fake.

---
## 4️⃣ Non-Repudiation (No Denial)

Ensures:  
Sender cannot deny sending the message.

Used in:

- Digital signatures
- Online contracts

#### Process:
- Encryption → Plaintext → Ciphertext
- Decryption → Ciphertext → Plaintext
---
#  What Makes Encryption Work?

Encryption needs something called a **Key**.

#### Think of a key like:

- A password
- A secret number
- A secret formula

#### Without the correct key:  
	You cannot convert ciphertext back to plaintext.

#### The security depends on:

- Strength of algorithm
- Length of key
- How safely key is stored



