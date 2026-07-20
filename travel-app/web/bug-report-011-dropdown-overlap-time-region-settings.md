# [BUG-011] Visual UI Overlap of Dropdown Options in Time Zone and Date Format Selectors

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Settings / Time & Region / Dropdown UI
- **Type**: Bug / UI Rendering
- **Severity**: Low
- **Priority**: Low
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Settings → Time and Region page

## Preconditions
User is on the **Settings → Time and region** page.

## Steps to Reproduce
1. Open the **Date format** dropdown list.
2. Open the **Time zone** dropdown list.

## Actual Result
Options from both dropdown menus visually merge into a single expanded section. Text elements from the two lists overlap each other, rendering both menus unreadable and preventing accurate selection.

## Expected Result
Each dropdown menu must open in isolation. Opening a second dropdown should automatically collapse the previously opened menu to prevent text overlap and maintain a clean, usable selection interface.

