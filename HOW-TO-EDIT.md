# How to edit your website — no coding needed

Your site now has a built-in **Edit Mode**. Everything below is done from your browser.

## 1. Open the editor

Go to your website and add `#edit` to the address, e.g.:

```
https://rachelchan.co/#edit
```

(Or press **Ctrl + Shift + E** — ⌘ + Shift + E on Mac.)

A panel opens on the right. Everything you change is **previewed live** on the page.

- **👁 Preview** hides the panel so you can see the full site; click the floating **✎** button to come back.
- **✕ Close** exits the editor (your changes stay saved as a draft in that browser).

## 2. What you can edit

| Section | What it changes |
|---|---|
| **Website & SEO** | Site name, browser tab title, Google search description, search tags (keywords), social-share preview image |
| **Typography** | Font style (Raleway, Roboto, Montserrat, Inter, Lato, Open Sans, Playfair Display, Cormorant Garamond, or plain Helvetica/system), font **size** (80–140 %), font **spacing** (letter-spacing) |
| **Intro & About** | Sidebar intro heading & tagline, About dialog heading and paragraphs (add/remove), email, LinkedIn URL |
| **Home Video** | The background video URL on the home screen |
| **Menu Labels** | The six menu items (HOME, VIDEO PROJECTS, …) |
| **Projects** | Every project in every category: title, year, client, role, description, cover image, external link, and its media (image / YouTube embed / video). Add, delete, duplicate, and re-order with the ↑ ↓ buttons |
| **Publish** | Download the file, save/discard your draft, or push a copy to GitHub |

## 3. Publish your changes

Your website is uploaded manually to your host, so publishing is a 3-step routine:

1. In the editor, click **⬇ Download site-config.js** — the file lands in your Downloads folder.
2. Log in to your **web host's file manager** (the place where `index.html` lives).
3. **Upload `site-config.js`** into that same folder, replacing the old one.

Done — your changes are live immediately. You never need to touch `index.html` again for content changes.

> **Drafts:** your in-progress edits are auto-saved in the browser you're using. If you close the tab and come back to `#edit`, they're still there until you publish or click **Discard**. Drafts are per-browser and per-device.

## 4. Optional: keep GitHub in sync

In the **Publish** section you can paste a GitHub *fine-grained personal access token* (with **Contents: Read and write** permission for `cyunmin12/rachelchan`) and click **Push to GitHub**. This commits `site-config.js` to your repository so your GitHub copy always matches the live site. The token stays only in your browser.

## 5. If something goes wrong

- **Site looks wrong after publishing:** open the editor, click **Discard**, download a fresh `site-config.js`, and upload it — that restores the content the site was built with.
- **Deleting site-config.js** from the host also works: the site falls back to its built-in defaults automatically. Nothing breaks.

## Note for the first deployment

This update added two new files to the repository. When you deploy, upload **all three** to your host:

1. `index.html` (the updated one)
2. `site-config.js` (new)
3. `HOW-TO-EDIT.md` (optional — it's just this guide)
