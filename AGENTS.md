# OPEN TRADE AI — Project Rules

## Mission
Build an open-source Forex research and paper-trading system.

## Architecture
Use modular Python architecture with independent components:
- ASAD: coordinator
- XOG: market analyst
- HILAAC: strategy researcher
- QUANT CORE: deterministic calculations
- AMAN: deterministic risk authority
- FALCON: paper execution simulator only

Use external projects as architectural references only. Do not copy source code without an explicit license review.

## Absolute safety policy
**PAPER-ONLY DEVELOPMENT.**

Never implement:
- Live broker connections or broker authentication.
- Real-money order placement or execution.
- Live trading switches or live-account switching.
- Broker credential storage.
- Hidden live-execution fallbacks.

Do not install MetaTrader5, broker SDKs, CCXT, or trading execution packages.

Initial market data must come from local CSV fixtures or deterministic synthetic data. Do not add live market access in the first milestone.

## First milestone
Implement:
1. Typed OHLCV market data model.
2. CSV ingestion.
3. Timestamp and candle validation.
4. EMA, RSI, and ATR indicators.
5. M5 trend and M1 signal analysis.
6. Deterministic tests.
7. Signal reporting only.

Signals are observations, not orders. Do not implement order execution in this milestone.

## Engineering requirements
- Python 3.12.
- Type hints and clear docstrings.
- Pytest coverage.
- Ruff formatting and linting.
- No look-ahead bias.
- Explicit timezone handling; normalize timestamps to UTC.
- Reproducible calculations.
- No fabricated profitability claims.

## Future simulated risk policy
The future paper system must enforce:
- 0.25% maximum simulated account risk per trade.
- 1% daily simulated loss limit.
- One maximum open simulated position.
- Mandatory simulated stop-loss.
- No martingale.
- No grid trading.

Risk validation must be deterministic and independent of AI agents. AI agents cannot override AMAN.

## Development workflow
Before changing files:
1. Inspect the existing repository.
2. Explain the proposed implementation.
3. Identify security implications.

After changing files:
1. Run tests.
2. Run Ruff.
3. Report changed files.
4. Report test results.
5. Explain remaining limitations.

Never remove safety restrictions to make tests pass.
