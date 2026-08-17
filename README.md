# Campus to Corporate Ready — Workshop Hub

A complete, ready-to-deliver **2-day workshop** that prepares final-year students for their first job. This repository hosts every deliverable — ten animated session decks, a facilitator guide, participant handouts, program-operations documents, and a modern-workplace supplement — behind a single landing page.

**Live site:** https://hedaprateek.github.io/campus-to-corporate/

> GitHub Pages serves this repository from the **root** of `main`. `index.html`, `.nojekyll`, and `materials/` must stay at the top level — if they get nested inside a subfolder, the live URL 404s and every download link breaks.

---

## Editing the site — the content editor

**<https://hedaprateek.github.io/campus-to-corporate/admin.html>**

Everything on the landing page comes from [`content.json`](content.json), and the editor is a form over
that file. It is **entirely static**: no server, no login, no API calls. It edits the content in your
browser, hands you the updated file, and GitHub's own website does the committing.

That last part is deliberate. Committing through the GitHub API from a browser needs a cross-origin
request to `api.github.com`, which corporate proxies and security appliances routinely intercept —
producing CORS failures that cannot be fixed from this end. Using github.com's normal upload page is
just an ordinary page visit, so it works from any network that can reach GitHub at all.

### Replacing a deck or document

1. Open the editor and find the file under **Materials**.
2. Click **Upload replacement ↗** — this opens GitHub's uploader already pointed at the right folder.
3. Drag the new version in, **keeping exactly the same filename** (there's a *Copy filename* button
   next to each file), and click *Commit changes*.

The path never changes, so every link on the site — and any link you have already shared — keeps
working. The site updates about a minute later.

File sizes on the site are read from the server at page load, so they correct themselves after a
replacement. There is nothing else to update.

> Uploading a file with a **different** name adds it alongside the old one rather than replacing it.
> If you want to do that, also update the matching *Deck file path* in the editor and commit the new
> `content.json` as below.

### Changing text and structure

The remaining panels edit every piece of copy on the page: hero, section headings, days, sessions,
trainer-kit documents, how-to steps, and the footer. Sessions, resources, stats and steps can be
added, reordered (↑ ↓) and deleted; whole days can be added or removed. Removing an entry takes it off
the page but leaves the underlying file in the repository.

When you're done:

1. Click **Download content.json** (or **Copy JSON** to paste instead).
2. Open <https://github.com/hedaprateek/campus-to-corporate/upload/main> and drop the downloaded
   `content.json` in — same filename, so it replaces the published one.
3. Commit. The site updates in about a minute.

Your edits are kept in the browser's local storage as you work, so closing the tab by accident doesn't
lose them — the editor offers to restore the draft next time. **Discard changes** throws the draft away
and reloads the published content. The "materials updated" date in the footer is stamped for you each
time you download or copy.

> The editor has no way to detect someone else editing `content.json` in the meantime. If two people
> are changing content, agree who holds the pen — the last upload wins.

---

## Viewing without downloading

Every deck and document on the site has a **View** button next to its download. It opens the file in Microsoft's free Office Web Viewer (`view.officeapps.live.com`) — no account, no download.

Two things to know:

- **Animations don't play reliably in the viewer.** The decks are built around click-advance builds; treat online view as a preview and deliver from PowerPoint.
- **The viewer needs the file to be publicly reachable.** It fetches the URL from Microsoft's servers. If this repository is ever made private, the View buttons stop working (downloads would too) — nothing else to change, but don't expect it to fail gracefully.

---

## What's inside

```
.
├── index.html                     ← the landing page
├── content.json                   ← all page content; the editor edits this
├── admin.html                     ← static content editor (no server, no login)
├── assets/
│   ├── og-preview.png             ← the image shown when the link is shared
│   └── og-preview-source.html     ← how that image was made; re-render to update it
├── materials/
│   ├── decks/                     ← 10 session decks (.pptx)
│   │   ├── S1_Corporate_World.pptx
│   │   ├── S2_Etiquettes.pptx
│   │   ├── S3_Communication.pptx
│   │   ├── S4_Teamwork.pptx
│   │   ├── S5_Day1_Recap.pptx
│   │   ├── S6_Personal_Branding.pptx
│   │   ├── S7_Interview_Skills.pptx
│   │   ├── S8_Ethics_Mindset.pptx
│   │   ├── S9_Mock_Interview.pptx
│   │   └── S10_Closing.pptx
│   ├── guides/
│   │   ├── Facilitator_Guide.docx
│   │   ├── Program_Toolkit.docx
│   │   └── Industry_Readiness_Playbook.docx
│   ├── handouts/
│   │   └── Participant_Handout_Pack.docx
│   └── supplements/
│       └── Modern_Workplace_2025_Supplement.pptx
└── .nojekyll                      ← tells GitHub Pages to serve files as-is
```

---

## Deploy to GitHub Pages (about 3 minutes)

You'll do this from your own computer, signed in to your GitHub account.

### 1. Create a new repository
On GitHub, click **New repository**. Name it something like `campus-to-corporate`. Make it **Public**. Don't add a README (this repo already has one). Create it.

### 2. Push these files
Download this whole folder, open a terminal inside it, and run:

```bash
git init
git add .
git commit -m "Campus to Corporate workshop hub"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Replace `<your-username>` and `<repo-name>` with your actual values.

### 3. Turn on GitHub Pages
In your repository on GitHub:
1. Go to **Settings → Pages**
2. Under **Source**, choose **Deploy from a branch**
3. Set branch to **main** and folder to **/ (root)**
4. Click **Save**

Wait about a minute. Your site goes live at:

```
https://<your-username>.github.io/<repo-name>/
```

That's the link you share. Anyone can open it and download the materials.

---

## Updating the materials later

The easy way is the [content editor](#editing-the-site--the-content-editor) — no git needed.

To do it from a terminal instead, replace any file in `materials/` with a newer version (keeping the
same filename), then:

```bash
git add .
git commit -m "Update materials"
git push
```

The site updates automatically within a minute. If you change filenames, update the matching `file`
paths in `content.json` too.

---

## A note on the QR codes

Three slides in the decks (and in the Modern Workplace supplement) contain **placeholder QR codes** pointing to example URLs. Before you deliver the workshop, swap them for your own live poll, resource links, and feedback form. Each slide carries an on-slide reminder.

---

## The workshop at a glance

**Day 1 — Foundations:** Corporate World · Etiquettes · Communication · Teamwork · Recap
**Day 2 — Readiness:** Personal Branding · Interview Skills · Ethics & Mindset · Mock Interview · Closing

Both days run 9:00 AM – 6:00 PM with breaks. Start with the **Facilitator Guide** — it has the timing, scripts, and talking points for every session.
