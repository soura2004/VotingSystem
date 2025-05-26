🗳️ VotingSystem Smart Contract
A simple and gas-efficient decentralized voting system built using Solidity.
It allows users to create proposals and vote on them using their Ethereum wallet address. Each user can vote only once, ensuring fair and transparent governance.

📌 Features
✅ Create proposals with a description.

🗳️ Vote on any existing proposal.

🔒 One vote per wallet (prevents duplicate voting).

📊 Public visibility of all proposals and vote counts.

🔍 Smart Contract Overview
👷 Structs
solidity
Copy
Edit

struct Proposal {
    string description;
    uint256 votes;
}
🧠 Mappings
mapping(address => bool) public hasVoted;
Ensures each address can vote only once.

🔧 Functions
createProposal(string memory _desc)
Allows any address to create a proposal.

Input: A short description string.

solidity
Copy
Edit

createProposal("Should we add a new feature?");
vote(uint256 proposalId)
Cast a vote for a proposal by its index.

Restrictions:

Only one vote per address.

Proposal ID must be valid.

solidity
Copy
Edit

vote(0); // votes for the first proposal
getProposals() view returns (Proposal[] memory)
Returns the list of all proposals with:

description

vote count

🛠️ Deployment
This contract can be compiled and deployed using:

Remix IDE

Hardhat

Truffle

Example in Remix:
Paste the code into Remix.

Compile with Solidity version ^0.8.20.

Deploy to a local or testnet environment.

Interact with createProposal, vote, and getProposals.

🚨 Limitations
Each address can vote only once across all proposals.

No time limits or proposal expiration.

No role-based permissions (e.g., anyone can create a proposal).

🚀 Future Improvements (Optional)
Allow 1 vote per proposal instead of globally.

Add admin-only access to proposal creation.

Implement voting deadlines and quorum requirements.

Token-weighted voting (ERC-20 governance).

Event logging for votes and creations.

📄 License
This project is licensed under the MIT License.

🙌 Contribution
Feel free to fork, modify, and propose improvements!
Pull requests are welcome for bug fixes, upgrades, and enhancements.

Contract Address
0xcce7ee74bd996ec9ce8bcf576bdced29ea5cb6ef

Hash Id 
0xcc95f071b0cddc1aa5a947c91e3538a0a1555b26f783658d25d19f5e5651f810

![Id 0xcc95f071b0cddc1aa5a947c91e3538a0a1555b26f783658d25d19f5e5651f810](https://github.com/user-attachments/assets/98cce9c8-0c8e-4f14-b9d0-88aaf5f48446)

