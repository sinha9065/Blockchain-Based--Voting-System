# Blockchain-Based Voting System

A simple command-line voting system built in Python that uses a custom blockchain to store and validate votes, ensuring transparency, immutability, and tamper-detection.

## Features
- **Custom Blockchain** — each vote is stored as a block, linked via SHA-256 hashes
- **Genesis Block** — chain initializes with a genesis block
- **Double-Voting Prevention** — tracks voter IDs to stop a voter from voting twice
- **Chain Validation** — verifies block hashes and previous-hash links to detect tampering
- **CLI Menu** — cast vote, display all votes, validate blockchain integrity, exit

## How It Works
1. `Block` class stores index, previous hash, timestamp, vote data, and its own hash (calculated via SHA-256 over its contents)
2. `Blockchain` class manages the chain — adding blocks and validating integrity by re-checking hashes and links
3. `VotingSystem` class wraps the blockchain with voting logic: candidate list, voter tracking, and vote casting

## Tech Stack
- Python 3
- `hashlib` (SHA-256)
- `json`, `time` (standard library)

## Usage
```bash
python voting_system.py
```
Menu options:
1. Cast Vote
2. Display Votes
3. Validate Blockchain
4. Exit

## Future Improvements
- Voter authentication (password/OTP)
- Persistent storage (database instead of in-memory)
- Web-based UI
- Proof-of-work / distributed nodes for real decentralization
