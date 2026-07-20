# [BUG-013] Sort Function Failure on Explore Component Tour Search Results

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Search & Filtering Layer
- **Type**: Bug / Functional Failure
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Explore Screen -> Tour Category

## Preconditions
The user is on the Explore screen tab.

## Steps to Reproduce
1. Tap the "Tour" category option on the Explore interface.
2. Tap the primary "Search" field or execute an empty query to populate the result list cards.
3. Tap the "Sort" control element and select the filter item: "Price Low to High".

## Actual Result
The selection registers visually, but the array order of the listed tour packages is completely unaffected. No data reloading indicator triggers, and pricing strings remain scattered out of chronological order.

## Expected Result
The interface should capture the filter update event, execute a localized sorting routine or dispatch a refreshed backend API query with the correct sorting params, and immediately display the tour array prioritized strictly by the lowest price tier up to the highest.
