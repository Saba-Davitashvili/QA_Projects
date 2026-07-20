# [BUG-027] Connect Button Unresponsive in Gardener List for Guest-Created Requests

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Customer Booking / Session Lifecycle
- **Type**: Bug / Functional
- **Severity**: Critical
- **Priority**: Critical
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Chrome 148)
- **App Context**: Gardener Selection List

## Preconditions
User created a service request in guest mode and then authenticated.

## Steps to Reproduce
1. Access the application as a guest.
2. Request a service and complete steps 1-5.
3. Proceed with the login/registration prompt.
4. Click the "Connect" button under a gardener's card.

## Actual Result
The button is completely unresponsive; contact cannot be initiated with the gardener.

## Expected Result
The "Connect" button should successfully initiate a contact request and chat session with the selected gardener.
