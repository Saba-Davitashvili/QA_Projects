# [BUG-008] UI Freeze and Significant Network Latency on Registration Submission

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Registration Layer / Thread Performance
- **Type**: Bug / Performance / UI responsiveness
- **Severity**: Medium
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Registration Submission page

## Preconditions
The user has populated all mandatory registration fields with valid criteria.

## Steps to Reproduce
1. Open the application and navigate to the registration screen.
2. Complete all required profile setup fields with valid data.
3. Tap the "Confirm and Continue" button once.
4. Attempt to interact with the screen or tap the button sequentially during the subsequent delay.

## Actual Result
The interface records the button press state visually, but the screen freezes completely. No loading spinner, progress bar, or activity indicator is presented to signal background processing. After a long delay, the system shifts automatically to the email verification module.

## Expected Result
Tapping the action button must instantly trigger a non-blocking asynchronous request accompanied by a visible loading indicator (e.g., a spinner overlay). Screen navigation to the email verification flow should finalize smoothly within acceptable latency thresholds (under 2 seconds).
