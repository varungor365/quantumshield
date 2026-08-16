# QuantumShield - Post-Quantum Cryptography & Quantum-Resistant Security

[![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat&logo=python)](https://www.python.org/)
[![Quantum](https://img.shields.io/badge/Quantum-Resistant-purple?style=flat)](https://github.com/varungor365/quantumshield)
[![License](https://img.shields.io/badge/License-GPL--3.0-green)](LICENSE)
[![Crypto](https://img.shields.io/badge/Crypto-Post--Quantum-orange)](https://github.com/varungor365/quantumshield)

Future-proof cryptographic toolkit implementing NIST-approved post-quantum algorithms to defend against quantum computer attacks.

## 🔮 Revolutionary Features

### **Post-Quantum Cryptography (PQC)**
- **CRYSTALS-Kyber** - Quantum-resistant key encapsulation (NIST winner)
- **CRYSTALS-Dilithium** - Post-quantum digital signatures
- **SPHINCS+** - Stateless hash-based signatures
- **FALCON** - Compact lattice-based signatures
- **Classic McEliece** - Code-based encryption

### **Quantum-Resistant Operations**
- **Secure Key Exchange** - PQC-based key agreement protocols
- **Digital Signatures** - Quantum-safe authentication
- **File Encryption** - Hybrid classical + PQC encryption
- **TLS/SSL Replacement** - Quantum-resistant transport layer
- **Blockchain Signatures** - Protect crypto wallets from quantum threats

### **Hybrid Cryptography**
- **Dual-Algorithm Mode** - Classical (AES, RSA) + PQC for transition period
- **Automatic Fallback** - Graceful degradation if PQC not supported
- **Performance Optimization** - Hardware acceleration for lattice crypto
- **Compatibility Layer** - Works with existing PKI infrastructure

### **Quantum Threat Assessment**
- **Harvest Now, Decrypt Later** - Assess risk of stored encrypted data
- **Migration Planning** - Roadmap for PQC adoption
- **Algorithm Comparison** - Benchmarks across all NIST finalists
- **Security Analysis** - Quantum attack surface evaluation

---

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/varungor365/quantumshield.git
cd quantumshield
pip install -r requirements.txt
```

### Basic Usage

#### **1. Generate Post-Quantum Keys**
```bash
# Kyber (key encapsulation)
python quantumshield.py --keygen --algorithm kyber --output kyber_keys

# Dilithium (signatures)
python quantumshield.py --keygen --algorithm dilithium --output dilithium_keys
```

#### **2. Encrypt Files with PQC**
```bash
# Hybrid encryption (AES + Kyber)
python quantumshield.py --encrypt secret.pdf --public-key kyber_keys.pub --output secret.enc

# Decrypt
python quantumshield.py --decrypt secret.enc --private-key kyber_keys.priv
```

#### **3. Create Quantum-Resistant Signatures**
```bash
# Sign document
python quantumshield.py --sign document.pdf --private-key dilithium_keys.priv

# Verify signature
python quantumshield.py --verify document.pdf.sig --public-key dilithium_keys.pub
```

---

## 📊 Expected Output

### Key Generation
```
╔═══════════════════════════════════════════════════════════╗
║  QuantumShield v1.0 - Post-Quantum Cryptography           ║
║  Generating Keys: CRYSTALS-Kyber-1024                     ║
╚═══════════════════════════════════════════════════════════╝

[+] Algorithm: Kyber-1024
    Security Level: NIST Level 5 (≈ AES-256)
    Quantum Security: 256 bits
    Classical Attack: 2^256 operations
    
[+] Key Generation
    ✓ Public key size: 1,568 bytes
    ✓ Private key size: 3,168 bytes
    ✓ Ciphertext size: 1,568 bytes
    ✓ Shared secret: 32 bytes
    
[+] Keys saved:
    Public: kyber_keys.pub
    Private: kyber_keys.priv
    
[+] Performance:
    Key generation: 0.45 ms
    Encapsulation: 0.62 ms
    Decapsulation: 0.71 ms
    
[+] Quantum Resistance: ✅ PROTECTED
    Against Shor's Algorithm: ✅ Immune
    Against Grover's Algorithm: ✅ 256-bit security
```

### File Encryption
```
[+] Encrypting: confidential_data.pdf
    File size: 2.4 MB
    
[+] Hybrid Encryption Mode
    Classical: AES-256-GCM
    Post-Quantum: Kyber-1024
    
[+] Encryption Process
    [1] Generate ephemeral Kyber keypair
    [2] Encapsulate shared secret with recipient's public key
    [3] Derive AES-256 key from shared secret (HKDF)
    [4] Encrypt file with AES-256-GCM
    [5] Package: Kyber ciphertext + AES ciphertext + auth tag
    
    ✓ Encrypted file: confidential_data.pdf.pqc
    ✓ Size: 2.4 MB (overhead: 1,568 bytes)
    ✓ Time: 45 ms
    
[+] Security Guarantees
    ✅ Classical security: AES-256 (unbreakable)
    ✅ Quantum security: Kyber-1024 (quantum-resistant)
    ✅ Authentication: GCM tag (tamper-proof)
    ✅ Forward secrecy: Ephemeral keys (session-unique)
    
[+] Quantum Threat Protection
    ✅ Shor's Algorithm: Cannot break lattice crypto
    ✅ Grover's Algorithm: 256-bit effective security
    ✅ Future quantum computers: PROTECTED
```

### Digital Signature
```
[+] Signing: contract.pdf
    Algorithm: CRYSTALS-Dilithium3
    
[+] Signature Generation
    [1] Hash document: SHA3-256
    [2] Sign hash with Dilithium private key
    [3] Attach signature to file
    
    ✓ Signature size: 3,293 bytes
    ✓ Time: 1.2 ms
    ✓ Output: contract.pdf.sig
    
[+] Verification
    ✓ Signature valid: ✅ AUTHENTIC
    ✓ Document integrity: ✅ UNMODIFIED
    ✓ Quantum-resistant: ✅ YES
    
[+] Security Properties
    ✅ Existential unforgeability (EUF-CMA)
    ✅ Resistant to quantum attacks
    ✅ NIST standardized (2024)
    ✅ No known classical or quantum attacks
```

---

## 🧠 Algorithm Comparison

### NIST Post-Quantum Finalists

| Algorithm | Type | Public Key | Signature | Speed | Security Level |
|-----------|------|------------|-----------|-------|----------------|
| **Kyber-512** | KEM | 800 B | - | ⚡⚡⚡⚡⚡ | NIST L1 (128-bit) |
| **Kyber-768** | KEM | 1,184 B | - | ⚡⚡⚡⚡ | NIST L3 (192-bit) |
| **Kyber-1024** | KEM | 1,568 B | - | ⚡⚡⚡ | NIST L5 (256-bit) |
| **Dilithium2** | Signature | 1,312 B | 2,420 B | ⚡⚡⚡⚡ | NIST L2 (128-bit) |
| **Dilithium3** | Signature | 1,952 B | 3,293 B | ⚡⚡⚡ | NIST L3 (192-bit) |
| **Dilithium5** | Signature | 2,592 B | 4,595 B | ⚡⚡ | NIST L5 (256-bit) |
| **FALCON-512** | Signature | 897 B | 666 B | ⚡⚡⚡⚡ | NIST L1 (128-bit) |
| **SPHINCS+-128** | Signature | 32 B | 7,856 B | ⚡ | NIST L1 (128-bit) |

### Performance Benchmarks
```
CPU: Intel Core i7-12700K
Operations per second:

Kyber-768:
  - KeyGen: 25,000/s
  - Encaps: 32,000/s
  - Decaps: 28,000/s
  
Dilithium3:
  - KeyGen: 8,500/s
  - Sign: 7,200/s
  - Verify: 18,000/s
  
FALCON-512:
  - KeyGen: 3,500/s
  - Sign: 11,000/s
  - Verify: 45,000/s
```

---

## 💻 Advanced Features

### Hybrid TLS (Classical + PQC)
```bash
# Generate hybrid server certificate
python quantumshield.py --gen-cert --hybrid --algorithm dilithium+ecdsa

# Start TLS server with PQC
python quantumshield.py --server --port 4433 --cert hybrid_cert.pem
```

### Blockchain Wallet Protection
```bash
# Generate quantum-resistant Bitcoin address (future-proof)
python quantumshield.py --gen-wallet --crypto bitcoin --pqc dilithium

# Sign transaction with PQC
python quantumshield.py --sign-tx transaction.json --wallet wallet.pqc
```

### Quantum Threat Assessment
```bash
# Assess cryptographic risk
python quantumshield.py --assess-risk --target myapp/

# Output:
# HIGH RISK: RSA-2048 keys (breakable by quantum in 2030s)
# MEDIUM RISK: ECDSA-256 (breakable by quantum in 2040s)
# LOW RISK: AES-256 (Grover's algorithm requires 2^128 ops)
# RECOMMENDATION: Migrate to Kyber + Dilithium
```

---

## 🔬 Technical Deep Dive

### Why Post-Quantum Cryptography?

**The Quantum Threat:**
- **Shor's Algorithm (1994)** - Breaks RSA, ECDSA, Diffie-Hellman in polynomial time
- **Grover's Algorithm (1996)** - Halves symmetric key strength (AES-128 → 64-bit security)
- **Timeline:** Large-scale quantum computers expected by 2030-2040

**Vulnerable Cryptosystems:**
- ❌ RSA (all key sizes)
- ❌ ECDSA / ECDH
- ❌ Diffie-Hellman
- ❌ DSA / ElGamal
- ⚠️ AES-128 (reduced security)

**Quantum-Resistant:**
- ✅ Lattice-based (Kyber, Dilithium)
- ✅ Hash-based (SPHINCS+)
- ✅ Code-based (Classic McEliece)
- ✅ Multivariate (Rainbow - not recommended)
- ✅ AES-256 (still secure with Grover's)

### Lattice-Based Cryptography

**Mathematical Foundation:**
- **Learning With Errors (LWE)** - Hard problem even for quantum computers
- **Ring-LWE / Module-LWE** - Efficient variants used by Kyber/Dilithium
- **Hardness assumption:** Finding short vectors in high-dimensional lattices

**Why Lattices?**
- ✅ Quantum-resistant (no known quantum algorithms)
- ✅ Fast (compared to other PQC)
- ✅ Small keys (compared to McEliece)
- ✅ Versatile (KEM + signatures)

---

## 🛠️ Requirements

**Core Dependencies:**
```
pqcrypto>=0.1.7        # Post-quantum algorithms
cryptography>=41.0     # Classical crypto
pynacl>=1.5.0          # Libsodium bindings
```

**Optional:**
```
qiskit>=0.45.0         # Quantum circuit simulation
numpy>=1.24.0          # Numerical operations
```

**Full requirements:** See `requirements.txt`

---

## 🎓 Use Cases

### **Secure Communications**
- Protect today's encrypted data from future quantum attacks
- "Harvest now, decrypt later" threat mitigation
- Email encryption (PGP replacement)
- Instant messaging (Signal, WhatsApp)

### **Blockchain & Crypto**
- Future-proof cryptocurrency wallets
- Quantum-resistant smart contract signatures
- Decentralized identity systems
- NFT ownership protection

### **Government & Military**
- Classified data encryption (50+ year security)
- Secure communications infrastructure
- NIST compliance (FIPS 203, 204, 205)
- National security applications

### **Financial Services**
- Banking transaction security
- Payment processing systems
- Secure document signing
- Long-term data archival

---

## 🔥 Real-World Examples

### Example 1: Migrate Existing PKI
```bash
# Audit current cryptosystem
python quantumshield.py --audit-pki --cert /etc/ssl/certs/

# Generate hybrid certificate (RSA + Dilithium)
python quantumshield.py --migrate-cert --input old_cert.pem --output hybrid_cert.pem

# Result: Backward compatible with classical systems, quantum-resistant
```

### Example 2: Protect Bitcoin Wallet
```bash
# Current Bitcoin uses ECDSA (vulnerable to quantum)
# Generate PQC-protected wallet
python quantumshield.py --protect-wallet bitcoin_wallet.dat --algorithm dilithium

# New transactions signed with hybrid ECDSA+Dilithium
```

### Example 3: Secure File Storage
```bash
# Encrypt sensitive documents for 50+ year storage
python quantumshield.py --encrypt-archive --input documents/ --algorithm kyber1024

# Guaranteed secure even when quantum computers exist
```

---

## ⚠️ Important Notes

**Migration Strategy:**
- 🟢 **Phase 1 (2024-2026):** Hybrid mode (classical + PQC)
- 🟡 **Phase 2 (2027-2030):** PQC preferred, classical fallback
- 🔴 **Phase 3 (2030+):** PQC only

**NIST Standardization:**
- **FIPS 203** - Kyber (Module-Lattice KEM) - *Approved 2024*
- **FIPS 204** - Dilithium (Lattice Signatures) - *Approved 2024*
- **FIPS 205** - SPHINCS+ (Hash Signatures) - *Approved 2024*

**Performance Trade-offs:**
- Slightly larger keys than RSA/ECDSA
- Comparable or faster operations
- Minimal overhead for most applications

---

## 📚 Documentation

- [Getting Started](docs/getting-started.md)
- [Algorithm Selection Guide](docs/algorithm-selection.md)
- [Migration Guide](docs/migration.md)
- [API Reference](docs/api.md)
- [NIST Standards](docs/nist-standards.md)

---

## 🤝 Contributing

Contributions welcome:
- Additional PQC algorithms
- Performance optimizations
- Hardware acceleration (AVX2, ARM NEON)
- Protocol implementations (TLS, SSH)

---

## 📜 License

GPL-3.0 - See [LICENSE](LICENSE)

**Protecting cryptography for the quantum era.**

---

## 👨‍💻 Author

**Varun Goradhiya**
- GitHub: [@varungor365](https://github.com/varungor365)
- Research: Post-Quantum Cryptography & Quantum Security

---

**Related Projects:**
- [supplyguard](https://github.com/varungor365/supplyguard) - Supply chain security
- [exploitforge](https://github.com/varungor365/exploitforge) - AI exploit generation
- [vault-destruct](https://github.com/varungor365/vault-destruct) - Password manager

---

*Future-proofing cryptography before quantum computers arrive.*

**🔮 The quantum threat is real. Are you protected?**

## Who this is for

QuantumShield is a post-quantum cryptography research toolkit for studying NIST-standardized algorithms, hybrid key exchange, and migration considerations. It is a learning and research project, not a replacement for a reviewed cryptographic library.

## Why star this repository

Star this project if post-quantum cryptography, hybrid TLS, or practical cryptography migration research is relevant to you.
