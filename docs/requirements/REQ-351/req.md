# Overlay trend and volatility indicators on the chart

Requirement: REQ-351 · Feature: Overlay trend and volatility indicators on the chart · Decision: DEC-386
Order: 5 of 11
Depends on: View a stock's daily price chart

## Purpose
Users analyse trend and volatility with indicator overlays on the price chart (intent G1). VWAP is skipped for now (user decision).

## Behaviour
- The user turns on or off: SMA, EMA, Bollinger Bands, Parabolic SAR.
- Indicators are computed on the server from cached daily history.
- Indicators are visual only; they never generate buy or sell signals (Assumptions §5.1).

## Acceptance criteria
1. Each indicator toggles independently.
2. Values are computed on the server from cached history.
3. Where history is too short, the value is shown as unavailable, not fabricated.
4. Documented, standard parameter defaults are used.

## Source documents
- docs/project/intent.md (G1)
- docs/project/source/01-detailed-functional-requirements.md (§4.2)
- docs/project/source/Assumptions.md (§5, §5.1)
- Decision from the user: VWAP skipped for now.

## Open questions
- Default periods for SMA, EMA, Bollinger Bands and Parabolic SAR are not stated, only "standard"; confirm the values.
- Whether the SMA and EMA periods are user-configurable is not defined (Assumptions §5 says "where supported").
