# wallet_credit_scorer
The project takes in transaction-level data from a blockchain protocol(Aave V2) and returns credit scores respective to user's transaction behavior.
# DeFi Wallet Credit Scoring

This project implements a **credit scoring system** for wallets based on historical transaction behavior on the **Aave V2 protocol**. The system assigns each wallet a credit score between `0` and `1000`, where higher scores indicate more reliable and responsible behavior.

## 📌 Objective

> **Develop a robust ML-based model that evaluates DeFi wallets using unsupervised learning and behavioral analysis.**

## 🧠 Features Engineered

Each wallet is evaluated based on the following features:

- `total_deposit_usd`: Total amount deposited
- `total_borrow_usd`: Total borrowed amount
- `repay_ratio`: Ratio of total repayments to total borrows
- `total_redeem_usd`: Amount of assets redeemed
- `deposit_to_redeem_ratio`: Efficiency of redeeming what was deposited
- `num_liquidations`: Number of times the wallet was liquidated

## 🔧 Methodology

1. **Data Ingestion**  
   Transactions are read from a JSON file with raw Aave V2 actions.

2. **Feature Engineering**  
   Behavioral metrics are computed per wallet (e.g., repay ratio, liquidation count).

3. **Unsupervised Learning**  
   - **Autoencoder** is used to compress wallet behavior into latent representations.
   - **KMeans clustering** groups wallets into behavioral profiles.

4. **Scoring Formula**  
   A weighted scoring formula combines key features:
   - Repay ratio (up to 500 points)
   - Liquidation penalty (up to 200 points)
   - High deposit bonus (100 points)
   - Deposit-to-redeem ratio (up to 100 points)

5. **Final Credit Score**  
   Normalized to a 0–1000 scale and output per wallet.

## 📊 Visualizations

- Distribution of credit scores
- Clustering of wallet behaviors
- Repay ratio vs. credit score scatter plots
- Wallet credit scores vs. number of liquidations

---
## 💻 Execution
Run main.pynb with the target Aave V2 protocol transaction file


