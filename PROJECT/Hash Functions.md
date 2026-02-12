Convert readable format to unreadable format using the mathematical format.

once converted means we can't decrypt that The hashing length was fixed. 

# What Is a Hash Function?

A mathematical function that converts any input into a fixed-length output.

It is **NOT encryption**.

Very important:  
❌ You cannot decrypt a hash  
❌ There is no key

It is **one-way only**.

The input change slightly means the output will completely different, Even it will change for the capital and the small characters also.
## Example:

Password 
# Types 

1. MD5
2. SHA 1
3. SHA 256
4. SHA 512
### 1. Fixed Length

No matter input size:

- 5 letters
- 1000 pages
- 10GB file
SHA-256 always gives 256-bit output.

Mainly hash functions are used in the password storage.
# Types

# 📊 Summary Table

| Type          | Example        | Usage             | Secure Today? |
| ------------- | -------------- | ----------------- | ------------- |
| MD Family     | MD5            | Old systems       | ❌ No          |
| SHA-1         | SHA-1          | Old SSL           | ❌ No          |
| SHA-2         | SHA-256        | HTTPS, blockchain | ✅ Yes         |
| SHA-3         | SHA3-256       | Modern apps       | ✅ Yes         |
| Password Hash | Bcrypt, Argon2 | Login systems     | ✅ Yes         |
| HMAC          | HMAC-SHA256    | API auth          | ✅ Yes         |
| SHA-512       |                |                   |               |