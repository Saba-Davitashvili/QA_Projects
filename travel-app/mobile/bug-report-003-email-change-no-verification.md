# [BUG-003] Email Change Permitted Without Verification and Allows Linking an Existing User's Email

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: User Profile / Security Logic
- **Type**: Bug / Security Vulnerability
- **Severity**: Critical
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Profile Settings -> Contact Info

## Preconditions
The user is securely authenticated and logged into their active profile.

## Steps to Reproduce
1. Open the application and navigate to the Profile / Contact Info settings page.
2. Select the option to update or change the current email address.
3. Enter an email address that is already registered and verified under a completely different active user account.
4. Tap the action button to confirm and save the change.

## Actual Result
The application accepts the change instantly. The system binds the duplicate email address to the current profile without generating an email verification request or throwing a conflict exception.

## Expected Result
The backend must cross-reference records and explicitly block updates if the email is already in use (e.g., *"This email address is already assigned to another account"*). Furthermore, any email update must trigger a verification token to the new destination before the profile modification is finalized.
