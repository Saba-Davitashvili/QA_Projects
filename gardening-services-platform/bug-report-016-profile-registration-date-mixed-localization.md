# [BUG-035] Mixed-Language Registration Date Displayed in Georgian UI

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: UI / Internationalization
- **Type**: Bug / Localization
- **Severity**: Low
- **Priority**: Low
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Opera GX 131)
- **App Context**: User Profile Page

## Preconditions
The website UI language is set to Georgian.

## Steps to Reproduce
1. Navigate to any user profile page.

## Actual Result
The date portion is displayed in mixed languages: "წევრი: 21 May 2026-დან" (English month inside Georgian sentence).

## Expected Result
The entire date string should be localized to Georgian: "წევრი: 21 მაისი 2026-დან".
