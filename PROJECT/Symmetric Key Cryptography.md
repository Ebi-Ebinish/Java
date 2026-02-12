# Symmetric Cryptography 

Symmetric cryptography means the key used both encryption and decryption.
### Example

If your sending an ATM pin 4589.
ATM does NOT send `4589` to bank.
ATM encrypts it using a **symmetric key** stored inside secure hardware (HSM).
Bank uses the **same secret key** to decrypt and verify.
### 📦 Example:

You and your friend share a secret password:

`Key = 12345`

You encrypt message using 12345  
Your friend decrypts using 12345

If someone gets the key → security broken.

---
### ✅ Characteristics:

- Very fast
- Good for large data
- Used in bulk encryption

### 🔐 Examples:

- AES (modern standard)
- 3DES (old)
- DES (obsolete)
---
### 🏦 Where Used:

- HTTPS session encryption
- Disk encryption
- ATM PIN encryption
- Database encryption

---
#### Advantages

- Fast and efficient (low computational overhead, suitable for large data).
- Simple to implement in hardware.

#### Disadvantages

- Key distribution problem: How to securely share the key? (Solved by asymmetric methods in practice.)
- Not suitable for scenarios with many parties (each pair needs a unique key).
- Vulnerable to key compromise if the key is intercepted.

### ⚠ Problem:

How do you securely share the key?

That problem is solved by asymmetric cryptography.

Same key used on both sides → That is symmetric cryptography.

---