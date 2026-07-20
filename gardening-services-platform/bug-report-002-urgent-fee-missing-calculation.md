# [BUG-002] Additional Urgent Service Fee Excluded from Final Price Calculation

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Pricing & Invoicing
- **Type**: Bug / Logic
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Chrome 148)
- **App Context**: Chat Price Summary / Final Bill

## Preconditions
User is logged in.
User has submitted a service request that includes an urgent service option.

## Steps to Reproduce
1. Choose a gardener who has an additional fee specified for urgent orders.
2. Review the price summary in the chat panel.

## Actual Result
The urgent service fee surcharge is not included in the final price calculation.

## Expected Result
The urgent service fee surcharge is correctly added to the total calculation amount.
