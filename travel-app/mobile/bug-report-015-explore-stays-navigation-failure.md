# [BUG-015] Navigation Failure on Explore Stays Call-to-Action Inside Booking Component

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Booking Component / Navigation
- **Type**: Bug / Navigation / Routing
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Booking Module -> Stays section

## Preconditions
The application is running and the user is authenticated.

## Steps to Reproduce
1. Open the primary navigation menu and select the Booking module.
2. Tap on the secondary Stays subsection filter.
3. Locate and tap the "Explore stays" call-to-action button element.

## Actual Result
The application interface fails to capture or redirect the event layout. The screen state remains frozen on the initial prompt, showing no feedback or component loading cycles.

## Expected Result
Tapping "Explore stays" must execute a routing transition that pushes the comprehensive catalog list or detailed landing view for available hospitality listings onto the active navigation stack.
