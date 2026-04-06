# Assignment 2 - Theory Questions

## Question 1: Difference Between Hardened and Non-Hardened Keys

### Non-Hardened Keys
- Derived using the parent PUBLIC key + chain code
- Public key can be derived without the private key
- Useful for watch-only wallets
- RISK: If a child private key is leaked, an attacker can derive all sibling private keys

### Hardened Keys
- Derived using the parent PRIVATE key + chain code
- Public key CANNOT be derived without the private key
- More secure - even if child private key leaks, sibling keys are safe
- Used for account-level keys where security is critical
- Denoted with apostrophe in path e.g m/44'/0'/0'

## Question 2: Why Should a Wallet Developer Prefer Deterministic Wallets Over Non-Deterministic Wallets

### Non-Deterministic Wallets
- Keys are generated completely randomly one by one
- Each key has NO relationship to the others
- Must backup EVERY single key every time a new one is generated
- Losing backup means losing ALL Bitcoin
- Also called JBOK wallet (Just a Bunch Of Keys)

### Deterministic Wallets
- ALL keys derived from ONE single master seed
- Same seed always generates same keys
- Only need to backup ONE seed phrase
- Easy recovery - restore everything with 12 or 24 words
- Industry standard - BIP32, BIP39, BIP44

### Reasons to Prefer Deterministic Wallets
1. Simple Backup - only ONE seed phrase backs up ALL keys forever
2. Easy Recovery - restore with just 12 words
3. Better Privacy - fresh address for every transaction
4. Hierarchical Structure - organize keys by account and purpose
5. Watch-only Wallets - share public key only without risk
6. Industry Standard - universally supported
7. User Friendly - users only need to remember a seed phrase
