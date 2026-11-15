# View momentum and volume indicator panels

Requirement: REQ-352 · Feature: View momentum and volume indicator panels · Decision: DEC-387
Order: 6 of 11
Depends on: Overlay trend and volatility indicators on the chart

## Purpose
Users analyse momentum and volume with indicator panels under the chart (intent G1). VWAP is skipped for now (user decision).

## Behaviour
- The user turns on or off: RSI, MACD, Stochastic, ATR, OBV.
- Each panel is drawn under the price chart on the same dates.
- Values are computed on the server from cached history.
- Indicators are visual only; they never generate buy or sell signals.

## Acceptance criteria
1. Each panel toggles independently.
2. Panels align with the price chart dates.
3. Where history is too short, the value is shown as unavailable.
4. Indicators never produce buy or sell signals.

## Source documents
- docs/project/intent.md (G1)
- docs/project/source/01-detailed-functional-requirements.md (§4.2)
- docs/project/source/Assumptions.md (§5, §5.1)
- Decision from the user: VWAP skipped for now.

## Open questions
- Default periods for RSI, MACD (fast, slow, signal), Stochastic and ATR are not stated; confirm the values.
- Panel layout and height are not defined (Assumptions §8.10 leaves styling open).
