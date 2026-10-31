# Risk Policy

## Current status

The project is strictly paper-only. No broker connection, live execution, real account, or real-money order functionality is permitted.

## Future simulation limits

These limits apply only to a future paper simulator and are not a recommendation to trade:
- Maximum simulated risk per trade: 0.25% of simulated equity.
- Maximum daily simulated loss: 1%.
- Maximum concurrent simulated positions: 1.
- Every simulated position must have a defined stop-loss.
- Martingale and grid strategies are prohibited.

## Enforcement

AMAN must implement deterministic checks independent of language models and strategy agents. A failed or unavailable risk check means reject the simulated action. AI components cannot override the risk authority.

## Research quality

Any backtest must model transaction costs and disclose assumptions for spread, commissions, slippage, latency, rejected fills, and missing data. Track drawdown and out-of-sample performance. Do not optimize and report results on the same data without disclosure.

## Legal and financial caution

This software is educational research infrastructure, not financial advice. No live funding or trading should be considered without independent legal, regulatory, broker, and operational review.
