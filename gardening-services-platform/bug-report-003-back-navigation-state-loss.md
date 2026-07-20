# [BUG-004] Back Navigation from Gardener Profile Redirects to Step 1 Instead of Step 6

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Navigation / Request Creation Flow
- **Type**: Bug / UX
- **Severity**: High
- **Priority**: Critical
- **Status**: Open

## Environment Details
- **Platform**: Desktop / Laptop (Windows 11, macOS 14)
- **App Context**: Gardener Selection Screen

## Preconditions
User is authorized as a customer.
User is on step 6 of the service creation flow (gardener matching list).

## Steps to Reproduce
1. Click on the "Profile" button on the right side of a gardener card.
2. Click the "Back" button in the upper-left corner of the page.

## Actual Result
The user is redirected to the first step of the service creation flow, losing all previously input data.

## Expected Result
The user should return to step 6 (the matching gardeners list) with all filter and navigation state intact.
