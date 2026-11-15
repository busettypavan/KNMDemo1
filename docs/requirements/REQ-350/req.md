# View a stock's daily price chart

Requirement: REQ-350 · Feature: View a stock's daily price chart · Decision: DEC-385
Order: 4 of 11
Depends on: Browse current Nifty 100 stocks

## Purpose
Users analyse a stock on its daily price chart (intent G1), using end-of-day data only.

## Behaviour
- Opening a stock shows its daily candlestick chart with volume.
- Daily data is fetched on first view and refreshed at most once per IST day (Assumptions ASM-017, ASM-018, ASM-021).
- The price date and the last successful refresh time are shown. The chart is not presented as a live quote.
- If data is unavailable, an error or stale-data warning is shown; no price is invented.
- A failed refresh keeps the last valid cached data (ASM-020).

## Acceptance criteria
1. The chart shows daily candles and volume.
2. The price date and last refresh time are visible.
3. Data is fetched once per IST day, on first view.
4. Unavailable data shows a clear error or stale warning, with no invented price.
5. A failed refresh keeps the last valid cached data.

## Source documents
- docs/project/intent.md (G1, Success)
- docs/project/source/01-detailed-functional-requirements.md (§4.1, §6)
- docs/project/source/Assumptions.md (§3, §3.1, §8.7, §10.2)

## Open questions
- Performance targets for chart load are not defined (DEC-008).
- The charting library is not chosen (Assumptions §8.8, §9).
