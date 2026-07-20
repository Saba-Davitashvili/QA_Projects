# [BUG-008] Comment Author Profile Navigation Blocked Inside Full-Screen Photo View

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Feed / Photo Lightbox / Comment Navigation
- **Type**: Bug / Navigation Failure
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Feed — full-screen photo viewer overlay (comment section)

## Steps to Reproduce
1. Open a post's photo in full-screen view.
2. Click on a **comment author's name or avatar**.

## Actual Result
The click event is not handled. The system remains in the full-screen photo view, and no navigation to the comment author's profile page occurs. The interactive element is visually rendered but the routing handler is not bound within the lightbox context.

## Expected Result
Clicking a comment author's name or avatar inside the full-screen photo view should navigate the user to that commenter's profile page.

