# Development Roadmap

## Milestone 01 — Offline market-data foundation
- OHLCV model and CSV loader
- UTC and candle validation
- EMA 50/200, RSI 14, ATR 14
- M5 trend context and M1 candidate-signal analysis
- Synthetic fixtures and deterministic tests
- Signal report only; no orders

## Milestone 02 — Backtesting research lab
- Event-driven historical simulation
- Explicit spread, commission, and slippage assumptions
- No look-ahead bias or survivorship-style data leakage
- Trade ledger and reproducible experiment configuration
- In-sample, validation, and out-of-sample separation

## Milestone 03 — Agent research layer
- ASAD workflow coordination
- XOG market-structure reports
- HILAAC strategy critique and experiment proposals
- Structured outputs with evidence and uncertainty
- AMAN remains deterministic and independent

## Milestone 04 — Paper simulation
- FALCON simulated order and position lifecycle
- Fill, spread, slippage, and rejection simulation
- Persistent journal and duplicate-action protection
- Kill switch and data-health checks
- No broker connectivity or real execution

## Milestone 05 — Performance intelligence
- Profit factor, expectancy, drawdown, Sharpe, and trade-count reporting
- Regime and robustness analysis
- Walk-forward evaluation
- Compare proposed changes against a frozen baseline

## Milestone 06 — Independent readiness review
- Security and dependency review
- Operational failure analysis
- Legal and regulatory review
- Independent validation of all risk controls

Passing a milestone does not imply that the strategy is profitable or suitable for live trading.
