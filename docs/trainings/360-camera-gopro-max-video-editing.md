---
tags:
  - Keralia Training
  - 360 Video
  - GoPro
  - Adobe Premiere
date: 2026-01-23
version: "1.0"
---

# 360 Camera Use – GoPro Max Video Editing

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

- How to import 360 footage and convert them to be used in Adobe Premiere to edit a basic 360 video for web/VR.

## Learning Outcomes

- Ingesting footage to convert for editing and being able to learn how to edit a basic 360 video in Premiere.

## Learning Deliverable

- Export a 360 video with other non-360 video content such as text and/or 2D content.

---

## Overview

### 1. Install GoPro Player

- Open the Microsoft Store and install the **"GoPro Player"** app. The icon to download and install will say **"Get"** if it needs to be downloaded, or **"Open"** if it's already installed.

### 2. Converting GoPro Footage

1. Launch the GoPro Player app.
2. Open your project folder and go to the footage folder where the GoPro media is located. **Drag and drop** the media (file type `.360`) into the GoPro Player.
3. Once the preview is loaded, export the video by going to **File > Export**. Export it to the same folder where the original file is located. The exported file will be in `.MP4` so you don't need to add an additional extension, but it can be helpful to add **"converted"** to the file name to easily identify the exported video.
4. Repeat for all `.360` videos.

### 3. Setting up Premiere Pro Project

1. Launch Premiere.
2. Create a new project and save it in the Project Folder. Below is the recommended folder structure:

```
Project Folder (Name of Project)
├── Footage/
│   └── GoPro Media/    ← Copy the entire folder from camera
├── Exports/            ← For exported media from Premiere
└── Premiere Project/   ← Same name as Project Folder
```

3. If needed, change the workspace for Premiere to **"Editing."**
4. Import the Footage folder into Premiere. The bin structure in Premiere should mirror the Project folder structure.

### 4. Creating 360 Sequence/Timeline

1. In the project window, create a new item called **"Sequence."** Make sure it's not created in any of the bins.
2. Drag and drop the entire **"Footage"** folder into the sequence timeline so that you can see the video and audio clips.

---

!!! tip "Related Resources"
    - [360 Cameras](../equipment/360-cameras.md) — Available 360 cameras in the lab
    - [360 Accessories](../equipment/360-accessories.md) — Tripods, mounts, and audio gear
    - [Equipment Checkout](../policies/equipment-checkout.md) — How to check out a GoPro Max
