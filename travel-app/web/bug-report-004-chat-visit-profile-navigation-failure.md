# [BUG-004] "Visit Profile" Action in Chat Menu Fails to Navigate

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Chat / Context Menu / Navigation Routing
- **Type**: Bug / Navigation Failure
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Chat section — conversation context menu

## Steps to Reproduce
1. Navigate to the **Chat** section and open any conversation.
2. Click the green button (next to the **'X'**) in the top right corner of the chat.
3. Select **"Visit Profile"** from the dropdown menu.

## Actual Result
Clicking **"Visit Profile"** produces no action. No route change is initiated, no loading state appears, and the user remains on the current chat view. The button's click handler appears to be either unbound or silently failing.

## Expected Result
The system should navigate the user to the selected chat participant's profile page immediately upon clicking **"Visit Profile."**

