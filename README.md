# iPhone Duo New Status Icon

A lightweight, responsive recreation of the new iPhone Duo status icon, built entirely with HTML and CSS. The icon combines battery level, Wi-Fi connectivity, and cellular signal strength into one circular status indicator, inspired by Apple's iPhone Duo design.

This is an independent visual recreation for the web, not an official Apple asset or implementation. Learn more about the iPhone Duo status bar in [Apple's announcement](https://www.apple.com/newsroom/2026/09/apple-unveils-iphone-duo/).

## Live Demo

Visit the deployed website on [Cloudflare Pages](https://ebfcf0df.combined-status-bar-icon.pages.dev).

## Features

- Pure HTML and CSS — no JavaScript, build tools, or dependencies.
- Animated battery charge cycle.
- Animated Wi-Fi connection strength.
- Four cellular signal dots that fade in sequence.
- Pause animation control.
- Responsive layout for desktop and mobile screens.
- Respects the user's `prefers-reduced-motion` setting.
- Scales the icon proportionally through CSS custom properties.

## Getting Started

No installation is required. Open [`index.html`](./index.html) directly in a modern browser.

For a local development server, run any static file server from the project directory. For example:

```bash
npx serve .
```

Then open the local URL shown in the terminal.

## Project Structure

```text
.
└── index.html    # Page markup, styles, animation, and responsive layout
```

## How It Works

The icon is composed from positioned HTML elements and CSS masks:

- The battery uses a conic gradient combined with radial masks to create a rounded open ring.
- The Wi-Fi symbol uses two clipped concentric arcs and a rotated quarter-circle point.
- The cellular indicator uses four circular elements with independent opacity animations.
- The animation timeline is controlled by the `--duration` custom property.

## Customization

The main visual settings are defined in `:root` inside `index.html`:

```css
:root {
  --icon-size: clamp(136px, 19vw, 184px);
  --wifi-scale: 1.2;
  --ink: #111112;
  --paper: #e7e7e9;
  --duration: 8s;
  --muted: .16;
}
```

Adjust these values to change the icon size, colors, animation speed, and inactive signal opacity.

## Browser Compatibility

The demo uses modern CSS features including `@property`, CSS trigonometric functions, `mask-image`, `mask-composite`, `clip-path`, and `:has()`. Use a current version of Chrome, Edge, Safari, or Firefox for the best results.

## Limitations

This is a visual web simulation. It does not read live device battery, Wi-Fi, or cellular data, and it does not modify the native iPhone status bar.

## License

No license has been specified for this project yet.
