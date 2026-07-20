# [BUG-011] Decimal Price Values Rounded Up Erroneously After 1.25x Multiplier

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Pricing & Invoicing
- **Type**: Bug / Precision
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Chrome 148)
- **App Context**: Price Breakdown Modal

## Preconditions
User is logged in.
User selected services totaling 230 GEL.
User submitted the request and selected their gardener.

## Steps to Reproduce
1. Open the price breakdown panel.

## Actual Result
The price calculation displays 288 GEL instead of the exact 287.5 GEL.

## Expected Result
The calculated price should show the exact decimal result: 230 x 1.25 = 287.5 GEL.
