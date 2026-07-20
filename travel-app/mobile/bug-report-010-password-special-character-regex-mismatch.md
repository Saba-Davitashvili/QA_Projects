# [BUG-010] Input Character Filtering Discrepancy and Insufficient Password Requirement Hints

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Registration / Password Input Validation
- **Type**: Bug / UI Validation / UX
- **Severity**: Low
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Registration screen

## Preconditions
The user is viewing the registration page with the real-time dynamic password strength requirements visible.

## Steps to Reproduce
1. Navigate to the account creation or registration screen.
2. Focus on the Password input field.
3. Enter a character string that integrates special symbols such as `_`, `€`, `£`, `¥`, `•`, or `‘`.
4. Review the status of the "Symbol" bullet requirement checklist indicator.

## Actual Result
The dynamic "Symbol" requirement line item remains highlighted in red (failed state) despite the presence of special characters in the text input box.

## Expected Result
The regex validation engine should recognize all standard standard keyboard symbols. If business logic deliberately restricts acceptable characters, the requirement text must be updated explicitly to inform the user exactly which symbols are approved (e.g., *"Must include a special character from the following list: !@#$%&*"*).
