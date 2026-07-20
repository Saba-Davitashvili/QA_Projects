# [BUG-001] Service Request Submission Fails When Authenticated via Google Sign-In

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Authentication / Request Submission
- **Type**: Bug / Functional
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Desktop (Windows 11, Opera GX 131)
- **App Context**: Service Request Submission

## Preconditions
User is signed in using the Google Sign-In option.
User has completed the full service request flow (steps 1–5).

## Steps to Reproduce
1. Click on the "Submit Request" button.

## Actual Result
The system displays an error stating the user needs to be logged in to submit a request.

## Expected Result
A success toast/notification pops up: "Request has been successfully created".
