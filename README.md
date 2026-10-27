# Fark Reader — Android/Kotlin starter

This is a small native Android reader for Fark's published RSS feed.

## Legal/usage note

Fark's FAQ currently says that an RSS feed exists and is intended as a convenience, but also warns that attempting to create a duplicate of Fark can result in a cease-and-desist. Fark's legal page also prohibits automated scraping without express written permission.

This project therefore does **not** scrape Fark's HTML pages. It uses the published RSS endpoint and opens the original destination article in the user's browser.

Before publishing this app publicly, contact Fark for permission/licensing if the app's scope could be considered a duplicate of Fark or if you intend to use Fark branding beyond what Fark expressly permits.

## Current behavior

- Native Jetpack Compose UI.
- Main feed from `https://www.fark.com/fark.rss`.
- Refresh button in the upper-right.
- No background polling.
- No automatic refresh after the initial load.
- The visible list is replaced only after the user taps Refresh and a new feed is successfully loaded.
- Headlines open in the device browser.
- Basic source/domain and comment-count parsing.
- No Fark login credentials are collected.
- No comments are copied into the app.

## Open in Android Studio

1. Install the current Android Studio.
2. Open the `FarkReader` folder.
3. Allow Android Studio to download the Gradle/Android dependencies.
4. Connect an Android phone with USB debugging enabled, or create an emulator.
5. Press Run.

## Important feed detail

The RSS feed is controlled by Fark. Its exact XML fields can change. If the feed does not expose comment counts in a stable field, the app will simply omit the count rather than scraping the Fark web page.

## Next logical versions

- Local last-successful-feed cache.
- Category feeds, if Fark provides appropriate RSS endpoints/permission.
- Favorites stored locally.
- Share button.
- Settings.
- Accessibility improvements.
- Dark theme.
- A dedicated "Open on Fark" action.
- Error retry UI.

