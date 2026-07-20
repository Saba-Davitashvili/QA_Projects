# [BUG-001] Incorrect Validation in Restriction Section — Maximum Stay Accepted Below Minimum Stay

## Metadata
- **Project**: — Social Travel & Booking Platform
- **Component**: Hotel Listing / Room Configuration / Validation (`restriction-bounds`)
- **Type**: Bug / Input Validation
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Hotel Listing page — "Room Category & Basics" configuration

## Preconditions
User is authorized and is on the hotel listing page: "Room Category & Basics" (Create a room type that guests can book).

## Steps to Reproduce
1. Navigate to the **"Restriction"** section of the room configuration form.
2. Enter `5` in the **Minimum stay (nights)** field.
3. Enter `3` in the **Maximum stay (nights)** field.
4. Click the **"Next"** button.

## Actual Result
The system accepts the logically invalid data and saves the parameters without triggering any validation error. A maximum stay value lower than the minimum stay is persisted to the backend.

## Expected Result
The system should block the save operation. Cross-field validation must trigger, highlight the invalid fields in red, and display the message: *"Maximum stay cannot be less than minimum stay."*

