# kraken-bot candles

Public market data only: closed BTC and altcoin candles, refreshed every hour (about :03-:05 UTC) by the kraken-bot server.

- `candles/KRAKEN_BTCUSD_<1h|4h|1D>.json`: Kraken spot XBTUSD (= TradingView KRAKEN:BTCUSD)
- `candles/BINANCE_<COIN>USDT_<1h|4h|1D>.json`: Binance spot, 21 coins
- `candles/index.json`: every file, its bars, its last closed bar, and whether this hour's read worked

Format (TradingView "columns"): {symbol, interval, source, updatedAt, t, o, h, l, c, v}; t = bar open in unix seconds, oldest first, closed bars only. A file that failed to refresh keeps its last good copy and its older updatedAt.

No account data, balances, positions, orders or keys are ever written here.
