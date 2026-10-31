<p>
  <a href="https://slowpixel.dev">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/slowpixel-dev/.github/main/profile/slowpixel-logo-dark.svg">
      <img alt="SlowPixel" src="https://raw.githubusercontent.com/slowpixel-dev/.github/main/profile/slowpixel-logo.svg" height="56">
    </picture>
  </a>
</p>

**E-ink displays that AI agents write to over MCP.**
Claude, ChatGPT, Hermes or any MCP client sends structured content; the display lays it out, checks that it fits and redraws slowly and calmly.

**CS:** E-ink displej, na který píšou AI agenti přes MCP. Agent pošle obsah, displej si ho rozvrhne a v klidu překreslí.

🌐 **[slowpixel.dev](https://slowpixel.dev)** · 📖 [Documentation](https://slowpixel.dev/dokumentace) · 🧩 [Modules](https://slowpixel.dev/moduly) · 🤖 [Connecting an agent](https://slowpixel.dev/navod)

## What it does

- **Agents write, the display lays out.** Zones (header, main, sidebar, footer) with text, lists, tables, charts, calendars, photos, clocks, QR codes and what is playing (Spotify, Kodi); every call reports whether it fits.
- **Rendered on the device.** One layout engine next to the panel; the cloud only relays MCP calls and never keeps the content.
- **Modules** fetch live values (weather, an HTTP JSON source, a script, a check of a web, port or ping) or run in JavaScript in a sandbox; a public catalog shares them.
- **The dashboard** pairs a display by its QR code, shows a live preview of the panel, sets templates, photos, calendars, monitoring with e-mail alerts, sharing with the family and the system's updates.
- **A kit**: a Raspberry Pi Zero 2 W, a 7.5" Good Display panel (800 × 480, four greys), a USB-C supply and one button that switches the display off and on, its LED dimmable from the dashboard.

## Projects

| | |
|---|---|
| **slowpixel-cloud** | [slowpixel.dev](https://slowpixel.dev): accounts, pairing, the dashboard, the catalog of modules, OAuth for agents and the MCP relay between agents and displays (TypeScript, React, Postgres). |
| **slowpixel-device** | The daemon next to the panel, in Zig: one static binary that lays out content, drives the e-ink panel (partial refreshes, greys), runs the modules and links to the cloud. |
| **slowpixel-os** | SlowPixel OS: the display's operating system (Yocto) for the Raspberry Pi 5, Zero 2 W and Zero W, with the daemon built in, WiFi set up from a phone, and signed A/B updates on a development and a stable channel. |

The repositories are private for now. Start at [slowpixel.dev](https://slowpixel.dev) and its user documentation.
