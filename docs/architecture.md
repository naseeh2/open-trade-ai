# Architecture

## Research pipeline

Local market data → validation → QUANT CORE features → agent research and challenge → deterministic AMAN policy checks → paper simulation (future) → performance evaluation.

## Components

| Component | Responsibility | Authority |
|---|---|---|
| ASAD | Coordinate research workflow | Cannot override risk rules |
| XOG | Describe market structure and trend | Analysis only |
| HILAAC | Research and challenge strategy hypotheses | Analysis only |
| QUANT CORE | Calculate indicators and quantitative features | Deterministic calculations |
| AMAN | Enforce hard simulated risk constraints | Independent veto authority |
| FALCON | Simulate hypothetical fills and positions | Paper-only; no broker connectivity |

LLMs are not deterministic controls. AI outputs must be treated as fallible research inputs and validated by code.

## Initial strategy hypothesis

Explore EMA 50/200 trend context, RSI 14, and ATR 14. Use M5 for trend context and M1 for confirmation. The first milestone emits only `BUY_CANDIDATE`, `SELL_CANDIDATE`, or `NO_SIGNAL`.

The hypothesis is not a validated strategy. Require out-of-sample and walk-forward evaluation before making claims about performance.

## Data integrity

- Normalize timestamps to UTC.
- Reject malformed OHLC candles and duplicate timestamps.
- Define missing-candle handling explicitly.
- Use only data available at the signal timestamp.
- Keep synthetic fixtures clearly labelled as synthetic.
