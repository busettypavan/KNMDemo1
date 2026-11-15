# Create account with email and password

Requirement: REQ-347 · Feature: Create account with email and password · Decision: DEC-382
Order: 1 of 11
Depends on: none

## Purpose
Sign-in is required, so each user needs a persistent account that their positions belong to (intent G4; Assumptions ASM-009, ASM-010).

## Behaviour
- A new user enters an email address and a password and creates an account.
- Only email and password are collected (user decision). Full name and terms checkbox shown in the mock are not part of this requirement.
- The server checks the input and stores the password hashed.

## Acceptance criteria
1. An account is created with a unique email.
2. The password is stored hashed, never in plain text.
3. A duplicate email is rejected with a clear message.
4. An invalid email or a password below the minimum is rejected by the server.

## Source documents
- docs/project/intent.md (G4, Not goals)
- docs/project/source/Assumptions.md (ASM-009, ASM-010, ASM-012; §10.3)
- Decision from the user: sign-in required; email and password only.

## Open questions
- Password rules: minimum length and complexity are not defined.
- Is email verification required at sign-up? Not defined.
