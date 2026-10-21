# NEXUS TERMINAL — Starter Build 0.1.0

A local, hacker-style crypto trading terminal prototype. This first build includes a working UI, illustrative candlestick chart, watchlist, paper order ticket, simulated positions/P&L, basic demo signal panel, activity log, and local demo persistence.

## Run now (Windows)

1. Extract the `NexusTerminal` folder.
2. Open `web/index.html` in Microsoft Edge or Chrome.
3. Keep in mind: this is a local UI prototype. It does not connect to Delta Exchange and does not send real orders.

For best rendering, run from a local static server if desired:

```powershell
cd .\web
py -m http.server 8080
```

Then open `http://localhost:8080`.

## Current status

- Implemented: cyberpunk terminal UI, simulated BTC/ETH/SOL/BNB watchlist, canvas candlestick chart, timeframes UI, paper order ticket, simple margin/risk estimates, paper positions, P&L, close positions, activity log, demo reset, responsive layout.
- Not implemented: live Delta market data, authenticated account balances, real order execution, reliable AI model integration, production-grade risk controls, backtesting, or options Greeks.
- All prices, chart candles, and signal outputs are simulated. Do not use them to trade.

## Planned desktop shell

`desktop/Nexus.Desktop` is reserved for the Windows WPF/WebView2 shell. The next implementation stage should add the .NET 8 WPF host, then move exchange connectivity and risk logic into separate C# services. Start with Delta read-only credentials and official API documentation: https://docs.delta.exchange/.

## Safety

Never put Delta API secrets into browser JavaScript. Keep demo and live environments separate, start with read-only access, and require explicit confirmation and server-side risk validation before any live order can be sent.
