# [BUG-009] Tagged User Profile Navigation Blocked Inside Full-Screen Photo View

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Feed / Photo Lightbox / Tag Navigation
- **Type**: Bug / Navigation Failure
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Feed — full-screen photo viewer overlay (tagged user mentions)

## Steps to Reproduce
1. Open a post's photo in full-screen view.
2. Click on a **tagged user** mentioned in the post text.

## Actual Result
The click event is not handled. The system remains in the full-screen photo view, and no navigation to the tagged user's profile page occurs. The `@mention` element appears as a hyperlink but lacks a bound route handler within the lightbox overlay.

## Expected Result
Clicking a tagged user mention inside the full-screen photo view should immediately navigate the user to the tagged user's profile page.

