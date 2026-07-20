# [BUG-004] Generic Authentication Error Displayed During Offline Login

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Authentication Network Layer
- **Type**: Bug / UX / Error Handling
- **Severity**: Low
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Login Screen (Offline State)

## Preconditions
The device's network connection (Wi-Fi and Cellular Data) is completely disabled.

## Steps to Reproduce
1. Disable internet connectivity on the iOS test device.
2. Launch the application and navigate to the Login screen.
3. Enter a valid email address and password, then tap the "Confirm" button.

## Actual Result
The application surfaces a generic, unhandled system error alert: `"Login failed. The operation couldn't be completed. (RequestError error 10.)"`. This matches the exact string shown for incorrect credentials, hiding the true source of failure.

## Expected Result
The client application should execute a network reachability check. If offline, it must intercept the request and present a user-friendly dialogue: *"No internet connection. Please check your network settings and try again."*
