# [BUG-006] Followers and Following Buttons Unresponsive on Profile Page

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Profile / Social Graph / UI Event Binding
- **Type**: Bug / Functional Failure
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Profile page — Followers / Following counters

## Steps to Reproduce
1. Navigate to the **Profile** page.
2. Click the **"Followers"** button/number.
3. Click the **"Following"** button/number.

## Actual Result
The system does not react to clicks on either element. No modal window, dropdown, or list view opens. The interface remains completely unchanged — no loading indicator, no error, and no navigation event is triggered.

## Expected Result
Clicking either button should open a corresponding modal window or navigate to a list page displaying the full roster of followers or following users, respectively.

