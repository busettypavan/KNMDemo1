# Browse current Nifty 100 stocks

Requirement: REQ-349 · Feature: Browse current Nifty 100 stocks · Decision: DEC-384
Order: 3 of 11
Depends on: Sign in and sign out

## Purpose
Users choose which stock to analyse from a curated list (intent G5). The universe is the current Nifty 100 (user decision).

## Behaviour
- A signed-in user sees the current Nifty 100 stocks with symbol, name, price and day change.
- Search and filter by name or symbol.
- An invalid or unsupported ticker is flagged, not silently dropped (Assumptions §4.6).

## Acceptance criteria
1. The list shows every current Nifty 100 stock with symbol, name, price and day change.
2. Search matches name or symbol.
3. An invalid ticker is flagged.
4. The constituent list is kept as reference data (not hard-coded in the UI).

## Source documents
- docs/project/intent.md (G5, Not goals: full NSE universe)
- docs/project/source/01-detailed-functional-requirements.md (§3, §4.1)
- docs/project/source/Assumptions.md (§4)
- Decision from the user: current Nifty 100.

## Open questions
- The exact list of current Nifty 100 constituents is not in the documents; it must be supplied.
- Filter fields beyond name and symbol (for example sector) are not defined.
- How the list is updated when index constituents change is not defined (Assumptions §4.5).
