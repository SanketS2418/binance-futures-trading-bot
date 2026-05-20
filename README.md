#  Trading Bot — Binance Futures Testnet

Simple Python trading bot for Binance Futures Testnet.



---

## Features

- Place **Market** and **Limit** orders via CLI or web UI
- Support for both **BUY** and **SELL** sides
- **Live web dashboard** at `http://localhost:5050` or with:
  - Real-time price tickers (auto-refresh every 4s)
  - Account balance & PnL display
  - Open orders list with one-click cancel
  - Activity log
- Structured logging to `logs/trading_bot.log`
- Full input validation and error handling
- Clean layered architecture (CLI / API / logic / client)

---


---

## Setup

### 1. Get Testnet API Keys

1. Go to [https://testnet.binancefuture.com](https://testnet.binancefuture.com)
2. Register / log in
3. Navigate to **API Management** → **Create API Key**
4. Copy your **API Key** and **Secret Key**

### 2. Install


1. cd trading-bot

2. python -m venv venv
venv\Scripts\activate      

3. pip install -r requirements.txt
```
bash
```
### 3.  Configure credentials

1. As the .env is named as .env.example "Rename" it to .env then  fill up the details`
2. Open `.env` and fill in your keys:

```
BINANCE_API_KEY= API key for Binanace 
BINANCE_API_SECRET=API secret for Binance
```



---

## Usage

### Option A — Web Dashboard (recommended)

```bash
Run - python app.py
```

Open **[http://localhost:5050](http://localhost:5050)** or `http://127.0.0.1:5050` or `http://10.131.252.102:5050`in your browser.

You'll see a live dashboard where you can place orders, view your balance, and manage open orders — all with real testnet data.

---

### Option B — CLI

```bash
# Market order
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.01

# Limit order
python cli.py --symbol ETHUSDT --side SELL --type LIMIT --quantity 0.1 --price 3000
```

### Option C - Added Interactive Mode(Bonus - Enhanced CLI UX)
python cli.py

For Example:
Symbol: BTCUSDT
Side: BUY
Type: MARKET
Quantity: 0.01

Press Enter.


#### All CLI arguments

| Argument     | Required        | Description                          |
|-------------|-----------------|--------------------------------------|
| `--symbol`  | Yes             | Trading pair e.g. `BTCUSDT`          |
| `--side`    | Yes             | `BUY` or `SELL`                      |
| `--type`    | Yes             | `MARKET` or `LIMIT`                  |
| `--quantity`| Yes             | Order quantity                       |
| `--price`   | LIMIT only      | Limit price in USDT                  |

#### Supported symbols
`BTCUSDT` · `ETHUSDT` · `BNBUSDT` · `SOLUSDT` · `XRPUSDT`

---

#

## Logging

All activity is logged to `logs/trading_bot.log`:




## Requirements

- Python 3.9+
- Binance Futures Testnet account

```
requests
python-dotenv
flask
flask-cors
```

---

