 Wallet Risk Scoring from Scratch

Overview
This project fetches on-chain transaction data for 100+ Ethereum wallets and assigns a risk score from 0 to 1000 based on simple behavioral features.
 Data Collection Method
Transaction data was pulled using the Etherscan API. For each wallet, we retrieved normal transactions with value, gas, and error status.

 Features Used
- Total number of transactions
- Total ETH sent
- Average gas price

Scoring Logic
A rule-based scoring system subtracts weighted penalties from a base score of 1000 based on:
- Transaction volume
- ETH activity
- Gas usage

Final scores are clamped to the [0, 1000] range.

 Output
The final scores are available in `wallet_scores.csv`, with two columns:
- `wallet_id`
- `score`

 Dependencies
- pandas
- requests
- tqdm
