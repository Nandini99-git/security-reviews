# Smart Contract Audit Report: PasswordStore

A security review of the `PasswordStore` smart contract protocol, conducted by **Nandini Gupta**.

## 📝 About the Project

`PasswordStore` is a simple Solidity-based protocol designed for the secure storage and retrieval of a user's password. The intended design is for a single-user system where only the contract owner can set and access the sensitive data.

## 🔍 Audit Summary

This repository contains a comprehensive security audit of the `PasswordStore.sol` contract. The audit identifies several critical vulnerabilities that could lead to complete loss of privacy and unauthorized access.

- **Lead Auditor:** [Nandini Gupta](https://github.com/Nandini99-git)
- **Timeframe:** June 2026
- **Status:** Completed
- **Commit Hash:** `2e8f81e263b3a9d18fab4fb5c46805ffc10a9990`

## 📊 Findings Overview

The audit discovered a total of **4 issues**, ranging from architectural flaws to documentation errors.


| Severity | Count |
| :--- | :--- |
| 🔴 **High** | 2 |
| 🟡 **Medium** | 0 |
| 🔵 **Low** | 1 |
| ⚪ **Info** | 1 |

### Key Vulnerabilities Found:
*   **[H-1] Data Visibility:** Passwords stored in `private` variables are still readable by anyone directly from the blockchain storage slots.
*   **[H-2] Missing Access Control:** The `setPassword` function lacks a `require` or `modifier` check, allowing any address to overwrite the owner's password.

## 📄 Final Report

The full PDF version of the audit report, including Proof of Concepts (PoC) and detailed mitigation steps, can be found here:

👉 **[Download the PDF Audit Report](./PasswordStore-audit.pdf)**

## 🛠️ Tools Used
- **Foundry / Cast** (for storage exploitation & testing)
- **Solidity**
- **Pandoc & XeLaTeX** (for report generation)

---
*Disclaimer: This audit report is not an endorsement of the project. It was a time-boxed review focused on the security of the Solidity implementation.*
