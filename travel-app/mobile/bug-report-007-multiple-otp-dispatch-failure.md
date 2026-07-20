# [BUG-007] Multiple Email Verification Codes Dispatched Simultaneously and Failure of Token Validation

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Registration / Verification Module
- **Type**: Bug / Authentication / Network
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: OTP verification screen

## Preconditions
The user has submitted valid registration parameters and is routed to the OTP verification screen.

## Steps to Reproduce
1. Open the application and navigate to the registration workflow.
2. Populate all mandatory text inputs and press "Confirm and Continue".
3. Check the registered email inbox and observe the received validation tokens.
4. Attempt to enter one of the delivered verification codes into the OTP input field.

## Actual Result
The system floods the user's inbox with multiple verification codes in a short timeframe. Upon submitting any of the codes, the process fails silently; the input field highlights in red with no error string provided, forcing the user to repeatedly request new tokens.

## Expected Result
Only a single unique verification code should be dispatched per request window. Upon entering the correct token, the application must successfully validate the session and complete account activation.
