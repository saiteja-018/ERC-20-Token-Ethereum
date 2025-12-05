# LEARNING.md – Reflections on Building MyToken

## Why I Built This

I wanted to understand how real tokens on Ethereum work internally, not just trade them in a wallet. Implementing ERC-20 from scratch helped me see how balances, allowances, and events are actually stored and updated on-chain.

## Challenges Faced

- Understanding how `decimals` affects total supply and UI display.
- Getting `transferFrom` + `approve` logic correct (allowance decreasing, error messages).
- Remembering to emit `Transfer` and `Approval` events in the right places.
- Debugging reverts in Remix and reading error messages carefully.

## Key Takeaways

- ERC-20 is mostly about **consistency**: if you follow the standard, any wallet or dApp can integrate your token.
- Events are essential for transparency and off-chain indexing.
- Input validation (zero address checks, balance checks, allowance checks) is the first line of defense against bugs and misuse.
- Even a "simple" token requires precise thinking about state changes.

## Next Steps

- Learn about OpenZeppelin’s ERC-20 implementation and compare it with my custom one.
- Explore features like minting, burning, and pausable tokens.
- Deploy the token to a public testnet and interact with it using a frontend or Etherscan.
