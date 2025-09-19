# FullStack-Crypto-Trading-Platform-JAVA-_SPRINGBOOT-COINHUB

# 🪙 Crypto Trading Platform (COINHUB)

A full-stack **Crypto Trading Web Application** developed using:

- **Frontend:** React.js, ShadCN UI, Tailwind CSS
- **Backend:** Spring Boot (Java), Maven
- **Database:** MySQL
- **API Integration:** CoinGecko API (free tier)
- **Deployment:** Frontend :- Vercel || Backend :-Railway
                   

---

## 🚀 Live Demo

👉 [LIVE LINK](#)  
[(https://coin-hub-frontend-3czr.vercel.app/)]

---

## 📸 Screenshots

### Dashboard
![dashboard](https://github.com/user-attachments/assets/83659ef6-4c76-4430-ab3d-84a44d3acb4d)
###SignUp
![signup](https://github.com/user-attachments/assets/0d8e09a8-540e-4bfa-a42a-bfc23c3bcee1)
### SignIn
![signin](https://github.com/user-attachments/assets/5561195d-a942-47e7-be34-74b923bfe1dc)
### Watchlist
![watchlist](https://github.com/user-attachments/assets/69993806-981e-4983-aa7d-777f4ab1e2a2)
### Wallet
![wallet](https://github.com/user-attachments/assets/b84209d5-b253-4514-b366-58942a23f4d0)
### Sell
![sell](https://github.com/user-attachments/assets/fb0671a6-e1c3-42b6-af50-e044ef4c0199)
### Buy
![buy](https://github.com/user-attachments/assets/7535dd78-ecc3-4e9d-957d-a20a1af8369f)
### Withdrawal
![withdrawal history](https://github.com/user-attachments/assets/d579c6ae-b264-486c-84e0-dc3381ccff39)
### Prediction chart
![prediction chart](https://github.com/user-attachments/assets/11a19fcb-064a-47ad-b987-81772c0f8059)
### Profile
![profile](https://github.com/user-attachments/assets/839d3b8d-eeb1-4de4-86ff-cba6fae5cdce)
### Activity
![activity](https://github.com/user-attachments/assets/e7de362f-d48e-4597-9c2c-ffb81df2f764)
### Prediction
![predictor 1](https://github.com/user-attachments/assets/e880096e-5b03-4e96-aedb-5d9f79ccdb9e)

![predictor 2](https://github.com/user-attachments/assets/38b68879-1b58-4303-8b8c-bd800deac4a3)


## ✨ Features

### 🏠 Dashboard

- Shows all crypto coins with real-time price updates.
- Displays **Top 50 coins**, **Top Gainers**, and **Top Losers**.
- Sponsor coin chart displayed on homepage for quick market glance.

### 📈 Coin Details & Trading

- Clicking on any coin opens full price chart.
- Buy/Sell functionality integrated with user wallet balance.
- Future Price Prediction feature (experimental & for insights only) using **CoinGecko API** and basic JavaScript prediction model.

### 💰 Wallet System

- Add money to wallet.
- Withdraw money from wallet.
- Transfer money from wallet-to-wallet between users.
- View withdrawal history (currently supporting Bank Withdrawals only).

### 🔔 Watchlist & Activity

- Users can maintain personal watchlists for favorite coins.
- Activity section logs user trading actions.

### 🔐 Authentication

- User **Signup/Signin** interface.
- Secure login system.

### 💳 Payment Details

- Users can save their payment details for faster transactions.

---

## ⚙️ Technologies Used

| Tech | Purpose |
| ---- | ------- |
| **React.js** | Frontend |
| **Tailwind CSS + ShadCN UI** | Styling & UI components |
| **Spring Boot (Java)** | Backend REST API |
| **Maven** | Java project management |
| **MySQL** | Relational Database |
| **CoinGecko API** | Crypto data fetching |
| **HTML/CSS/JS** | Frontend logic for price prediction |

---
📘 Entity-Relationship Diagram: Crypto Trading Platform
👤 User
id (PK)

email

password

is_email_verified

created_at

updated_at

🔐 Verification Code
id (PK)

user_id (FK)

code

created_at

🔑 Forgot Password Token
id (PK)

user_id (FK)

token

created_at

🔒 Two-Factor Auth
id (PK)

user_id (FK)

secret_key

recovery_codes

created_at

🪙 Coin
id (PK)

name

symbol

image

change_percentage_1h

change_percentage_24h

change_percentage_7d

current_price

market_cap

market_cap_rank

total_volume

high_24h

low_24h

price_change_24h

price_change_percentage_24h

circulating_supply

total_supply

max_supply

ath

ath_change_percentage

ath_date

atl

atl_change_percentage

atl_date

last_updated

💼 Wallet
id (PK)

user_id (FK)

created_at

updated_at

💰 Wallet Coin
id (PK)

wallet_id (FK)

coin_id (FK)

amount

created_at

updated_at

📌 Watchlist
id (PK)

user_id (FK)

created_at

updated_at

📌 Watchlist Coin
id (PK)

watchlist_id (FK)

coin_id (FK)

created_at

updated_at

📦 Orders
id (PK)

user_id (FK)

type

status

created_at

updated_at

📦 Order Item
id (PK)

order_id (FK)

coin_id (FK)

amount

price

created_at

updated_at

💳 Payment Order
id (PK)

order_id (FK)

payment_method

status

created_at

updated_at

💳 Payment Details
id (PK)

payment_order_id (FK)

card_number

card_holder

expiry_date

cvv

created_at

updated_at

📊 Asset
id (PK)

user_id (FK)

coin_id (FK)

amount

created_at

updated_at

🔄 Wallet Transaction
id (PK)

wallet_id (FK)

coin_id (FK)

amount

transaction_type

created_at

updated_at

🔁 Transaction
id (PK)

sender_wallet_id (FK)

receiver_wallet_id (FK)

coin_id (FK)

amount

created_at

updated_at
