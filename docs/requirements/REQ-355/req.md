# Delete a position lot

Requirement: REQ-355 · Feature: Delete a position lot · Decision: DEC-390
Order: 9 of 11
Depends on: Add a position lot

## Purpose
Users can remove a lot they entered by mistake or no longer hold (Assumptions §6.2).

## Behaviour
- A signed-in user deletes one of their own lots.
- The server refuses to delete a lot owned by another user.
- Editing lots is not part of this requirement (user decision).

## Acceptance criteria
1. A deleted lot no longer appears in the user's lots.
2. The server refuses to delete another user's lot.
3. No edit action is provided.

## Source documents
- docs/project/source/Assumptions.md (§6.2, §2 security baseline)
- docs/project/source/Assumptions.md (DEC-005 proposes editing; the user has decided no editing for now)

## Open questions
- Should the user confirm before deletion? Not defined.
