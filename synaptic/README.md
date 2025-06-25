# Neural Trust Network - Basic Synaptic Credit System v1.0

A Clarity-based smart contract that simulates a **cognitive lending system** using neural metaphors. This system assigns lending capacity based on activity-driven **synaptic strength**, enabling decentralized trust, neural credit formation, and pathway-based resource allocation.

---

## 🚀 Overview

The **Neural Trust Network** is a novel decentralized identity and lending protocol inspired by the human brain's neural architecture. It introduces concepts such as:

- **Synaptic strength**: Determines a node’s influence and borrowing power.
- **Neural pathways**: Lending channels created by eligible users.
- **Cognitive lending**: Lending based on verified behavioral and activity metrics.

---

## 🧩 Key Concepts

| Concept              | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `synaptic-strength`  | A score that represents a user's reliability, based on their activity.       |
| `neural-pathways`    | Lending channels that users can create if they meet the required threshold. |
| `data-providers`     | Authorized oracles responsible for recording user activity.                 |
| `activity-records`   | Metrics such as transaction volume, count, and account age.                 |
| `NEURAL_ARCHITECT`   | Contract deployer with special admin rights.                                |

---

## 🔐 Access Control

- Only the **NEURAL_ARCHITECT** can:
  - Toggle the network on/off.
  - Authorize or revoke data providers.

- Only **authorized data providers** can:
  - Record activity.
  - Update synaptic strength.

- Any **eligible user** can:
  - Create and close neural pathways.

---

## 🧠 Synaptic Strength Logic

Synaptic strength is computed from:

1. **Transaction Volume**  
2. **Number of Transactions**  
3. **Account Age**

These are weighted and capped to avoid manipulation. Strength must be above a threshold (`MIN_SYNAPTIC_THRESHOLD`) to be eligible for lending.

---

## 📦 Functions

### ✅ Read-only Functions

| Function | Description |
|---------|-------------|
| `get-synaptic-strength(node)` | Returns the synaptic strength of a node. |
| `get-neural-profile(node)` | Returns the full neural profile. |
| `get-lending-capacity(node)` | Calculates the max credit a user can borrow. |
| `get-pathway(pathway-id)` | Retrieves details of a neural pathway. |
| `check-eligibility(node, amount)` | Checks if the user can borrow a specified amount. |

---

### 🔄 Public Functions

| Function | Description |
|---------|-------------|
| `record-activity(user, transactions, volume, age)` | Records user behavior for scoring. |
| `update-synaptic-strength(node)` | Recalculates synaptic strength using activity. |
| `create-pathway(amount)` | Creates a new neural pathway (if eligible). |
| `close-pathway(pathway-id)` | Closes an active neural pathway. |
| `authorize-provider(provider)` | Grants permission to submit data. |
| `revoke-provider(provider)` | Removes a provider’s permission. |
| `toggle-network()` | Turns the protocol on/off. |

---

## 🧪 Errors

| Error Code | Meaning |
|------------|---------|
| `u400` | Access denied: Not authorized |
| `u401` | Synaptic strength too low |
| `u402` | Cognitive data missing |
| `u403` | Pathway not found |
| `u405` | Insufficient neural power (credit) |

---

## 🔧 Constants

| Constant | Value |
|----------|-------|
| `MIN_SYNAPTIC_THRESHOLD` | `u500` |
| `NEURAL_AMPLIFICATION_FACTOR` | `u50` |
