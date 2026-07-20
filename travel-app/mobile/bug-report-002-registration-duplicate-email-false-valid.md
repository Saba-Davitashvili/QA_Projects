# [BUG-002] Registration Email Field Shows Green Checkmark for Already Registered Email

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Registration Workflow
- **Type**: Bug / Validation Logic
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Registration screen

## Preconditions
The user is on the account registration screen.

## Steps to Reproduce
1. Open the application and select **"Registration"**.
2. In the Email field, enter an email address already linked to an existing active account.
3. Fill out all remaining required fields with valid data.
4. Tap **"Confirm and Continue"**.

## Actual Result
The email field keeps a green visual highlight — incorrectly signaling the address is available. When tapping "Confirm and Continue", the system silently blocks progression but shows no error message, leaving the user stuck with no feedback.

## Expected Result
An async uniqueness check should fire on the email field. If the address is already registered, the field should turn red and display: *"This email address is already in use."* Submission should be blocked until a unique email is entered.
