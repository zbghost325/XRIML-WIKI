---
tags:
  - Guide
date: 2026-04-01
version: "2.0"
---

# How to Edit This Wiki

<div class="page-meta">
  <span class="meta-date">Last updated: 2026-04-01 &middot; v2.0</span>
  <span class="tag">Guide</span>
</div>

This guide explains how to update the XRIML Wiki. **No coding experience required** — you can edit everything directly in your web browser.

## Quick Edits (Browser Only)

### Step 1: Go to the GitHub Repository

Navigate to: `https://github.com/zbghost325/XRIML-WIKI`

### Step 2: Find the File to Edit

All content lives in the `docs/` folder:

```
docs/
├── index.md                ← Homepage
├── how-to-edit.md          ← This guide
├── tags.md                 ← Tag index (auto-generated)
├── equipment/              ← Resource Guide (all equipment categories)
│   ├── overview.md
│   ├── vr-headsets.md
│   ├── ar-headsets.md
│   ├── mr-headsets.md
│   ├── xr-accessories.md
│   ├── 360-cameras.md
│   ├── 360-accessories.md
│   ├── motion-capture.md
│   ├── volumetric-capture.md
│   ├── workstations.md
│   ├── displays.md
│   ├── software.md
│   └── legacy.md
├── trainings/              ← Keralia Training guides
│   ├── overview.md
│   └── 360-camera-gopro-max-video-editing.md
├── policies/               ← Lab rules, reservations, checkout
│   ├── lab-rules.md
│   ├── reservations.md
│   └── equipment-checkout.md
├── spaces/                 ← Lab rooms and spaces
├── software/               ← Software guides
├── about/                  ← Lab info and contact
├── images/                 ← All images go here
└── stylesheets/            ← Custom CSS (advanced)
```

### Step 3: Edit the File

1. Click on any `.md` file
2. Click the **pencil icon** (Edit this file)
3. Make your changes
4. Scroll down and click **"Commit changes"**
5. The wiki will automatically rebuild (takes ~1 minute)

---

## Page Metadata: Tags & Version Dates

Every content page includes **YAML frontmatter** at the top and a **metadata banner** below the title. When editing or creating pages, follow this pattern:

```yaml
---
tags:
  - Equipment
  - VR
  - Keralia Training    # Add this tag for Keralia training content
date: 2026-04-01        # Update when content changes
version: "1.1"          # Bump version on updates
---
```

Then add the visual banner after the `# Title`:

```html
<div class="page-meta">
  <span class="meta-date">Last updated: 2026-04-01 &middot; v1.1</span>
  <span class="tag">Equipment</span>
  <span class="tag">VR</span>
  <span class="tag tag-keralia">Keralia Training</span>
</div>
```

Use `class="tag tag-keralia"` for the special Keralia Training tag (gold styling).

### Equipment Page Icons

Equipment pages use inline Material icons to indicate availability:

```markdown
### Meta Quest 3 :material-cart-outline: :material-access-point:
```

| Icon | Meaning |
|------|---------|
| `:material-cart-outline:` | Available for checkout via WebCheckout |
| `:material-access-point:` | Standalone (no PC required) |
| `:material-link-variant:` | Wired / PC-tethered |

---

## Adding a Keralia Training

Training pages follow a specific naming and header convention. Use an existing training as a template.

### Step 1: Create the File

1. Navigate to `docs/trainings/` in GitHub
2. Click **"Add file" → "Create new file"**
3. Name it using the pattern: `topic-specific-tool.md` (e.g., `360-camera-gopro-max-video-editing.md`)

### Step 2: Use the Training Template

```yaml
---
tags:
  - Keralia Training
  - 360 Video           # Add relevant topic tags
date: 2026-01-23        # Date from training document (MMDDYY → YYYY-MM-DD)
version: "1.0"
---
```

```markdown
# Training Title – Specific Tool Name

<div class="training-header">
  <div class="training-title-row">
    <span class="tag tag-keralia">Keralia Training</span>
    <span class="badge-duration">&#x1F552; 60 mins</span>
  </div>
  <div class="training-meta">
    <span>&#x1F4C5; Dated: 01/23/26</span>
    <span>&middot;</span>
    <span>v1.0</span>
  </div>
</div>

---

## Learning Objectives
- ...

## Learning Outcomes
- ...

## Learning Deliverable
- ...

---

## Overview
(Step-by-step instructions here)
```

**Key fields:**

- **Title**: `Topic – Specific Tool` (e.g., `360 Camera Use – GoPro Max Video Editing`)
- **Duration**: Update the `60 mins` in `badge-duration` to match the training length
- **Date**: Use the `MMDDYY` date from the training document header, formatted as `MM/DD/YY`

### Step 3: Add to Navigation

Edit `mkdocs.yml` and add your training under the `Keralia Trainings` section:

```yaml
nav:
  - Keralia Trainings:
      - Overview: trainings/overview.md
      - Your Training Title: trainings/your-training-file.md  # ← Add here
```

Also add it to the list in `trainings/overview.md`.

---

## Markdown Basics

The wiki uses Markdown, a simple formatting language:

### Text Formatting

```markdown
**bold text**
*italic text*
[Link text](https://example.com)
```

### Headings

```markdown
# Main Title
## Section
### Subsection
```

### Lists

```markdown
- Bullet point
- Another point

1. Numbered item
2. Second item
```

### Tables

```markdown
| Column 1 | Column 2 |
|----------|----------|
| Data     | Data     |
```

### Images

```markdown
![Alt text](../images/filename.jpg)
```

### Info Boxes

```markdown
!!! info "Title"
    This is an info box.

!!! warning "Caution"
    This is a warning box.
```

---

## Adding Images

### Step 1: Upload the Image

1. Go to `docs/images/` in GitHub
2. Click **"Add file" → "Upload files"**
3. Drag your image and commit

### Step 2: Reference in Your Page

```markdown
![Description](../images/your-image.jpg)
```

!!! tip "Image Tips"
    - Use descriptive filenames: `quest-3-setup.jpg` not `IMG_1234.jpg`
    - Compress large images before uploading (use [TinyPNG](https://tinypng.com))
    - Recommended formats: `.jpg` for photos, `.png` for screenshots/diagrams

---

## Adding a New Page

### Step 1: Create the File

1. Navigate to the appropriate folder in `docs/`
2. Click **"Add file" → "Create new file"**
3. Name it `your-page-name.md`
4. Add your content and commit

### Step 2: Add to Navigation

Edit `mkdocs.yml` and add your page to the `nav:` section:

```yaml
nav:
  - Resource Guide:
      - Overview: equipment/overview.md
      - Your New Page: equipment/your-page-name.md  # ← Add here
  - Keralia Trainings:
      - Overview: trainings/overview.md
      - Your Training: trainings/your-training.md   # ← Or here
  - Policies:
      - ...
```

---

## Common Tasks

| Task | How |
|------|-----|
| Fix a typo | Edit the `.md` file directly |
| Update equipment info | Edit the relevant page in `equipment/` |
| Add a new headset | Edit the appropriate headset page (e.g., `equipment/vr-headsets.md`) |
| Add a new training | Create `.md` in `trainings/`, add to `mkdocs.yml` (see template above) |
| Change lab hours | Edit `about/contact-hours.md` |
| Add a new policy | Create `.md` in `policies/`, add to `mkdocs.yml` |
| Browse by topic | Visit the [Tags](tags.md) page |

---

## Need Help?

- **Markdown Guide:** [markdownguide.org](https://www.markdownguide.org/basic-syntax/)
- **MkDocs Documentation:** [mkdocs.org](https://www.mkdocs.org)
- **Material Theme Features:** [squidfunk.github.io/mkdocs-material](https://squidfunk.github.io/mkdocs-material)

Or contact: **camdimmersivemedialab@northeastern.edu**
