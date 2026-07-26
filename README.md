# heartdistance-legal

Public web pages and App Store text for the **HeartDistance** iPhone app. Static HTML, no
build step — it is served straight from GitHub Pages.

## Contents

| File | Purpose | Used for |
| --- | --- | --- |
| `index.html` | Landing page with App Store download button, features, privacy promise, FAQ (EN + DE) | App Store Connect *Marketing URL*, link in bio, anything you share |
| `privacy.html` | Privacy policy (DE + EN) | App Store Connect *Privacy Policy URL* — **required** |
| `support.html` | Support page with troubleshooting and contact (EN + DE) | App Store Connect *Support URL* — **required** |
| `app-store-listing.md` | Name, subtitle, promo text, keywords, description and marketing copy, in B2-level English and German. Every field checked against Apple's character limit. | Paste into App Store Connect |

## Before you submit: replace the App Store link

The download buttons currently point at a placeholder:

```
https://apps.apple.com/app/heartdistance
```

Once the app is approved, replace it with the real product URL, which looks like
`https://apps.apple.com/app/heartdistance/id1234567890`. It appears in three places:

```
index.html    2 occurrences (hero button, German section)
```

Find them with:

```sh
grep -rn "apps.apple.com" .
```

Adding `?mt=8` or a campaign token (`&ct=launch-post`) to the URL lets you see in App Store
Connect where the downloads came from.

## Enabling GitHub Pages

Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
The pages are then reachable at:

- `https://marco-p-keller.github.io/heartdistance-legal/`
- `https://marco-p-keller.github.io/heartdistance-legal/privacy.html`
- `https://marco-p-keller.github.io/heartdistance-legal/support.html`

Apple checks that the privacy and support URLs load during review, so confirm both open in
a browser before submitting.

## Language level

The English on every page and in the listing copy is deliberately kept at **CEFR B2**:
short sentences, everyday vocabulary, no idioms. It is easier to read for non-native
speakers, and it survives Apple's and users' machine translation much better.
