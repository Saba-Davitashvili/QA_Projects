# [BUG-009] Broken Forgot Password Workflow Navigation and Uncapped Duplicate Email Dispatch

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Account Recovery / Navigation
- **Type**: Bug / Navigation / Logic
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Forgot Password recovery interface

## Preconditions
The user is on the initial Forgot Password recovery interface.

## Steps to Reproduce
1. Input a valid, registered email address and tap the "Continue" button.
2. Once routed to the "Check your inbox" screen, tap the native or custom "Back" action button.
3. On the populated recovery input screen, tap the "Continue" button again without modifying the email string.
4. Observe the interface behavior and attempt to tap "Continue" repeatedly.

## Actual Result
A duplicate verification email is dispatched to the target account. However, the interface fails to navigate forward a second time; the screen remains stuck on the input page regardless of unlimited subsequent interactions.

## Expected Result
If an email has already been dispatched within an active session window, the "Continue" button must either be debounced/disabled or display an inline notice (e.g., *"Verification email already sent"*). Forward navigation properties must remain consistent if re-routed.
