# Squarespace-Hacks
Squarespace hacks that I've found so you don't have to look thru the forums

# Add a Custom Bluesky Icon to Squarespace
https://forum.squarespace.com/topic/260721-social-media-icons-can-we-change-them-and-how

1. Go to Custom CSS page on your site url where it ends in `/config/pages/website-tools/custom-css`. You can get there thru Website > Pages > Website Tools (at bottom of sidebar) > Custom CSS.
2. Paste in the code at the bottom of the Custom CSS page and save.
3. Paste in the url of your Bluesky profile link in Social Links section on your site url where it ends in `/config/settings/website/social-links`
4. Eg) `https://bsky.app/profile/kpossibles.bsky.social` or `https://bsky.app/profile/sara.pizza`

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
# How to Set Your Domain Name as Your Handle in Squarespace
This is for people who have their domain name through Squarespace.

1. Go to this link and replace DOMAINNAME with the domain name `https://account.squarespace.com/domains/managed/DOMAINNAME` Eg) `https://account.squarespace.com/domains/managed/google.com`
2. Click DNS
3. In the Custom Records section, click ADD RECORD button
4. Follow the steps from the [Bluesky tutorial](https://bsky.social/about/blog/4-28-2023-domain-handle-tutorial) to fill in your info
5. Wait a couple minutes for the change to propogate the internet, then click Verify DNS Record button in Bluesky

![Squarespace DNS Custom Records fields](https://github.com/kpossibles/Squarespace-Hacks/blob/0fe5de8b1c70a8ccd7d1c44333e33ae073b7c40f/images/squarespace-dns-record-bluesky.png)
