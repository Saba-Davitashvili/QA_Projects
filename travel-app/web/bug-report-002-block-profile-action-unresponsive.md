# [BUG-002] Block Profile Action Unresponsive from "Not Interested" Context Menu

## Metadata
- **Project**: Social Travel & Booking Platform
- **Component**: Social Feed / Post Actions / User Block Pipeline
- **Type**: Bug / Functional Failure
- **Severity**: High
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Home page — post context menu ("Not Interested" flow)

## Preconditions
User is authorized and is on the home page.

## Steps to Reproduce
1. Select any post on the home page.
2. Click the three dots (**...**) in the upper right corner of the post.
3. Select **"Not Interested"** from the context menu.
4. Click the **"Block Profile"** button.

## Actual Result
Clicking the **"Block Profile"** button produces no system reaction. The click event is silently consumed — no API call is dispatched, no confirmation dialog appears, and the target profile is not blocked.

## Expected Result
Clicking **"Block Profile"** should execute the block action, display a success confirmation message (*"User has been blocked"*), and immediately remove the blocked user's post from the active feed.

