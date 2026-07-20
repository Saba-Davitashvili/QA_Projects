# [BUG-006] Missing Minimum Age Validation During Registration Flow

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Registration / Verification Logic
- **Type**: Bug / Business Logic Validation
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Registration screen

## Preconditions
The user is on the account creation/registration screen.

## Steps to Reproduce
1. Open the application and select the "Registration" option.
2. Fill out all required fields with valid registration data.
3. In the Date of Birth selector, input a date that corresponds to exactly one day prior to the current date (e.g., registering an infant).
4. Tap the "Confirm and Continue" button.

## Actual Result
The system accepts the invalid birthdate without executing a validation check, successfully finalizing the registration and creating the account.

## Expected Result
The system must validate the input against predefined age limits. If the user does not meet the minimum age constraint, registration must be rejected with an explicit error message: *"You do not meet the minimum age requirement to register an account."*
