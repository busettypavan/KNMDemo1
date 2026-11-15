# See current profit or loss per lot

Requirement: REQ-354 · Feature: See current profit or loss per lot · Decision: DEC-389
Order: 8 of 11
Depends on: Add a position lot, View a stock's daily price chart

## Purpose
Users see real, current P&L for each lot they entered (intent G2).

## Behaviour
- Each of the user's lots shows its own P&L.
- Amount = (current price − buy price) × quantity.
- Percent = (current price − buy price) ÷ buy price × 100.
- The current price is the latest usable close; its date is shown.
- Missing or stale market data shows P&L as unavailable or stale, never zero.
- There is no aggregate across lots of the same stock (Assumptions §6.2).

## Acceptance criteria
1. Amount and percent match the formulas above.
2. The price date is shown beside the P&L.
3. Missing data shows unavailable or stale, not zero.
4. Each lot shows its own P&L.

## Source documents
- docs/project/intent.md (G2, Success)
- docs/project/source/01-detailed-functional-requirements.md (§4.3)
- docs/project/source/Assumptions.md (ASM-025, ASM-026; §6.1, §6.2)

## Open questions
- What counts as "stale" (how many days old the price may be) is not defined.
- Whether percent is shown to two decimals is not defined.
