# Apply Moving Average Crossover with a chosen period

Requirement: REQ-356 · Feature: Apply Moving Average Crossover with a chosen period · Decision: DEC-391
Order: 10 of 11
Depends on: View a stock's daily price chart

## Purpose
Users apply the single MVP strategy and choose its moving-average period (intent G3).

## Behaviour
- The user applies Moving Average Crossover to a stock and sets the period.
- Default period: 5 days (user decision).
- The moving average is a simple moving average (SMA), computed on the server from cached daily closes.
- Nothing is stored; the result is computed when the stock is viewed (Assumptions §7.1).

## Acceptance criteria
1. The period is configurable, with a default of 5 days.
2. The moving average is an SMA.
3. The strategy is computed on the server from cached closes.
4. No signal is stored.
5. The period must be a positive whole number.

## Source documents
- docs/project/intent.md (G3)
- docs/project/source/01-detailed-functional-requirements.md (§4.4)
- docs/project/source/Assumptions.md (ASM-005, §7.1, §7.2)
- Decision from the user: 5-day default.

## Open questions
- The allowed range for the period (minimum and maximum) is not defined.
- Whether "5 days" means 5 trading days or 5 calendar days is not defined.
- Confirm the moving-average type is SMA (Assumptions §8.2 item 1 asks for this).
