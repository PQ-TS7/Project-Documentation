# Glossary

| Term | Meaning |
| --- | --- |
| ADR | Architecture Decision Record |
| CA | Certificate Authority — issues and signs certificates |
| CRL | Certificate Revocation List (RFC 5280 v2), published periodically |
| CSR | Certificate Signing Request |
| DNS-01 / HTTP-01 | Domain-control validation challenges (TXT record / well-known HTTP file) |
| DUNS | Dun & Bradstreet D-U-N-S number, used as an external organization identifier |
| FIPS 204 | NIST standard defining ML-DSA |
| HSM | Hardware Security Module; SoftHSM2 emulates one via PKCS#11 |
| Intermediate CA | Online issuing CA; key held behind PKCS#11 |
| liboqs / oqs-provider | Open Quantum Safe library and its OpenSSL 3 provider |
| ML-DSA | Module-Lattice Digital Signature Algorithm (44 / 65 / 87 parameter sets) |
| OCSP | Online Certificate Status Protocol — real-time revocation status |
| OV | Organization Validation — verifying the applicant organization is real and authorized |
| OV agent | AI service that produces an advisory OV assessment; a human RA officer decides |
| PKCS#11 | Standard API for cryptographic tokens / HSMs |
| PQC | Post-Quantum Cryptography |
| RA | Registration Authority — validates requests before the CA signs |
| RAG | Retrieval-Augmented Generation |
| RBAC | Role-Based Access Control |
| Root CA | Offline, air-gapped trust anchor |
| RFC 9881 | ML-DSA in X.509 certificates |
