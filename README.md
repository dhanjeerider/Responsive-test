# Responsive Device Studio

A lightweight **responsive website tester**, **mobile viewport preview tool**, and **device mockup simulator** built for quickly checking how a website looks across phones, tablets, desktops, and custom screen sizes.

This project focuses on a simple workflow:

- enter a URL
- pick a device
- preview the page inside a device frame
- switch frame on/off
- rotate portrait/landscape
- zoom and pan the preview
- open a direct screenshot API URL in **PNG** or **JPG**
- record the visible stage for demos

If you want a **single HTML responsive testing tool** for your repo, this project is designed for that.

---

## Why this project

Most responsive testing demos are either:

- too heavy
- too generic
- broken on mobile
- dependent on browser extensions
- not easy to share as a single file

**Responsive Device Studio** is built to be:

- fast to open
- easy to understand
- demo-friendly
- repo-friendly
- SEO-friendly for GitHub discoverability
- usable as a real responsive preview screen

---

## Core features

### Responsive website preview

- test any public URL
- preview websites in device-sized viewports
- quickly reload the current page preview

### Real device frame support

- uses **remote device mockup image URLs** from WebMobileFirst
- overlays website screenshots inside phone, tablet, desktop, and watch frames
- frame mode for presentation-style previews
- frame-off mode for clean viewport previews

### Screenshot API integration

- generates preview images using the screenshot API:
  - `https://shot.dktczn.workers.dev/api/screenshot`
- choose:
  - **current height** screenshot
  - **full page** screenshot
  - **JPG** export
  - **PNG** export
- opens the direct API screenshot URL instantly

### Device testing controls

- portrait mode
- landscape mode
- zoom in
- zoom out
- background toggle
- drag / pan the preview area

### Device selection panel

- browse grouped device lists
- device images in the chooser
- search devices quickly
- select devices from Apple, Android, tablets, and specials

### Custom devices

- create your own custom device
- set device name, width, height, and type
- save custom devices in local browser storage
- reuse custom devices later

### Recording support

- record the visible stage
- export the screen recording from the preview area
- useful for bug reports, product demos, and client walkthroughs

### Single-file friendly

- main experience available as a **single HTML file**
- good for quick demos, lightweight hosting, and sharing in repositories

---

## Current UI layout

The current interface is designed around a compact productivity layout:

- **top single-line URL bar**
- **left thin vertical toolbar**
- **center preview stage**
- **right device chooser panel**

This makes it easy to use on both desktop and mobile-width layouts.

---

## Best use cases

This repo is useful for:

- responsive design testing
- mobile website preview
- landing page QA
- client demos
- device frame mockups
- screenshot generation workflows
- quick viewport checks
- front-end review
- design handoff previews
- product showcase recordings

---

## Supported interactions

### Preview actions

- load website URL
- reload preview
- rotate viewport
- switch frame on/off
- zoom preview
- drag the preview canvas

### Screenshot actions

- choose current-height capture
- choose full-page capture
- choose PNG
- choose JPG
- open direct screenshot API URL

### Recording actions

- start recording stage
- stop recording stage
- export video file

---

## How it works

This project does **not rely on live iframe rendering** for the main preview flow.

Instead, it uses a screenshot-based approach for better reliability:

1. user enters a URL
2. project requests a screenshot from the screenshot API
3. returned image is placed inside the selected device frame
4. controls allow zoom, rotate, pan, and export

This avoids common iframe issues like:

- blank white pages
- blocked embeds
- `X-Frame-Options` problems
- CSP restrictions

---

## Device source and credits

Device mockup references are sourced from:

- https://www.webmobilefirst.com/en/mockups/

This project uses remote mockup image URLs for the frame layer.

---

## Project structure

```text
project/
├─ public/
│  ├─ single.html          # main single-file responsive testing UI
│  ├─ index.html           # earlier app shell version
│  └─ data/
│     └─ devices.json      # device metadata
├─ scripts/
│  ├─ scrape_devices.py
│  ├─ add_landscape_masks.py
│  ├─ build_single_html.py
│  ├─ build_premium_single_html.py
│  └─ build_focus_single_html.py
├─ server.mjs              # lightweight local server
└─ README.md
```

---

## Run locally

### Start the local server

```bash
node server.mjs
```

Then open:

```text
http://localhost:3000/single.html
```

---

## Recommended file to use

For the latest compact responsive tester UI, use:

- `public/single.html`

---

## Keywords this repo targets naturally

These are the kinds of searches this repository is relevant for:

- responsive tester
- responsive website tester
- mobile responsive test tool
- device frame website preview
- website preview in phone mockup
- responsive web design checker
- viewport testing tool
- website screenshot preview tool
- mobile website preview generator
- responsive testing single html

---

## SEO notes for your repository

To help this repo perform better on GitHub and Google:

### 1. Use a clear repo name

Example:

- `responsive-device-studio`
- `responsive-website-tester`
- `mobile-preview-device-mockup`

### 2. Add a strong GitHub description

Example:

> Responsive website tester with device mockup preview, screenshot API support, custom devices, zoom, rotate, and recording in a single HTML app.

### 3. Add topic tags

Suggested GitHub topics:

- responsive-design
- responsive-testing
- mobile-preview
- screenshot-api
- device-mockup
- frontend-tools
- web-testing
- single-html
- viewport-testing
- ui-testing

### 4. Keep README keyword-rich but natural

This README is written to help with discoverability while still reading like real documentation.

---

## Limitations

- preview is screenshot-based, not a full live browser engine
- some websites may load slowly depending on screenshot API response time
- recording captures the stage view, not a real remote browser session
- remote frame image availability depends on source URLs staying available

---

## Roadmap ideas

Possible future improvements:

- multi-device side-by-side comparison mode
- custom device edit/delete UI
- saved device presets
- direct share links
- better touch gestures on mobile
- per-device zoom persistence
- screenshot history panel
- dark/light UI themes

---

## Who is this for?

- front-end developers
- UI designers
- agencies
- freelancers
- QA testers
- founders preparing demos
- anyone needing a simple responsive testing repo

---

## License / attribution

Use the project according to the licenses and terms of any external resources you depend on, including remote device mockup assets and screenshot providers.

If you plan to publish commercially, review the source asset terms first.

---

## Summary

**Responsive Device Studio** is a compact, single-file-friendly, repo-ready tool for:

- responsive website testing
- mobile device preview
- screenshot-based layout checking
- phone frame and no-frame presentation
- custom viewport testing
- screenshot API export
- stage recording

If you want a clean **responsive test repo** that is easy to demo and easy to describe in search, this README is optimized for that use case.
