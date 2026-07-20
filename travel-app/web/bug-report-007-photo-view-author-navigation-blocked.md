# [BUG-007] Post Author Profile Navigation Blocked Inside Full-Screen Photo View

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Feed / Photo Lightbox / Profile Navigation
- **Type**: Bug / Navigation Failure
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Feed — full-screen photo viewer overlay

## Steps to Reproduce
1. Open a post's photo in full-screen view.
2. Click on the **post author's name or avatar**.

## Actual Result
The click event is not handled. The system remains in the full-screen photo view, and no navigation to the author's profile page occurs. The clickable element appears visually interactive but has no bound routing logic in the lightbox context.

## Expected Result
Clicking the post author's name or avatar inside the full-screen photo view should navigate the user to the author's profile page.

