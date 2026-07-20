# [BUG-095] Price Discrepancy Between Customer View and Gardener Offer View

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Pricing & Invoicing / Real-time Offers
- **Type**: Bug / Logic
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Opera GX 131)
- **App Context**: Request Details Screen

## Preconditions
User has both customer and gardener profiles on the platform.
Gardener has sent a price offer on an active request.

## Steps to Reproduce
1. Open the request as a customer and note the displayed price.
2. Switch to the gardener profile and view the same request.

## Actual Result
The gardener sees a price of 300 GEL, while the customer sees 375 GEL for the exact same offer.

## Expected Result
The same price should be rendered on both customer and gardener profile views.
