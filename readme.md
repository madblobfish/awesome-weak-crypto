# Awesome Crypto Papers  [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of weak [cryptographic](https://en.wikipedia.org/wiki/Cryptography) algorithms.
The recommendations are my personal opinion and are possibly not secure for all usecases.

## Asymmetric (public key) Encryption
* [Merkle–Hellman knapsack cryptosystem](https://en.wikipedia.org/wiki/Merkle%E2%80%93Hellman_knapsack_cryptosystem)

### avoid
* [ElGamal encryption system](https://en.wikipedia.org/wiki/ElGamal_encryption): malleable and should only be used with authentication. There exist secure variants.
* [Naccache–Stern knapsack cryptosystem](https://en.wikipedia.org/wiki/Naccache%E2%80%93Stern_knapsack_cryptosystem): although not broken it lacks provable security and should be avoided.

### recommendation
* [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)): with keysizes starting from 4098
* [X25519](https://en.wikipedia.org/wiki/Curve25519)

## Block Cipher Mode of Operation
* [ECB](https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation#ECB)

### avoid
* [EAX](https://en.wikipedia.org/wiki/EAX_mode): should only be used for disk encryption

### recommendation
* [CBC](https://en.wikipedia.org/wiki/Cipher_block_chaining)
* [GCM](https://en.wikipedia.org/wiki/Galois/Counter_Mode): avoid for persisted data.
* alternatively use a proven AEAD cipher+mac combination (for example chacha20+Poly1305)

## Cryptographic Hash Functions
* [GOST](https://en.wikipedia.org/wiki/GOST_(hash_function))
* [MD2](https://en.wikipedia.org/wiki/MD2_(hash_function))
* [MD4](https://en.wikipedia.org/wiki/MD4)
* [MD5](https://en.wikipedia.org/wiki/MD5)
* [PANAMA](https://en.wikipedia.org/wiki/Panama_(cryptography))
* [RIPEMD](https://en.wikipedia.org/wiki/RIPEMD)
* [SHA-0](https://en.wikipedia.org/wiki/SHA-1#SHA-0)
* [SHA1](https://en.wikipedia.org/wiki/SHA-1)
* all non cryptographic hash functions ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check), ...)

### recommendation
* [SHA-3](https://en.wikipedia.org/wiki/SHA-3)

## Cryptographically secure pseudo-random number generators
* []

### recommendation
* use `/dev/urandom` on linux

## Digital signatures
* []

### avoid
* [DSA](https://en.wikipedia.org/wiki/Digital_Signature_Algorithm): although not broken it is hard to implement correctly and should be avoided.
* [ECDSA](https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm): simmlar to DSA above.

### recommendation
* [EdDSA](https://en.wikipedia.org/wiki/EdDSA) or concretely: [ED25519](https://en.wikipedia.org/wiki/Ed25519)

## Key derivation functions, often used for password hashing and key stretching
* [crypt](https://en.wikipedia.org/wiki/Crypt_(C)): with this the original sheme is meant. But also other shemes are affected.
* []

### avoid
* []

### recommendation
* [Argon2id](https://en.wikipedia.org/wiki/Argon2): remember to properly tune the parameters
* [bcrypt](https://en.wikipedia.org/wiki/Bcrypt): Argon2 should be considered first
* [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2): Argon2 should be considered first
* [Scrypt](https://en.wikipedia.org/wiki/Scrypt): Argon2 should be considered first

## Key exchange algorithms
* []

## Message Authentication Codes
* [DAA](https://en.wikipedia.org/wiki/Data_Authentication_Algorithm)

## Secret sharing, Secret Splitting, Key Splitting, M of N algorithms
* []

## Symmatric (secret key) Encryption
* [3DES](https://en.wikipedia.org/wiki/Triple_DES)
* [A5/1](https://en.wikipedia.org/wiki/A5/1)
* [A5/2](https://en.wikipedia.org/wiki/A5/2)
* [DES](https://en.wikipedia.org/wiki/Data_Encryption_Standard)
* [IDEA](https://en.wikipedia.org/wiki/International_Data_Encryption_Algorithm)
* [MARS](https://en.wikipedia.org/wiki/MARS_(cipher))
* [RC2 or ARC2](https://en.wikipedia.org/wiki/RC2)
* [RC4 or ARC4](https://en.wikipedia.org/wiki/RC4)
* [RC5](https://en.wikipedia.org/wiki/RC5)
* [RC6](https://en.wikipedia.org/wiki/RC6)
* [TEA](https://en.wikipedia.org/wiki/Tiny_Encryption_Algorithm)

### avoid
* [Blowfish](https://en.wikipedia.org/wiki/Blowfish_(cipher)): not broken but weak

## Post-quantum cryptography
* []

## Proof-of-work algorithms
* []

## Other weak algorithms
* []

### padding schemes
* []
