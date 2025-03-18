# Crypto Trading Bot

A powerful, modular cryptocurrency trading bot supporting multiple exchanges and trading strategies.

## Features

- 🚀 **Multi-Exchange Support**: Compatible with major exchanges like Binance, Coinbase Pro, and Bybit
- 📊 **Multiple Trading Strategies**: Includes popular strategies like Grid Trading, DCA, and Technical Analysis based
- 🔔 **Real-time Notifications**: Get alerts via Telegram for trades and market movements
- 📈 **Data Visualization**: Track your performance with interactive dashboards
- 🔒 **Secure**: Your API keys stay on your own machine
- ⚙️ **Customizable**: Easy configuration for risk management and strategy parameters

## Quick Start

### Prerequisites

- Python 3.9+
- pip (Python package manager)
- API keys from your preferred exchange

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/trading_bot.git
cd trading_bot

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up configuration
cp config.example.json config.json
# Edit config.json with your API keys and preferences

# Run the bot
python src/main.py
```

## Configuration

Edit the `config.json` file to customize your trading bot:

```json
{
  "exchange": {
    "name": "binance",
    "api_key": "YOUR_API_KEY",
    "api_secret": "YOUR_API_SECRET",
    "testnet": true
  },
  "trading": {
    "strategy": "grid",
    "pairs": ["BTC/USDT", "ETH/USDT"],
    "investment_per_pair": 100,
    "max_open_trades": 5
  },
  "risk_management": {
    "stop_loss_percentage": 5,
    "take_profit_percentage": 10,
    "max_daily_loss": 50
  },
  "notifications": {
    "telegram": {
      "enabled": true,
      "bot_token": "YOUR_TELEGRAM_BOT_TOKEN",
      "chat_id": "YOUR_TELEGRAM_CHAT_ID"
    }
  }
}
```

## Supported Strategies

### Grid Trading

Automatically buys at lower prices and sells at higher prices within a predefined range.

### DCA (Dollar Cost Averaging)

Automatically invests a fixed amount at regular intervals, regardless of price.

### Technical Analysis

Uses technical indicators (RSI, MACD, etc.) to make trading decisions.

## Project Structure

```
trading_bot/
├── src/
│   ├── exchanges/        # Exchange connectors
│   ├── strategies/       # Trading strategies
│   ├── models/           # Data models
│   ├── utils/            # Utility functions
│   ├── notification/     # Notification services
│   ├── data/             # Data handling
│   └── main.py           # Entry point
├── tests/                # Unit and integration tests
├── config.example.json   # Example configuration
├── config.json           # Your configuration (gitignored)
├── requirements.txt      # Python dependencies
└── README.md             # This file
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This software is for educational purposes only. Do not risk money which you are afraid to lose. USE THE SOFTWARE AT YOUR OWN RISK. THE AUTHORS AND ALL AFFILIATES ASSUME NO RESPONSIBILITY FOR YOUR TRADING RESULTS.