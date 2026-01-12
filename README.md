# Meaty Reviews

Extract reviews from Chrome Web Store extension pages.

## Why a Bookmarklet?

Chrome extensions cannot script the Chrome Web Store (security restriction). This bookmarklet runs directly in the page context, bypassing that limitation.

## Installation

1. Open `index.html` in your browser
2. Drag the "Extract Reviews" button to your bookmarks bar

**Or manually:**
1. Create a new bookmark
2. Set the URL to the contents of `bookmarklet.js`

## Usage

1. Navigate to a Chrome Web Store extension page
2. Click the "Extract Reviews" bookmarklet
3. Wait while it scrolls and collects reviews (up to 250)
4. JSON file downloads automatically

## JSON Output

```json
{
  "extensionName": "Extension Name",
  "extractedAt": "2024-01-15T12:00:00.000Z",
  "reviewCount": 150,
  "reviews": [
    {
      "stars": 5,
      "date": "Jan 10, 2024",
      "text": "Great extension!"
    }
  ]
}
```

## Files

- `index.html` - Installation page with draggable bookmarklet
- `bookmarklet.js` - Raw bookmarklet code (minified)
