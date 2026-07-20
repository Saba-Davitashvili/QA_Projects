# [BUG-005] Unhandled Technical Error Code Displayed on UI During Invalid Password Login Attempts

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Authentication Component
- **Type**: Bug / UX / Error Handling
- **Severity**: Low
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Login Screen

## Preconditions
The application is launched and the user is on the Login screen.

## Steps to Reproduce
1. Open the application and go to the Login screen.
2. Enter a valid registered email address.
3. Enter an incorrect password, then tap the "Confirm" button.

## Actual Result
The system surfaces a native alert containing development-level error codes: `"Login failed. The operation couldn't be completed. (RequestError error 10.)"`.

## Expected Result
The interface must gracefully parse the 401/403 HTTP code from the server and display a refined user-facing notification: *"Incorrect email or password. Please try again."*
