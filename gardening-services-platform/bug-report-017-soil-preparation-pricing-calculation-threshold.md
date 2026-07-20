# [BUG-038] Non-Linear Pricing Logic Deviation After Selecting Soil Preparation Service

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Pricing & Invoicing
- **Type**: Bug / Logic
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Opera GX 131)
- **App Context**: Request Creation - Step 2

## Preconditions
User is logged in.
User selects service category "Soil Preparation".

## Steps to Reproduce
1. Select "Soil Preparation" service.
2. Change quantity value to 1.
3. Change quantity value to 2.

## Actual Result
The price calculation scale logic deviates and changes incorrectly once quantity exceeds 2.

## Expected Result
Pricing should scale linearly and consistently based on the unit rate specified for "Soil Preparation" service.
