# ** MEV Resistant ERC20 (Same Block Solution) **

### **Summary**
Everyone hates sandwich attacks, except for those attacking. This ERC20 contract discourages them
by preventing a buy and sell in the same block. A person will be unable to sell their coins
unless they wait 1 block (typically 10-15 seconds on Ethereum).

### **Description**
Since sandwich attacks are greatly reliant on speedy execution, the "same block restriction" may discourage them altogether. By the time the attacker can sell, their profit may have completely disappeared.

For details, see MEVResistantERC20.sol, specifically the _beforeTokenTransfer and _afterTokenTransfer functions.

An alternative and likely more robust solution utilizing longer cooldown times can be found here: https://github.com/GregoryUnderscore/MEV-Resistant-ERC20

Forked from $APE.

Original Smart Contract: https://etherscan.io/address/0x4d224452801aced8b2f0aebe155379bb5d594381#code#F5#L1

### **How to Use**
1. Fork the code.
2. Add appropriate whitelists (i.e. Uniswap etc.) via the addTimeRestrictionWhitelist function (only the contract owner can do this).
