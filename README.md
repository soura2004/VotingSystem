VotingSystem Smart Contract
A simple decentralized voting system built in Solidity that allows users to:

✅ Create proposals

✅ Vote once per address

✅ View all proposals with vote counts

📦 Features
Any user can create a proposal with a description.

Each wallet address can vote only once.

Votes are counted on-chain and publicly viewable.

All proposals and vote counts are stored on-chain.

🧱 Contract Structure
🔹 struct Proposal
solidity
Copy
Edit

struct Proposal {
    string description;
    uint256 votes;
}
Each proposal has:

description: The proposal's text.

votes: Number of votes received.

🧪 Functions
✅ createProposal(string memory _desc)
Create a new proposal.

solidity
Copy
Edit

votingSystem.createProposal("Should we enable feature X?");
🗳️ vote(uint256 proposalId)
Vote on an existing proposal. Only one vote per address.

solidity
Copy
Edit

votingSystem.vote(0); // votes for the first proposal
📄 getProposals() view returns (Proposal[] memory)
Returns all current proposals with their descriptions and vote counts.

🔐 Restrictions
A wallet address can only vote once, across all proposals.

Proposals can be created by anyone.

No time limit or deadline (for simplicity).

🚧 Potential Improvements
Add per-proposal voting (1 vote per proposal instead of global).

Add owner/admin restrictions (e.g., proposal creation).

Include voting deadlines or quorum thresholds.

Integrate token-based voting power.

🛠️ Compile & Deploy
You can compile and deploy using:

Remix IDE

Hardhat / Truffle CLI

Third-party dApps (e.g., Thirdweb, Tally)


Hash Id 

