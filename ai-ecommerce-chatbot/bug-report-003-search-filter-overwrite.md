# [BUG-003] Search Parameter Filtering Overwrite

## Metadata
- **Project**: AI-Powered E-commerce Search & Chatbot Platform
- **Type**: Bug / Search Relevance
- **Severity**: High
- **Date Discovered**: 2026-06-30
- **Status**: Reported

## Environment Details
- **URL / App Context**: Storefront search bar — product results page
- **OS / Platform**: OS Independent
- **Build / Version**: Production

## Description
When a user applies multiple attribute filters (e.g., brand + price range + color), later-added filter parameters overwrite earlier ones in the search query instead of combining them. This causes incorrect search results that do not reflect all selected filters.

## Steps to Reproduce
1. Navigate to the storefront search/product listing page.
2. Enter a broad search term (e.g., `"jacket"`).
3. Apply Filter A from the sidebar (e.g., select a specific brand).
4. While Filter A is active, apply Filter B (e.g., select a price range).
5. Observe the results and the active filter state.

## Actual Behavior
Filter B overwrites Filter A in the underlying search query. The results only reflect the most recently applied filter — previously selected filters are silently dropped from the active parameter set. The filter UI chips may still show both filters as active, creating a false impression.

## Expected Behavior
All applied filters should be combined additively in the search query (AND logic). Applying a new filter must append to the existing parameter set without removing previously active filters. The results should reflect all concurrently active filter conditions.
