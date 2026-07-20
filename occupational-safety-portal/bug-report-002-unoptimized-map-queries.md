# [BUG-002] Un-Optimized Map Query Formulation Executing Fallback Regional View

## Metadata
- **Project**: Professional Occupational Safety & Risk Management Platform
- **Component**: Geographic Hyperlink Routing Node (`onboarding-nav-geo-02`)
- **Type**: Bug / Map Integration
- **Severity**: Low
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Contact Details page (`/contact`)

## Steps to Reproduce
1. Navigate to the contact directory page.
2. Locate the designated interactive text element containing the physical office address string.
3. Click the address link to trigger the third-party mapping platform redirect event.

## Actual Result
The routing engine compiles an un-escaped or truncated query parameter string. This triggers the external mapping software to default to a zoomed-out regional city view, completely obscuring the exact location point.

## Expected Result
The anchor tag wrapper must pass cleanly escaped string parameter data blocks matching a precise address string configuration (e.g., `?q=Street+Number,+Suite,+City`) or explicit GPS coordinates to drop the pin at the exact office location.
