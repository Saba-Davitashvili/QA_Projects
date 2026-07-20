# [BUG-018] Image View Thread Lock and UI Navigation Freeze on Chat Attachment Interactivity

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Chat Subsystem / Media Viewer
- **Type**: Bug / Performance / UI Lockup
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Chat Room -> Fullscreen Lightbox View

## Preconditions
The user is engaged in an active messaging room where an image file has been received from an external user profile.

## Steps to Reproduce
1. Open the target chat stream containing an inbound image asset.
2. Note the placeholder preview box state, then tap directly on the message bubble container to open the full-screen lightbox window view.
3. Attempt to close the modal presentation layout or swipe backward to exit the chat workspace.

## Actual Result
The image canvas displays a completely blank box signature in both views. The asset only updates and presents correctly if the application is killed from background tasks and cold-booted back into memory. If the user hits the blank asset frame without terminating the application process, the interface becomes permanently frozen on that screen, blocking access to all previous view states.

## Expected Result
Inbound images must render clear inline previews smoothly. Tapping the file must expand a fluid lightbox modal displaying the asset instantly without forcing memory leaks or locking up navigation controls.
