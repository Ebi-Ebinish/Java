Combines symmetric and asymmetric for best of both.

- How: Use asymmetric to exchange a symmetric session key, then symmetric for bulk data.
- Example: TLS/HTTPS – RSA/ECDH for key exchange, AES for encryption.
- Depth: In TLS 1.3, ephemeral Diffie-Hellman ensures forward secrecy (past sessions safe if key compromised later).

Advantages: Efficiency + secure key distribution.