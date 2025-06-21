# compound-v3-phantom-minting

🚨 **Critical Exploit Disclosure**  
Phantom mint bug in Compound v3 – allows inflation of `totalsSupply` using fake ERC20 tokens.

## 📌 Summary
This exploit abuses the way `approve()` and `transferFrom()` interact with Comet v3 and unverified token contracts.  
By deploying a fake ERC20 token with custom `decimals()` and spoofed balances, attackers can mint unlimited cTokens.

## 🧪 PoC & Exploit Code
- `Exploit.sol` — full reproducible attack
- `FakeToken.sol` — custom token with controlled decimals
- `Compound_Report.zip` — includes screenshots, transactions, and technical report

## 🧠 Impact
- Zero-value tokens result in phantom minting
- Users can drain liquidity pools
- Losses are untraceable if exploited via mixed RPC routes

## 🔗 Live Repo:
https://github.com/MattysInc-Sec/compound-v3-phantom-minting

## © MattysInc – Whitehat Researcher  
mattysinc@protonmail.com
