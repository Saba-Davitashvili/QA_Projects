# [BUG-001] Missing UI Validation Feedback on Invalid Forgot Password Submission

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Authentication / Password Recovery
- **Type**: Bug / UI Validation
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Forgot Password screen

## Preconditions
The application is launched and the user is on the Login screen.

## Steps to Reproduce
1. Tap the **"Already have an account? Login"** action link.
2. Tap the **"Forgot Password"** link to navigate to the recovery screen.
3. In the "Email or Phone Number" field, enter an invalid value: `martivi:D`
4. Tap the **"Continue"** button.

## Actual Result
The application fails to respond. No inline validation error, toast alert, loading spinner, or field highlight is triggered. The UI remains completely static.

## Expected Result
The system should execute client-side regex validation on submit. If the input fails email/phone constraints, the UI must block submission and display a clear inline message — e.g., *"Please enter a valid email or phone number."*
