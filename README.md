# Blockchain-Based Voting System

A simple command-line voting system built in Python that uses a custom blockchain to store and validate votes, ensuring transparency, immutability, and tamper-detection.

## Features
- Custom blockchain where each vote is stored as a block
- Each block is linked to the previous one using SHA-256 hashing
- Genesis block created automatically when the blockchain starts
- Prevents a voter from voting more than once
- Validates only allowed candidates
- Blockchain integrity validation by checking hashes and links
- Command-line menu to cast votes, display all votes, and validate the blockchain

## How It Works
- **Block class**: stores index, previous hash, timestamp, vote data (voter ID + candidate), and its own hash calculated using SHA-256
- **Blockchain class**: manages the chain, adds new blocks, and validates the chain by rechecking hashes and previous-hash links
- **VotingSystem class**: handles voting logic — candidate list, voter tracking (to stop double voting), and casting votes as new blocks

## Candidates
- Candidate A
- Candidate B
- Candidate C

## Tech Stack
- Python 3
- hashlib (SHA-256)
- json, time (standard library)

## Usage
Run the script:
```bash
python voting_system.py
```

Menu options:
1. Cast Vote
2. Display Votes
3. Validate Blockchain
4. Exit
