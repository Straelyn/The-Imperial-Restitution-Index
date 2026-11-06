# The Imperial Restitution Index — EVE Frontier

Put EVE on a pilot's head. Whoever destroys that pilot's ship collects it. Payouts are checked on chain against the world's own **killmail**, which only CCP's server can create, so nobody has to be trusted to say who killed whom.

**Play / dApp:** https://straelyn.github.io/The-Imperial-Restitution-Index/

## How it works

1. **Post a bounty:** paste a pilot's chat link or character id, pick an amount (minimum 10 EVE) and 1–30 days. The EVE is held by the contract.
2. **Claim:** after you destroy the pilot's ship, use the in-game button to report your kill so it reaches the chain at once, then open the **Claim** tab and press *Find my kills*. The page finds your killmail and the contract pays you, less the board's fee (1%).
3. **Refund:** if nobody collects, you can take your EVE back 3 days after the bounty expires. The delay is there because killmails reach the chain a median of ~80 minutes after the kill, and sometimes days later.

## Rules (enforced by the contract)

- No bounties on yourself, or on pilots in your own tribe.
- The killmail must be a **ship** loss whose victim is the target and whose killer is the claimer.
- The kill must fall between the bounty being posted and its expiry.
- The poster cannot claim their own bounty, and the target cannot collect on themselves.
- Pays in EVE only. NPC kills never produce killmails, so they don't count.

## On chain (Sui testnet, Stillness)

- Package `0xca5cd8aa697a0cf896ec84ec30f293a22f208e990a6b5dd169e572c4dcfdefa0` (module `board`)
- Board `0x506bc71307e966eeb69cf14b743887238e741ac8c49685676af150ed41c81d1f`
- 27 Move tests, including full post / claim / refund runs against the real world contracts.

Direct revisions or contract updates to **Strae on Discord**.
