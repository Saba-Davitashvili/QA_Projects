# [BUG-010] Tagged User @Mention in Feed Triggers Post Open Instead of Profile Navigation

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Feed / Tag Routing / Event Propagation
- **Type**: Bug / Incorrect Routing
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Home feed — inline @mention tags within post text

## Steps to Reproduce
1. Locate a post in the feed containing a tagged user (`@username`) in the post text.
2. Click on the **tagged user mention**.

## Actual Result
Instead of navigating to the tagged user's profile, the system intercepts the click as a post-open event. The photo expands to full-screen view. The `@mention` click handler is overridden by the parent post container's click event due to missing event propagation control (`stopPropagation`).

## Expected Result
Clicking a tagged user `@mention` in the feed should navigate directly to that user's profile page. The tag element's click event must stop propagation to prevent the parent post container from capturing and redirecting the interaction.

