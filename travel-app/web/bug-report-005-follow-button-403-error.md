# [BUG-005] Follow Button Triggers 403 Forbidden Network Error on Profile Page

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Profile / Follow System / API Authorization
- **Type**: Bug / API Error
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: User profile page — Follow action

## Steps to Reproduce
1. Navigate to a specific user's profile page.
2. Click the **"Follow"** button.

## Actual Result
The system throws an error and displays: *"Network error. Please check your connection and try again. (403 error)."* The follow relationship is not created, and the button state remains unchanged.

## Expected Result
After clicking the **"Follow"** button, the API should return a success response. The button state should update to reflect the new relationship (e.g., change to *"Following"*), and the user should be added to the authenticated user's following list.

