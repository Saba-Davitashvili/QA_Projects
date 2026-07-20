# [BUG-067] Suggestion to Include 1.25x Platform Fee in Initial Quote Stage to Prevent User Trust Issues

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Pricing & Invoicing
- **Type**: Improvement / UX
- **Severity**: Low
- **Priority**: Low
- **Status**: Open

## Environment Details
- **Platform**: All Platforms
- **App Context**: Request Creation Flow

## Preconditions
When choosing a service, the user is shown the base rate. However, once the request is submitted, the system automatically applies a 1.25x platform coefficient surcharge. This sudden price increase causes confusion and trust issues for users.

## Steps to Reproduce
1. Select any service and view the estimated price.
2. Observe the price change after creating the request.

## Actual Result
The 1.25x platform fee multiplier is only visible after the request has been submitted, creating an unexpected price jump.

## Expected Result
Apply the 1.25x coefficient multiplier to the initial estimated price quote at the service selection stage, so the customer sees the final price upfront.
