# What is a Digital Signature?

A **Digital Signature** is a cryptographic mechanism used to:

1.  Prove who sent the message (**Authentication**)
2.  Ensure the message was not changed (**Integrity**)
3.  Prevent the sender from denying it later (**Non-repudiation**)

It is created using **asymmetric cryptography** (public & private key).
## Step 1: Create Hash of Message

Suppose message is:

`Transfer ₹10,000 to Ravi`

We generate hash using SHA-256:

`A9F3C7X892...`

This hash is:

- Fixed size
- Unique to the message
- Changes even if 1 letter changes

---
## Step 2: Encrypt Hash Using Private Key

Sender uses their **Private Key** to encrypt the hash.

Encrypted hash = **Digital Signature**

---
## Step 3: Send

Sender sends:

- Original Message
- Digital Signature

---
## Step 4: Verification

Receiver:

1. Hashes the received message again
2. Decrypts signature using sender’s **Public Key**
3. Compares both hashes

If both match:

 Message not modified  
 Sender is authentic  
 Cannot deny sending