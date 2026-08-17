# Campus to Corporate Ready — Workshop Hub

A complete, ready-to-deliver **2-day workshop** that prepares final-year students for their first job. This repository hosts every deliverable — ten animated session decks, a facilitator guide, participant handouts, program-operations documents, and a modern-workplace supplement — behind a single landing page.

**Live site:** `https://<your-username>.github.io/<repo-name>/`
(fill this in after you enable GitHub Pages — see below)

---

## What's inside

```
.
├── index.html                     ← the landing page
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

Replace any file in `materials/` with a newer version (keep the same filename), then:

```bash
git add .
git commit -m "Update materials"
git push
```

The site updates automatically within a minute. If you change filenames, update the matching paths in `index.html` too.

---

## A note on the QR codes

Three slides in the decks (and in the Modern Workplace supplement) contain **placeholder QR codes** pointing to example URLs. Before you deliver the workshop, swap them for your own live poll, resource links, and feedback form. Each slide carries an on-slide reminder.

---

## The workshop at a glance

**Day 1 — Foundations:** Corporate World · Etiquettes · Communication · Teamwork · Recap
**Day 2 — Readiness:** Personal Branding · Interview Skills · Ethics & Mindset · Mock Interview · Closing

Both days run 9:00 AM – 6:00 PM with breaks. Start with the **Facilitator Guide** — it has the timing, scripts, and talking points for every session.
