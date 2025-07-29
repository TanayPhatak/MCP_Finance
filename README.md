# Stock Analysis MCP Server

A simple MCP (Model Context Protocol) server that provides basic stock technical analysis tools for AI assistants.

## Features

- **Moving Averages**: Calculate short and long-term moving averages
- **RSI Analysis**: Relative Strength Index calculations
- **Trade Recommendations**: Basic buy/sell/hold signals based on technical indicators

## Installation

```bash
# Clone the repository
git clone https://github.com/TanayPhatak/MCP_Finance.git

# Create a virtual environment and activate it
uv venv
.venv\Scripts\activate  # for Windows
.venv/bin/activate  # for Linux

# Install dependencies
uv sync
```

## Configuration

Create a `.env` file:

```env
ALPHA_VANTAGE_API_KEY=your_api_key_here
```

Get your free API key from [Alpha Vantage](https://www.alphavantage.co/support/#api-key).

## Usage

#### Start the server (dev):

```bash
mcp dev stock_analysis_server.py  # this will start a dev environment where you can test the tools
```

#### Integrate the MCP server with Claude Desktop:
Ensure Claude desktop is installed ([Download Link](https://claude.ai/download))

```bash
mcp install stock_analysis_server.py --with requests --with pandas --with tabulate
```

Restart Claude Desktop after running the above command.

## Tools offered

The server provides these tools:
- `calculate_moving_averages` - Get MA analysis for a stock symbol
- `calculate_rsi` - Get RSI analysis for a stock symbol  
- `trade_recommendation` - Get comprehensive buy/sell recommendation

### Example prompts with Claude

```
Analyze AAPL stock using moving averages.
Get RSI for MSFT.
What's your recommendation for Google stock?
Should I buy or sell Apple stocks?
```

## Requirements

- Python 3.9+
- Alpha Vantage API key
- UV package manager (or pip)
