# Add a position lot

Requirement: REQ-353 · Feature: Add a position lot · Decision: DEC-388
Order: 7 of 11
Depends on: Sign in and sign out, Browse current Nifty 100 stocks

## Purpose
Users record their own purchases manually so that P&L can be shown (intent G2).

## Behaviour
- A signed-in user adds a lot with stock, quantity, buy price and buy date.
- Each entry is saved as its own lot; lots are never averaged (Assumptions ASM-022).
- The server validates the input and sets the owner to the signed-in user.

## Acceptance criteria
1. The lot stores stock, quantity, buy price, buy date and the owning user.
2. Quantity and buy price must be positive.
3. Buy date must not be after today (IST).
4. Each entry is its own lot.
5. The server enforces all of the above.

## Source documents
- docs/project/intent.md (G2)
- docs/project/source/01-detailed-functional-requirements.md (§3, §4.3)
- docs/project/source/Assumptions.md (ASM-006, ASM-022, ASM-023, ASM-028; §6.2)

## Open questions
- The earliest allowed buy date is not defined.
- Whether the buy date may fall on a non-trading day is not defined.
