# Chapter 57: Blockchain & Web3 Development

**Last Updated:** February 5, 2026

---

## Overview

This chapter covers blockchain and Web3 development skills for building decentralized applications, smart contracts, and cryptocurrency integrations.

### Skills Covered in This Chapter

| Skill | Purpose | Complexity |
|-------|---------|------------|
| `@blockchain-developer` | General blockchain development | Intermediate |
| `@solidity-security` | Smart contract security | Advanced |
| `@defi-protocol-templates` | DeFi protocol patterns | Advanced |
| `@nft-standards` | NFT implementation standards | Intermediate |
| `@web3-testing` | Web3 application testing | Intermediate |

---

## 57.1 Blockchain Development with @blockchain-developer

### Skill Introduction

The `@blockchain-developer` skill provides comprehensive guidance for blockchain application development across multiple platforms.

**When to use:** Building dApps, integrating blockchain features, or developing smart contracts.

---

### Skill Prompts

#### Designing a Blockchain Application

```text
@blockchain-developer Design a blockchain-based application for:

Use case: Supply chain tracking

Requirements:
- Track product origin to delivery
- Immutable record of transfers
- Multi-party verification
- Integration with existing ERP

Please provide:
1. Blockchain platform recommendation
2. Smart contract architecture
3. Data model design
4. Integration approach
5. Gas optimization strategies
```

**Expected Output:**
- Platform comparison (Ethereum, Polygon, Solana)
- Contract structure and functions
- Off-chain vs on-chain data decisions
- API integration patterns

---

## 57.2 Smart Contract Security with @solidity-security

### Skill Introduction

The `@solidity-security` skill focuses on writing secure Solidity smart contracts and identifying vulnerabilities.

**Key areas:**
- Common vulnerability patterns
- Security best practices
- Audit preparation
- Testing strategies

---

### Skill Prompts

#### Security Audit for Smart Contract

```text
@solidity-security Audit this smart contract for vulnerabilities:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleVault {
    mapping(address => uint256) public balances;
    
    function deposit() external payable {
        balances[msg.sender] += msg.value;
    }
    
    function withdraw(uint256 amount) external {
        require(balances[msg.sender] >= amount);
        (bool success, ) = msg.sender.call{value: amount}("");
        require(success);
        balances[msg.sender] -= amount;
    }
}
```

Check for:
1. Reentrancy vulnerabilities
2. Integer overflow/underflow
3. Access control issues
4. Gas optimization opportunities
```

---

## 57.3 DeFi Protocols with @defi-protocol-templates

### Skill Introduction

The `@defi-protocol-templates` skill provides patterns for building DeFi applications including lending, staking, and DEX protocols.

---

### Skill Prompts

#### Building a Staking Protocol

```text
@defi-protocol-templates Design a staking protocol:

Requirements:
- Users stake ERC20 tokens
- Earn rewards over time
- Flexible unstaking with cooldown
- Reward distribution mechanism

Include:
1. Contract architecture
2. Reward calculation logic
3. Emergency functions
4. Admin controls
5. Testing scenarios
```

---

## 57.4 NFT Development with @nft-standards

### Skill Introduction

The `@nft-standards` skill covers NFT implementation following ERC-721 and ERC-1155 standards.

---

### Skill Prompts

#### Creating an NFT Collection

```text
@nft-standards Create an NFT collection smart contract:

Collection details:
- 10,000 unique items
- Reveal mechanism
- Royalty support (ERC-2981)
- Whitelist minting phase

Include:
1. Contract implementation
2. Metadata structure
3. Minting logic
4. Reveal mechanism
5. Marketplace compatibility
```

---

## 57.5 Web3 Testing with @web3-testing

### Skill Introduction

The `@web3-testing` skill provides testing strategies for blockchain applications.

---

### Skill Prompts

#### Creating a Test Suite

```text
@web3-testing Create a comprehensive test suite for:

Contract: Token vesting contract

Test coverage needed:
- Unit tests for all functions
- Integration tests
- Edge cases
- Gas consumption benchmarks

Framework preference: Hardhat + Chai

Include test structure and example tests.
```

---

## Best Practices Summary

### Smart Contract Development
- **Security first:** Audit before deployment
- **Gas efficiency:** Optimize storage and computation
- **Upgradeability:** Plan for contract upgrades
- **Testing:** Extensive test coverage

### DeFi Specifics
- **Reentrancy guards:** Use checks-effects-interactions
- **Oracle security:** Validate price feeds
- **Flash loan resistance:** Consider attack vectors
- **Time locks:** Implement governance delays

### NFT Development
- **Metadata standards:** Follow OpenSea standards
- **Gas optimization:** Batch minting
- **Royalty support:** Implement ERC-2981
- **Reveal timing:** Secure randomness

---

## Reflection Points

1. How do you balance decentralization with user experience?
2. What security measures are non-negotiable for production contracts?
3. How do you handle upgrades in immutable systems?
4. What testing coverage is sufficient for financial contracts?

---

**Previous Chapter:** [← Chapter 56: AI Agents & LLM](56-ai-agents-llm.md)

**Appendices:** [Appendix A: Skills Reference →](../appendices/a-skills-reference.md)
