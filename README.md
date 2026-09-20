<div align="center">

  <br />

  <img src="assets/soul-os-title.svg" alt="Soul OS" width="460" />

  <p><b><em>macOS polish, Windows familiarity, and Linux freedom — in one fluid web OS.</em></b></p>

  <br />

  [![Live Preview](https://img.shields.io/badge/Live_Demo-akshat96af.github.io%2FSoulOS-4d5643?style=for-the-badge&logo=googlechrome&logoColor=white)](https://akshat96af.github.io/SoulOS/)
  [![React 19](https://img.shields.io/badge/React-19-149eca?style=for-the-badge&logo=react&logoColor=white)](https://react.dev/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5.7-3178c6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
  [![Vite](https://img.shields.io/badge/Vite-6.0-646cff?style=for-the-badge&logo=vite&logoColor=white)](https://vite.dev/)
  [![Motion](https://img.shields.io/badge/Motion-12-0055ff?style=for-the-badge&logo=framer&logoColor=white)](https://motion.dev/)
  [![Zustand](https://img.shields.io/badge/Zustand-5.0-443e38?style=for-the-badge)](https://zustand-demo.pmnd.rs/)

  <br />

  <p align="center">
    <b>
      <a href="https://akshat96af.github.io/SoulOS/">Launch Live Experience</a>
      &nbsp;&bull;&nbsp;
      <a href="#interface-overview">Interface</a>
      &nbsp;&bull;&nbsp;
      <a href="#built-in-applications">Applications</a>
      &nbsp;&bull;&nbsp;
      <a href="#core-capabilities">Capabilities</a>
      &nbsp;&bull;&nbsp;
      <a href="#system-architecture">Architecture</a>
      &nbsp;&bull;&nbsp;
      <a href="#author">Author</a>
    </b>
  </p>

  <br />

  <img src="assets/preview%201.png" alt="Soul OS Desktop Interface" width="100%" style="border-radius: 12px; box-shadow: 0 24px 48px rgba(0, 0, 0, 0.2);" />

</div>

<br />

---

## Overview

> *"Technology should leave you room to breathe."*

Soul OS reimagines desktop computing for the browser — combining native window management with zero-install accessibility.

- **Tactile**: Continuous proximity dock magnification, spring physics, and edge snapping.
- **Private**: 100% client-side. Zero tracking, zero telemetry, local persistence.
- **Unified**: macOS aesthetic craft, Windows workflow familiarity, and Linux autonomy.

<br />

---

## Interface Overview

<div align="center">

| Desktop Environment | Entrance & Lock Screen |
|:---:|:---:|
| [![Desktop](assets/preview%201.png)](assets/preview%201.png) | [![Lock Screen](assets/preview%202.png)](assets/preview%202.png) |
| *Top system bar, weather widget, and magnetic dock.* | *Atmospheric entrance surface with session initialization.* |

| Multitasking & Window Stacking | System Settings & Personalization |
|:---:|:---:|
| [![Multitasking](assets/preview%203.png)](assets/preview%203.png) | [![Settings](assets/preview%204.png)](assets/preview%204.png) |
| *Edge snapping, z-stacking, and active dock scaling.* | *Appearance themes, sound controls, and developer notes.* |

</div>

<br />

---

## Built-in Applications

| Icon | Application | Purpose | Highlights |
|:---:|:---|:---|:---|
| <img src="assets/icons/files.svg" width="34" alt="My PC" /> | **My PC (Files)** | Virtual filesystem | Breadcrumb pathing, search, grid/list view, trash recovery, and local file import. |
| <img src="assets/icons/notes.svg" width="34" alt="Notes" /> | **Notes** | Minimalist editor | Multi-note indexing, instant local auto-save, and live word counting. |
| <img src="assets/icons/gallery.svg" width="34" alt="Gallery" /> | **Gallery** | Image curator | Variable zoom (50%–300%), carousel navigation, and one-click wallpaper setting. |
| <img src="assets/icons/video.svg" width="34" alt="Video" /> | **Video** | Media player | Zero-upload local video playback with automatic memory cleanup. |
| <img src="assets/icons/calculator.svg" width="34" alt="Calculator" /> | **Calculator** | Desktop math utility | Precision arithmetic, percentage evaluation, and full keyboard entry. |
| <img src="assets/icons/browser.svg" width="34" alt="Browser" /> | **Browser** | Web portal | Smart address detection, search engine fallback, and external launch tabs. |
| <img src="assets/icons/settings.svg" width="34" alt="Settings" /> | **Settings** | Control hub | Visual themes, wallpaper gallery, dock scaling, audio volume, and preferences. |

<br />

---

## Core Capabilities

- **Magnetic Proximity Dock**: Smooth mathematical scale curve calculated across neighboring icons with launch bounce physics.
- **Window Management**: Boundary-constrained dragging, dynamic z-index focus stacking, and 3-way split/maximize snapping.
- **Workspaces**: 3 isolated virtual spaces with on-the-fly window reassignment.
- **Spotlight Search**: Global <kbd>Ctrl</kbd> / <kbd>Cmd</kbd> + <kbd>K</kbd> palette indexing apps, files, and system settings.
- **Control Center**: Grouped toggles for Wi-Fi, Bluetooth, Focus Mode, brightness, master volume, and battery telemetry.
- **Acoustic Feedback**: Centralized Web Audio service providing discrete cues for window events, clicks, and errors.
- **Curated Themes**: 8 bespoke photographic sceneries with light/dark adaptive balance.

<br />

---

## Keyboard Shortcuts

| Key Combination | Action |
|:---|:---|
| <kbd>Ctrl</kbd> / <kbd>Cmd</kbd> + <kbd>K</kbd> | Toggle Spotlight Search |
| <kbd>Ctrl</kbd> + <kbd>`</kbd> &nbsp;or&nbsp; <kbd>Alt</kbd> + <kbd>Tab</kbd> | Cycle focus between active windows |
| <kbd>Esc</kbd> | Dismiss active panel, overlay, or context menu |
| <kbd>Enter</kbd> / <kbd>=</kbd> | Calculate expression in Calculator |
| <kbd>Double Click</kbd> | Open folder or launch file in associated app |

<br />

---

## System Architecture

Modular, decoupled architecture with strict type safety and zero external runtime services:

```
src/
|-- core/                  # Headless Services & State Stores
|   |-- windows.ts         # Window manager, z-indexing, edge snapping & workspaces
|   |-- settings.ts        # Persisted settings with automated migration schema (v1-v6)
|   |-- filesystem.ts      # Virtual filesystem tree & file associations
|   |-- sound.ts           # Central Web Audio acoustic feedback service
|   |-- motion.ts          # Spring motion configs & reduced-motion queries
|   |-- battery.ts         # Web Battery Status API integration
|   |-- registry.ts        # App manifests & wallpaper metadata
|   `-- shortcuts.ts       # Global keyboard event dispatcher
|
|-- shell/                 # Desktop Shell & Composites
|   |-- Desktop.tsx        # Master desktop canvas & context menus
|   |-- TopBar.tsx         # System status bar & panel anchors
|   |-- Dock.tsx           # Continuous proximity magnetic dock
|   |-- Window.tsx         # Resizable window frames & spatial transitions
|   |-- ControlCenter.tsx  # Quick settings and sliders
|   |-- Search.tsx         # Spotlight command palette
|   |-- Workspaces.tsx     # Virtual desktop switcher
|   |-- StatusPanels.tsx   # Clock, date, and battery subpanels
|   `-- Boot.tsx           # Entrance view & session initialization
|
|-- apps/                  # Sandboxed Application Suite
|   |-- Files.tsx          # Virtual file manager with trash & imports
|   |-- Notes.tsx          # Local notepad with real-time save
|   |-- Gallery.tsx        # Image showcase & wallpaper switcher
|   |-- Video.tsx          # Blob-based video player
|   |-- Calculator.tsx     # Arithmetic engine with keyboard support
|   |-- Browser.tsx        # Web query interface & external launcher
|   `-- Settings.tsx       # System preferences & developer notes
|
`-- styles.css             # Design tokens & glassmorphic materials
```

### Tech Stack
- **React 19 & TypeScript 5.7**: Strict component hierarchy and typed interfaces.
- **Zustand 5**: Multi-store state management with local schema migrations.
- **Motion 12**: Continuous spring dynamics and reduced-motion compliance.
- **react-rnd**: Controlled geometric dragging and resizing bounds.
- **Lucide Icons**: Uniform SVG iconography.
- **Typography**: Variable distributions of DM Sans and Manrope.

<br />

---

## Source Code & Deployment

> [!NOTE]
> The source codebase and build pipelines for **Soul OS** are maintained in a **private repository** for portfolio showcase.
>
> The fully compiled, interactive desktop application is deployed live at:  
> **[https://akshat96af.github.io/SoulOS/](https://akshat96af.github.io/SoulOS/)**

<br />

---

## Author

<table style="border: none;">
  <tr>
    <td width="90" align="center" valign="middle">
      <img src="https://github.com/akshat96af.png" width="80" style="border-radius: 50%;" alt="Akshat" />
    </td>
    <td>
      <h3>Akshat</h3>
      <p><em>UI Developer &bull; Creator of Soul OS</em></p>
      <p>
        <a href="https://github.com/akshat96af">GitHub</a>
        &nbsp;&bull;&nbsp;
        <a href="https://instagram.com/_.a.k.s.h.a.t._">Instagram</a>
        &nbsp;&bull;&nbsp;
        <a href="https://akshat96af.github.io/SoulOS/">Live Preview</a>
      </p>
    </td>
  </tr>
</table>

<br />

---

<div align="center">
  <p><b>Room to think. Space to be.</b></p>
  <p><sub>Designed and developed by <a href="https://github.com/akshat96af">Akshat</a> &bull; Soul OS Edition 01</sub></p>
</div>
