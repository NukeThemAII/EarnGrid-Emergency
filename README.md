# EarnGrid Emergency Withdrawal

Standalone emergency page to withdraw USDC from [EarnGrid](https://earngrid.site) vaults and
underlying MetaMorpho strategies **when the main website is down**.

🔗 **Live:** https://nukethemaII.github.io/EarnGrid-Emergency/

## What it does

- Connect MetaMask (Base chain, chainId 8453)
- **Section 1:** Redeem bvUSDC shares from the BlendedVault for USDC
- **Section 2:** Redeem directly from MetaMorpho strategy vaults (emergency bypass)

## How it works

Single self-contained HTML file. No server, no build step, no npm. Uses ethers.js v6
from CDN. All reads go through public RPC (`base-rpc.publicnode.com`), writes go
through your wallet's injected provider.

## Contracts

| Contract | Address |
|---|---|
| BlendedVault | `0x8694D7D44309665D51Cb5002fceC0454f1c233dE` |
| USDC | `0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913` |
| Gauntlet USDC Prime | `0xeE8F4eC5672F09119b96Ab6fB59C27E1b7e44b61` |
| Steakhouse Prime USDC | `0xBEEFE94c8aD530842bfE7d8B397938fFc1cb83b2` |
| Moonwell Flagship USDC | `0xc1256Ae5FF1cf2719D4937adb3bbCCab2E00A2Ca` |
| Gauntlet USDC Frontier | `0x236919F11ff9eA9550A4287696C2FC9e18E6e890` |
| Steakhouse High Yield USDC | `0xBEEFA7B88064FeEF0cEe02AAeBBd95D30df3878F` |

## Security

This page holds NO credentials. All contract addresses are public onchain data.
Transactions are signed by YOUR wallet — this page never sees your private key.

Always verify transaction details in your wallet before signing.

## Source

Maintained as part of the [EarnGrid](https://github.com/NukeThemAII/EarnGrid) project.
