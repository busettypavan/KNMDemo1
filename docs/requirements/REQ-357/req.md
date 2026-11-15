# Show crossover buy and sell markers on the chart

Requirement: REQ-357 · Feature: Show crossover buy and sell markers on the chart · Decision: DEC-392
Order: 11 of 11
Depends on: Apply Moving Average Crossover with a chosen period

## Purpose
Users see where the crossover strategy signals on the chart (intent G3).

## Behaviour
- Buy marker: the close crosses from below to above the moving average.
- Sell marker: the close crosses from above to below the moving average.
- Markers are drawn on the chart at the dates they occurred.
- No signal table is part of this requirement (Assumptions §7.3).
- Signals are not orders and do not account for costs (Assumptions §7.3).

## Acceptance criteria
1. A buy marker appears on a day the close crosses from below to above the MA.
2. A sell marker appears on a day the close crosses from above to below the MA.
3. No marker appears where history is too short for the MA.
4. Markers are computed when viewed, not stored.

## Source documents
- docs/project/intent.md (G3, Success)
- docs/project/source/01-detailed-functional-requirements.md (§4.4, §8 open item 3)
- docs/project/source/Assumptions.md (§7.1, §7.3, §8.2)

## Open questions
- Duplicate-signal suppression while the price stays on one side of the MA is proposed but not confirmed (Assumptions §8.2 item 4).
- The first valid signal date and the handling of insufficient history are not confirmed (Assumptions §8.2 item 5).
