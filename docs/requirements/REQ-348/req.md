# Sign in and sign out

Requirement: REQ-348 · Feature: Sign in and sign out · Decision: DEC-383
Order: 2 of 11
Depends on: Create account with email and password

## Purpose
Users must be identified to keep and see only their own positions (intent G4; Assumptions ASM-011).

## Behaviour
- A user signs in with email and password. Correct credentials start a session.
- Wrong credentials are refused with one generic message.
- Signing out ends the session.
- Pages and data that need a user are unavailable without a session.

## Acceptance criteria
1. Correct credentials start a session.
2. Wrong credentials are rejected with a generic message.
3. Sign-out ends the session.
4. Protected data cannot be read without a session, enforced on the server.

## Source documents
- docs/project/intent.md (G4)
- docs/project/source/Assumptions.md (ASM-011, ASM-012, security baseline in §2)
- Decision from the user: sign-in required.

## Open questions
- Session length and "remember me" are not defined (the mock shows "remember me for 30 days").
- Password reset ("Forgot password?" in the mock) is not defined.
