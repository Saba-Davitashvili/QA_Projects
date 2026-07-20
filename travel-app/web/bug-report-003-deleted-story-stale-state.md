# [BUG-003] Deleted Story Remains Visible Until Manual Page Refresh

## Metadata
- **Project**: — Social Travel & Booking Platform
- **Component**: Stories / Client-Side State Synchronization
- **Type**: Bug / State Management
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Home page — Stories section

## Preconditions
User is on the home page.

## Steps to Reproduce
1. Upload any story.
2. Delete the newly uploaded story.

## Actual Result
After deletion, the story remains visible in the interface. The Delete button becomes unresponsive on subsequent clicks. The stale story persists until the user manually triggers a full page refresh. No success or confirmation message is displayed.

## Expected Result
The story should be immediately removed from the DOM upon successful deletion. A confirmation message should appear (e.g., *"Story successfully deleted"*), and the stories feed should reactively update without requiring a manual refresh.

