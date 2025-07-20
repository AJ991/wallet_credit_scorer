# 📊 DeFi Wallet Credit Score — Analysis Report

This analysis evaluates wallet-level behavior on the Aave V2 protocol by examining their interactions with DeFi lending and borrowing features. Using engineered features and unsupervised learning, we derive a credit score (0–1000) to represent each wallet's financial reliability.

---

## ⚙️ Feature Summary

| Feature | Description |
|--------|-------------|
| `total_deposit_usd` | Total USD value deposited into the protocol |
| `total_borrow_usd` | Total amount borrowed by the wallet |
| `repay_ratio` | Ratio of repaid amount to borrowed amount |
| `total_redeem_usd` | Assets withdrawn from protocol |
| `deposit_to_redeem_ratio` | Efficiency metric: redeems / deposits |
| `num_liquidations` | Number of times the user was liquidated |
| `cluster` | Behavior group assigned via KMeans |
| `credit_score` | Final credit score (0–1000) assigned based on scoring logic |

---

## 📈 Visual Insights

### 1. Repay Ratio vs. Credit Score

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/eb48d553-6bad-4b19-bec6-85ee0bd3a039" />





---

### 2. Score Distribution

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/f8ec51c4-4fb6-41f7-94a4-6700c4b8911e" />


---

### 3. Wallet Behaviour

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/c8def836-f1b6-417d-aa01-dd8dd3f2fdcf" />

---
### 4.Credit Score vs. Number of Liquidations

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/7ad7ebc4-64e5-4ac1-8cc0-246b822d3b21" />



## 💡 Key Observations

- **Repayment behavior** is the strongest positive indicator.
- **Frequent liquidations** significantly lower the score, even if deposits are large.
- Wallets with **no borrow-repay activity** tend to receive **moderate or low scores**, depending on their redeem patterns.
- **Clustering** helped group wallet behaviors into 5 distinct user types.

---

## ✅ Conclusion

This model offers a scalable and explainable way to assign creditworthiness to DeFi wallets, even in the absence of labeled data. It can be further improved using supervised learning if repayment success or loan default labels become available.

---

