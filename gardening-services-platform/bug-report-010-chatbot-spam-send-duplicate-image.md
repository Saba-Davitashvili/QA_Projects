# [BUG-021] Spamming Send Button in Chatbot Widget Dispatches Duplicate Image Attachments

## Metadata
- **Project**: On-Demand Gardening & Landscaping Service Platform
- **Component**: Chatbot Widget / Input Controls
- **Type**: Bug / Logic
- **Severity**: Medium
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Desktop / Laptop (Windows 11, macOS 14)
- **App Context**: AI Support Chatbot Widget

## Preconditions
User is in the AI support chatbot section.

## Steps to Reproduce
1. Select an image file to upload/send.
2. Rapidly click the "Send" button multiple times.

## Actual Result
The image is sent twice or multiple times to the chat feed.

## Expected Result
The image should only be sent once, and the "Send" button should be debounced or disabled immediately after the first click.
