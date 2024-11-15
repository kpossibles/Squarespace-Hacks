# Squarespace-Hacks
Squarespace hacks that I've found so you don't have to look thru the forums

# Add a custom Bluesky icon to Squarespace
https://forum.squarespace.com/topic/260721-social-media-icons-can-we-change-them-and-how

1. Go to Custom CSS page on your site url where it ends in `/config/pages/website-tools/custom-css`. You can get there thru Website > Pages > Website Tools (at bottom of sidebar) > Custom CSS.
2. Paste in the code at the bottom of the Custom CSS page and save.
3. Paste in the url of your Bluesky link at your site url ending in `/config/settings/website/social-links`
4. It must start with bsky.app for it to work. Eg) `https://bsky.app/profile/kpossibles.bsky.social`

Customize your bluesky icon by updating the url in the code below:
* Black: `https://raw.githubusercontent.com/OzzyCzech/bluesky-icon/refs/heads/main/dist/bluesky-icon.svg`
* White: `https://raw.githubusercontent.com/OzzyCzech/bluesky-icon/refs/heads/main/dist/bluesky-icon.white.svg`
* Blue: `https://raw.githubusercontent.com/OzzyCzech/bluesky-icon/refs/heads/main/dist/bluesky-icon.blue.svg`

Thanks to [OzzyCzech](https://github.com/OzzyCzech/bluesky-icon) for the SVG!
```
//Bluesky Icon//
footer.sections a.sqs-svg-icon--wrapper[href*="bsky.app"] svg {
    visibility: hidden;
}
footer.sections a.sqs-svg-icon--wrapper[href*="bsky.app"] {
    background-image: url(https://raw.githubusercontent.com/OzzyCzech/bluesky-icon/refs/heads/main/dist/bluesky-icon.white.svg) !important;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
}
```
