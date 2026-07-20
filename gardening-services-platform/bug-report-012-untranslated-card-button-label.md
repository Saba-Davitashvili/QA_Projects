# [BUG-025] Raw Localization Key "common.profile" Rendered on Gardener List Card

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: UI / Internationalization
- **Type**: Bug / UI
- **Severity**: Low
- **Priority**: Low
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Opera GX 131)
- **App Context**: Gardener Selection List

## Preconditions
User is logged in.
User has successfully submitted a service request.
User is on the matching gardeners list screen.

## Steps to Reproduce
1. Scroll down to the matching gardeners list.
2. Observe the profile button label on any gardener card.

## Actual Result
The button renders the raw localization key string "common.profile".

## Expected Result
The button should display the translated text (e.g., "Profile" or translated equivalent).
