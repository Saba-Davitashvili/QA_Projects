# [BUG-013] Gardener Base Service Rate Omitted from Price Breakdown Screen

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Pricing & Invoicing
- **Type**: Bug / UI
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Chrome 148)
- **App Context**: Gardener Connection Screen

## Preconditions
User is logged in.
User has submitted a service request.

## Steps to Reproduce
1. Select any gardener from the matched list.
2. Click the "Connect" button.

## Actual Result
The price updates to a different amount after clicking "Connect", and individual service base rates are not listed in the price breakdown.

## Expected Result
The price should remain consistent with the breakdown shown under the gardener's info, listing all base rates.
