# Asymmetric Cryptography

Also called **Public Key Cryptography**

### 🔑 Concept:

Two different keys:

- Public Key (shared with everyone)
- Private Key (kept secret)

What one key encrypts, the other decrypts.

Data encrypted with one key can only be decrypted with the other key.

---
### 📦 Example:

Bank has:
- Public key (anyone can see)
- Private key (only bank knows)

You:

- Encrypt message using bank’s public key
- Only bank can decrypt using private key

Even if hacker sees public key → cannot decrypt.

---
### ✅ Characteristics:

- More secure key exchange
- Slower than symmetric
- Used for authentication & key exchange

---
### 🔐 Examples:

- RSA
- ECC (Elliptic Curve Cryptography)
- Diffie-Hellman

---
### 🌐 Used In:

- SSL/TLS
- Digital certificates
- Secure login
- Key exchange

# Usages 
## 1️⃣ Internet (HTTPS – Every Secure Website)'

When you visit:

```d
https://bank.com
https://google.com
https://amazon.in
```

