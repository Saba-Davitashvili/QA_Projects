# [BUG-019] Service Price Input Accepts Alphabetic Characters and Falsely Indicates Success

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Gardener Portal / Input Validation
- **Type**: Bug / Logic
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Opera GX 131)
- **App Context**: Gardener Service & Prices Settings

## Preconditions
User is logged in as a gardener.

## Steps to Reproduce
1. Navigate to the gardener profile and go to the "Services & Prices" page.
2. Enter a value containing letters (e.g., "25e") into a global price field.
3. Click "Save All Prices".
4. Refresh the page.

## Actual Result
The field accepts "25e" and displays a success toast after saving. However, upon page refresh, the value reverts to 0, indicating the save silently failed.

## Expected Result
The input field should reject non-numeric characters. If an invalid value is entered, saving should be blocked, and a validation warning displayed.
