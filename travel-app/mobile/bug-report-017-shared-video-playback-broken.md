# [BUG-017] Broken Playback Engine inside Chat Shared Media Viewer Workspace

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Media Viewer Workspace
- **Type**: Bug / Media Playback
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Chat Info -> Shared Media

## Preconditions
The user has accessed a conversation containing at least one verified video file delivery.

## Steps to Reproduce
1. Enter the specific chat channel and tap the upper header profile layout to open Chat Settings.
2. Select the "View Media" repository directory.
3. Locate and select a video thumbnail card to trigger full-screen preview mode.
4. Attempt to interact with the center or bottom alignment "Play" icon button.

## Actual Result
The preview environment opens successfully, but remains anchored to a static frame canvas. Pressing the play button does not initiate the video rendering stream, leaving the playback system fully unresponsive.

## Expected Result
Tapping a video file within the shared directory must launch the media core layout cleanly, enabling smooth streaming playback with functional transport parameters (Play, Pause, Scrubbing).
