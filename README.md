# MarketMind

**An autonomous AI trading agent for the stock market.** MarketMind combines machine-learning price forecasting with reinforcement-learning decision-making, and tests everything safely on Alpaca's paper-trading API, so no real money is ever at risk.

**Author:** [Sayed Jibril](https://github.com/Sayed-jibril)

> **Disclaimer:** MarketMind is an educational Computer Science project, not financial advice. It is built for **paper trading only**. Past performance in backtests does not predict real-world results.

---

## Features

- **Live market data:** real-time and historical prices pulled from Alpaca's API
- **ML-powered predictions:** trend forecasting from historical prices and technical indicators
- **Agentic RL trader:** an autonomous agent that learns when to buy, sell, or hold, using DQN and PPO
- **Backtesting and paper trading:** validate strategies on history first, then run them live against a simulated account
- **Performance dashboards:** track equity, trades, and returns with interactive charts
- **Free and open source:** runs entirely on free tools and APIs

## How It Works

```
Alpaca market data
        │
        ▼
Feature engineering (technical indicators)
        │
        ▼
ML model ──► price-trend predictions
        │
        ▼
RL agent (DQN / PPO) ──► buy / sell / hold decisions
        │
        ▼
Alpaca paper-trading account ──► dashboard (Streamlit + Plotly)
```

## Tech Stack

| Area                   | Tools                              |
| ---------------------- | ---------------------------------- |
| Language and data      | Python, Pandas, NumPy              |
| Machine learning       | Scikit-learn                       |
| Reinforcement learning | Stable-Baselines3 (DQN, PPO)       |
| Brokerage and data     | Alpaca API (paper trading)         |
| Dashboards             | Streamlit, Plotly                  |
| Training               | Google Colab (no local GPU needed) |

## Getting Started

### Prerequisites

- Python 3.9+
- A free [Alpaca](https://alpaca.markets) account with **paper-trading** API keys

### 1. Clone the repository

```bash
git clone https://github.com/Sayed-jibril/marketmind-trading-bot.git
cd marketmind-trading-bot
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Add your Alpaca keys

Create a `.env` file in the project root:

```bash
ALPACA_API_KEY=your_paper_api_key
ALPACA_SECRET_KEY=your_paper_secret_key
ALPACA_BASE_URL=https://paper-api.alpaca.markets
```

Never commit this file. Make sure `.env` is listed in your `.gitignore`.

### 4. Launch the dashboard

```bash
streamlit run app.py
```

## Training on Google Colab

No GPU? Train the RL agents on Colab's free tier, then download the saved model and load it locally for backtesting and paper trading.

## Roadmap

- [ ] Add more technical indicators and features
- [ ] Compare DQN and PPO performance side by side
- [ ] Risk management: position sizing and stop-losses
- [ ] Multi-stock portfolio support
- [ ] Trade logs and exportable performance reports

## Contributing

Ideas and improvements are welcome. Fork the repo, create a branch, and open a pull request.

## Author

**Sayed Jibril**: [github.com/Sayed-jibril](https://github.com/Sayed-jibril)

---

**MarketMind**: an agent that learns the market, one paper trade at a time.
