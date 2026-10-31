# OPEN TRADE AI

An open-source Forex research and paper-trading project combining quantitative analysis, multi-agent research, and deterministic risk controls.

> **Safety status: PAPER-ONLY.** This repository is for offline research and simulated trading development. It does not connect to brokers or place real-money trades.

## Initial research scope

- Instrument: EUR/USD
- Primary analysis timeframe: M5
- Confirmation timeframe: M1
- Initial hypothesis: EMA trend-pullback, with RSI and ATR context
- Initial signals: `BUY_CANDIDATE`, `SELL_CANDIDATE`, `NO_SIGNAL`

These are research labels, not trade instructions or executable orders. No strategy is assumed profitable.

## Architecture

- **ASAD** — workflow coordinator
- **XOG** — market structure and trend analyst
- **HILAAC** — strategy researcher and challenger
- **QUANT CORE** — deterministic indicators and feature calculations
- **AMAN** — independent deterministic risk authority
- **FALCON** — future paper-execution simulator only

See [docs/architecture.md](docs/architecture.md), [docs/risk_policy.md](docs/risk_policy.md), and [docs/development_roadmap.md](docs/development_roadmap.md).

## Development

Python 3.12 is the target runtime.

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -e ".[dev]"
pytest
ruff check .
ruff format --check .
```

The first milestone uses local CSV fixtures and deterministic synthetic data only. No live market feed, broker SDK, broker credentials, or order execution is part of the initial implementation.

## Important limitations

Backtests and paper results do not guarantee future performance. Any evaluation must account for spread, commission, slippage, latency assumptions, data quality, overfitting, and changing market regimes. Do not interpret screenshots or isolated winning periods as evidence of a durable edge.

## License

Apache License 2.0. See [LICENSE](LICENSE).
