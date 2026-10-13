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

## 2. The five tabs

Everything is grouped into five tabs at the top of the panel:

| Tab | What you do there |
|---|---|
| **✏️ Text** | Your name, welcome heading & tagline, the "About me" text (add/remove paragraphs, **drag ⠿ to re-order them**), profile picture, email, LinkedIn. *Collapsible extras:* menu names, Google/search & social-sharing settings |
| **🎨 Design** | Font style (Raleway, Roboto, Montserrat, Inter, Lato, Open Sans, Playfair Display, Cormorant Garamond, or plain Helvetica/system), font size slider, letter-spacing slider, **cover picture shape/fit/size for all projects at once**, and — folded away under *🎬 Home background video* — the home video |
| **🖼️ Projects** | Pick a section, then edit any project: title, year, client, role, description, cover image, links and media. Add / copy / delete with one tap, and **drag the ⠿ handle to re-order** (projects *and* the media inside them). Folded under *Cover shape, columns & showreel* you'll find the **cover ratio override** (with one tap *apply it to all projects*), the **gallery columns** (how many pictures sit side-by-side inside the project), and the optional **showreel video** (see below). An **external link URL** makes a button appear on the project page |
| **📱 Mobile** | Appearance of the **phone version only**: text size, spacing, gallery columns, plus a **📱 phone preview** that shows your site at phone width updating live |
| **📤 Publish** | One big green button + 3 simple steps to put your changes live. *Collapsible extra:* GitHub token & sync |

### Showreel for one project

Any single project can have its own **showreel video**: open the project in the **Projects** tab, unfold *Cover shape, columns & showreel*, and upload or paste a video URL there. That project's tile then **plays the video automatically** (muted, looping) instead of showing its cover picture — with **no title and no dark overlay** — while still opening the project when clicked. On phones, the whole card plays the video and tapping it opens the project.

Want it first in its section? **Drag the project's ⠿ handle to the top of the list.** Leave the showreel URL empty to go back to a normal picture cover.

### The About page

The About dialog pairs your heading with the profile photo (heading left, photo right; stacked on phones), then your paragraphs, then a neat **contact footer** where your email and LinkedIn appear as buttons matching the site's button style. It's all edited in the **Text** tab — the buttons appear automatically once Email / LinkedIn are filled in.

### Drag & drop

- **Re-order:** drag the **⠿** handle on any project row, any media row inside a project, or any "About me" paragraph — drop it where you want; a red line shows the landing spot. The old **↑ ↓** buttons still work too.
- **Upload:** drag a picture/video file from your computer and **drop it straight onto any ⬆ Upload button** — no file-picker needed.

## 3. Uploading images & videos

You can upload media files straight from the editor — no separate uploading tool needed:

- **⬆ Upload** buttons appear next to the *home video*, the *share image*, each project's *cover image*, each project's *showreel video*, and every *media row* inside a project. You can click one — or simply **drag a file onto the button** and let go.
- The first time, paste your **GitHub token** into the *Publish* tab under **GitHub (advanced)** (fine-grained token with **Contents: Read and write** for `cyunmin12/rachelchan`). It is stored only in your browser. If you forget, the editor opens that spot for you automatically.
- Pick a file → it is uploaded to the repo's `media/` folder → the permanent public URL is **filled into the field automatically** and previews live.
- For project media, the type (image / video) is detected automatically.
- Limits: **95 MB per file**. Keep the home background video small (a few MB) so your site loads fast.

> **Important:** uploaded media is served from GitHub, so the repository must be **public** for visitors to see the images/videos. (Your GitHub → repo → Settings → General → Danger Zone → Change visibility.) The rest of your site is unaffected.

## 4. Publish your changes

Your website is uploaded manually to your host, so publishing is a 3-step routine:

1. In the editor, click **⬇ Download site-config.js** — the file lands in your Downloads folder.
2. Log in to your **web host's file manager** (the place where `index.html` lives).
3. **Upload `site-config.js`** into that same folder, replacing the old one.

Done — your changes are live immediately. You never need to touch `index.html` again for content changes.

> **Drafts:** your edits are saved in the browser **automatically as you type** — closing the tab or the whole browser won't lose them. Come back to `#edit` and carry on until you publish or click **Discard**. Drafts are per-browser and per-device.

## 5. Optional: keep GitHub in sync

In the **Publish** section you can paste a GitHub *fine-grained personal access token* (with **Contents: Read and write** permission for `cyunmin12/rachelchan`) and click **Push to GitHub**. This commits `site-config.js` to your repository so your GitHub copy always matches the live site. The token stays only in your browser.

## 6. If something goes wrong

- **Site looks wrong after publishing:** open the editor, click **Discard**, download a fresh `site-config.js`, and upload it — that restores the content the site was built with.
- **Deleting site-config.js** from the host also works: the site falls back to its built-in defaults automatically. Nothing breaks.

## Note for the first deployment

This update added two new files to the repository. When you deploy, upload **all three** to your host:

1. `index.html` (the updated one)
2. `site-config.js` (new)
3. `HOW-TO-EDIT.md` (optional — it's just this guide)
