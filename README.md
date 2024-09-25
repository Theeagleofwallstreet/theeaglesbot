# Algoedgebot
# TheEagleOfWallStreet Trading Bot

### Overview

Thealgoedgebot is an automated trading bot designed to trade the XAU/USD currency pair on the 4-hour timeframe. This bot is built using MQL4 and is intended to execute trades based on specific technical patterns and conditions.

### Strategy

The bot follows a simple yet effective strategy focusing on key price levels and candlestick patterns, with specific rules for risk management. The main features of the strategy include:

- **Timeframe**: 1-hour (H1)
- **Currency Pair**: GBP/USD

#### Entry Conditions

- **Sell Orders**:
  - Triggered when the price reaches the **High of the Day (H.O.D.)**.
  - The price must form one of the following patterns:
    - **Railroad Track**
    - **M Pattern**
    - **Evening Star**
  - A **Sell** order is placed with a stop loss above the H.O.D.

- **Buy Orders**:
  - Triggered when the price reaches the **Low of the Day (L.O.D.)**.
  - The price must form one of the following patterns:
    - **Inverted Hammer**
    - **Morning Star**
    - **W Pattern**
  - A **Buy** order is placed with a stop loss below the L.O.D.

#### Risk Management

- **Stop Loss**: 
  - Placed above the H.O.D for Sell orders.
  - Placed below the L.O.D for Buy orders.
  
- **Break-Even**: 
  - Once a trade reaches 10 pips in profit, the stop loss is moved to 10 pips below the entry price for Sell orders, and 10 pips above the entry price for Buy orders.

- **Take Profit**:
  - Set to 50 pips from the entry price.

### Installation

To use this bot, follow these steps:

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/yourusername/TheEagleOfWallStreet-Bot.git
