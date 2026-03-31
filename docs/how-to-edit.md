---
tags:
  - Guide
date: 2026-03-30
version: "1.0"
---

# How to Edit This Wiki

<div class="page-meta">
  <span class="meta-date">Last updated: 2026-03-30 &middot; v1.0</span>
  <span class="tag">Guide</span>
</div>

This guide explains how to update the XRIML Wiki. **No coding experience required** — you can edit everything directly in your web browser.

## Quick Edits (Browser Only)

### Step 1: Go to the GitHub Repository

Navigate to: `https://github.com/yourusername/xriml-wiki`

### Step 2: Find the File to Edit

All content lives in the `docs/` folder:

```
docs/
├── index.md              ← Homepage
├── about/
│   └── about-the-lab.md
├── spaces/
│   ├── testing-room.md
│   └── ...
├── equipment/
│   ├── vr-headsets.md
│   └── ...
└── images/               ← All images go here
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
date: 2026-03-30        # Update when content changes
version: "1.1"          # Bump version on updates
---
```

Then add the visual banner after the `# Title`:

```html
<div class="page-meta">
  <span class="meta-date">Last updated: 2026-03-30 &middot; v1.1</span>
  <span class="tag">Equipment</span>
  <span class="tag">VR</span>
  <span class="tag tag-keralia">Keralia Training</span>
</div>
```

Use `class="tag tag-keralia"` for the special Keralia Training tag (gold styling).

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
  - Equipment:
      - Overview: equipment/overview.md
      - VR Headsets: equipment/vr-headsets.md
      - Your New Page: equipment/your-page-name.md  # ← Add here
```

---

## Common Tasks

| Task | How |
|------|-----|
| Fix a typo | Edit the `.md` file directly |
| Update equipment specs | Edit the relevant page in `equipment/` |
| Add a new headset | Edit `equipment/vr-headsets.md` or create new page |
| Change lab hours | Edit `about/contact-hours.md` |
| Add a new policy | Create new `.md` in `policies/`, add to `mkdocs.yml` |
| Browse by topic | Visit the [Tags](tags.md) page |

---

## Need Help?

- **Markdown Guide:** [markdownguide.org](https://www.markdownguide.org/basic-syntax/)
- **MkDocs Documentation:** [mkdocs.org](https://www.mkdocs.org)
- **Material Theme Features:** [squidfunk.github.io/mkdocs-material](https://squidfunk.github.io/mkdocs-material)

Or contact: [Add lab manager contact]
