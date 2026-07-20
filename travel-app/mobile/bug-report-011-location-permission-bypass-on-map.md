# [BUG-011] Map Visualizes Precise User Location While Device Location Permissions Are Disabled

## Metadata
- **Project**: Mobile Social Travel & Booking App
- **Component**: Map Module / Location Permissions Privacy
- **Type**: Bug / Privacy / Security Bypass
- **Severity**: Critical
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: iOS (Mobile)
- **App Context**: Home Screen -> Map View

## Preconditions
The user is authenticated, on the Home screen, and has verified that location access is turned off in the iOS settings app.

## Steps to Reproduce
1. Open the mobile application and navigate to the Home view.
2. Locate and tap the "Open Map" action button.
3. Observe the initial focal point and blue tracking marker on the map interface.

## Actual Result
The map centers and renders a pinpoint marker over the user's precise real-time physical location, bypassing system-level permission controls.

## Expected Result
Since location access is revoked, the application must respect the system privacy flag. The map should default to a generic global/regional view, restrict coordinate tracking, or display a clean permission dialog stating: *"Location services are disabled. Please enable location permissions in your settings to view your current position."*
