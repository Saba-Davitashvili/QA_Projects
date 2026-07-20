# [BUG-012] Missing Navigation Header Elements and UI Deadlock in Group Chat Interface

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Group Chat Interface
- **Type**: Bug / Navigation Deadlock
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Group Chat Room View

## Preconditions
The user is logged in and has an active group messaging thread available.

## Steps to Reproduce
1. From the Home screen, tap the global "Chat" tab icon.
2. Select and enter an active Group Chat room from the thread index.
3. Attempt to locate a return navigation mechanism, then tap the ellipsis context menu button (three dots) situated in the upper right-hand corner.

## Actual Result
There is no "Back" button rendered on the view hierarchy. Tapping the ellipsis menu button generates zero response or overlay expansion. The user is entirely trapped on the active conversation screen, with the only exit path being a forced application termination.

## Expected Result
A standard navigation bar must persist at the top of the interface featuring an operational "Back" button that returns the user to the chat channel directory. The context menu button must execute cleanly on tap to reveal group configurations.
