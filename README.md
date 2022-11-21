# snapshot-airdrop-data
Query for Snapshot Voting To Be Used in Airdrop Txs


[Snapshot](https://snapshot.org/#/) is a tool for governance votes in Web3. It's an extremely useful tool for DAOs conducting votes, and the team at Snapshot has also compiled many useful tools to help users gather relevant data. 

# This repo shows the GraphQL query to run on a particular vote in order to identiy the addresses that engage in the vote. 

We then upload the addresses to Safe to distribute the relevant airdrop.

## Query:

query Votes {
  votes(first: 1000, skip: 0, where: {proposal: "0xb7f3e660bf7d358eb58cbe1957cb520aff83a0f7464486c305b629b9eeaeee2c"}, orderBy: "created", orderDirection: desc) {
    voter
  }
}
