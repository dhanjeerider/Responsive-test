# Responsive Device Studio

[![Responsive Web Testing](https://img.shields.io/badge/Responsive-Web%20Testing-5fa7ff?style=for-the-badge)](https://github.com/dhanjeerider/Responsive-test)
[![Single HTML App](https://img.shields.io/badge/Single%20HTML-App-57d98d?style=for-the-badge)](https://github.com/dhanjeerider/Responsive-test/blob/main/index.html)
[![License](https://img.shields.io/badge/license-review%20external%20assets-lightgrey?style=for-the-badge)](https://github.com/dhanjeerider/Responsive-test)

**Responsive Device Studio** is a lightweight, browser-based **responsive website tester** and **mobile viewport preview tool**. Enter any public website URL, select a phone, tablet, desktop, or watch viewport, and inspect the result inside a device mockup.

It is designed as a fast, shareable **single-file HTML responsive testing tool** for frontend developers, UI designers, QA testers, agencies, freelancers, and product teams.

![Responsive website testing and device preview](https://img.shields.io/badge/Preview-phone%20%7C%20tablet%20%7C%20desktop%20%7C%20watch-7f83ff?style=flat-square)

## Why use Responsive Device Studio?

Testing a website at only one screen size can hide layout, navigation, and typography problems. This tool makes it easy to check a public URL across realistic device sizes before publishing or sharing a design.

- Preview websites in responsive phone, tablet, desktop, and watch viewports
- Compare portrait and landscape layouts
- Use realistic device mockup frames or a clean frame-free viewport
- Zoom, pan, reload, and switch the preview background
- Generate PNG or JPG screenshots through the integrated screenshot API
- Create and save custom device presets in browser local storage
- Record the visible preview stage for demos, bug reports, and walkthroughs
- Use the app directly from one HTML file with no build step

## Features

### Responsive website preview

- Enter a URL such as `https://example.com`
- Load a website in a device-sized preview
- Open the target URL in a new browser tab
- Reload the preview whenever the page changes

### Device mockup testing

- Apple and Android phone presets
- Tablet, desktop, and smartwatch presets
- Device search and grouped device selection
- Portrait and landscape orientation
- Frame on/off mode for mockup presentations or clean viewport testing

### Screenshot and recording tools

- Current-height screenshot capture
- Full-page screenshot capture
- PNG and JPG export options
- Direct screenshot API URL generation
- Visible-stage screen recording for product demos and QA notes

### Custom viewport presets

Create a custom device by specifying:

- Device name
- Viewport width
- Viewport height
- Device type: phone, tablet, desktop, or watch

Custom devices are saved locally in your browser and can be reused later.

## How it works

1. Enter a public website URL.
2. Choose a device and viewport size.
3. Select portrait or landscape mode.
4. Inspect the page inside the responsive preview.
5. Use the screenshot or recording controls when you need an export.

The preview uses a live iframe when the target website permits embedding. If a website blocks iframe rendering with security headers such as `X-Frame-Options` or a restrictive CSP, use the **Open tab** option or the screenshot export workflow instead.

## Run locally

This project has no dependency installation or build process.

### Option 1: Open the HTML file

Open [`index.html`](./index.html) directly in a modern browser.

### Option 2: Use a local server

```bash
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000/
```

A local server is recommended when testing browser features such as iframe loading and screen recording.

## Project structure

```text
Responsive-test/
├── index.html   # Complete responsive device testing application
├── style.css    # Reserved stylesheet entry
└── README.md    # Documentation and usage guide
```

Most of the current interface, responsive layout, device data, and application logic are contained in `index.html`, which keeps the project easy to download, customize, and deploy.

## Screenshot API

Screenshot exports use the following endpoint:

```text
https://shot.dktczn.workers.dev/api/screenshot
```

The app builds the request with the selected URL, viewport width and height, output format, scale, user agent, and full-page option. Availability and response time may depend on the target website and the external screenshot service.

## Best use cases

- Responsive web design testing
- Mobile website preview
- Website viewport checking
- Landing page QA
- Frontend and UI review
- Device mockup presentations
- Client demos and design handoffs
- Screenshot-based bug reports
- Product showcase recordings
- Quick cross-device layout checks

## SEO and accessibility notes

This repository is relevant to searches such as:

- responsive website tester
- responsive design testing tool
- mobile responsive checker
- website preview on phone mockup
- device viewport testing
- responsive web design checker
- mobile website preview tool
- screenshot-based responsive testing
- single HTML responsive tester
- frontend responsive QA tool

The interface includes a viewport meta tag, semantic page sections, descriptive controls, device image alt text, keyboard-accessible buttons, and responsive layouts for smaller screens.

## Limitations

- A target website may block iframe previews.
- Screenshot quality and speed depend on the external screenshot API.
- Recording captures the visible local preview stage, not a remote browser session.
- Remote device frame assets may change or become unavailable.
- Only public URLs that the browser or screenshot service can access can be tested.

## Credits and external resources

Device mockup frame references are loaded from [WebMobileFirst mockups](https://www.webmobilefirst.com/en/mockups/). Please review the source terms before using the assets in a commercial product.

## Contributing

Suggestions and improvements are welcome. Useful contributions include new device presets, better mobile interactions, side-by-side comparison, saved share links, screenshot history, and accessibility improvements.

1. Fork the repository.
2. Create a feature branch.
3. Test the change in a modern browser.
4. Open a pull request with a clear description and screenshots when relevant.

## License

Review the license and terms of all external device images and screenshot services before redistributing or using this project commercially.

---

**Responsive Device Studio** is a simple, fast, and shareable way to test responsive websites across multiple device sizes without installing a heavy browser extension or design application.
