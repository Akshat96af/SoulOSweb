<div align="center">

  <br />

  # Soul OS
  ### *macOS polish, Windows familiarity, and Linux freedom — in one fluid web OS.*

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
      &nbsp;&nbsp;&bull;&nbsp;&nbsp;
      <a href="#interface-overview">Interface Overview</a>
      &nbsp;&nbsp;&bull;&nbsp;&nbsp;
      <a href="#built-in-applications">Built-in Applications</a>
      &nbsp;&nbsp;&bull;&nbsp;&nbsp;
      <a href="#core-capabilities">Core Capabilities</a>
      &nbsp;&nbsp;&bull;&nbsp;&nbsp;
      <a href="#system-architecture">Architecture</a>
      &nbsp;&nbsp;&bull;&nbsp;&nbsp;
      <a href="#author">Author</a>
    </b>
  </p>

  <br />

  <img src="assets/preview%201.png" alt="Soul OS Desktop Interface" width="100%" style="border-radius: 12px; box-shadow: 0 24px 48px rgba(0, 0, 0, 0.2);" />

</div>

<br />

---

## Design Philosophy

> *"A little space to make your own. Built around a simple idea: technology should leave you room to breathe."*

**Soul OS** is a browser-based desktop operating system environment designed to explore human-centric desktop interaction on the modern web. Developed by **[Akshat](https://github.com/akshat96af)**, the environment combines the tactility and structure of traditional window-managed computing with the accessibility and fluidity of web technologies.

The project is guided by three principles:
- **Calm by Default**: Ambient glassmorphism, disciplined typographic scales, muted contrast levels, and restrained system acoustics.
- **Continuous Fluidity**: Proximity-scaled magnetic dock physics, fluid window snapping mechanics, and spring-smoothed state transitions.
- **Client-Side Autonomy**: Zero runtime services, tracking, or remote databases. All user configurations, notes, and file structures persist locally and privately within the browser.

<br />

---

## Interface Overview

<div align="center">

| Desktop Environment | Entrance and Lock Screen |
|:---:|:---:|
| [![Desktop](assets/preview%201.png)](assets/preview%201.png) | [![Lock Screen](assets/preview%202.png)](assets/preview%202.png) |
| *Desktop canvas featuring system status bar, weather widget, and magnetic floating dock.* | *Atmospheric entrance surface with system time display and personal session initialization.* |

| Multitasking and Window Stacking | System Settings and Preferences |
|:---:|:---:|
| [![Multitasking](assets/preview%203.png)](assets/preview%203.png) | [![Settings](assets/preview%204.png)](assets/preview%204.png) |
| *Active window management, edge snapping, Notes, Files, and magnetic dock hover scaling.* | *System configuration suite covering display parameters, acoustics, themes, and developer notes.* |

</div>

<br />

---

## Built-in Applications

Soul OS includes a suite of native web applications engineered to operate independently within the desktop environment:

| Application | Name | Purpose | Key Capabilities |
|:---|:---|:---|:---|
| <img src="https://raw.githubusercontent.com/lucide-icons/lucide/main/icons/folder.svg" width="20"/> | **My PC (Files)** | Desktop virtual filesystem | Hierarchical folder tree, breadcrumb navigation, real-time file search, grid and list views, folder creation, inline rename, recoverable Trash, and local file import (images, markdown/text, and video). |
| <img src="https://raw.githubusercontent.com/lucide-icons/lucide/main/icons/file-text.svg" width="20"/> | **Notes** | Distraction-free writing environment | Multi-document repository, real-time word counting, local browser persistence, clean typographic layout, and sidebar indexing. |
| <img src="https://raw.githubusercontent.com/lucide-icons/lucide/main/icons/image.svg" width="20"/> | **Gallery** | Image viewer and curator | High-resolution image previewing, variable zoom control (50% to 300%), sequential carousel navigation, and direct wallpaper assignment. |
| <img src="https://raw.githubusercontent.com/lucide-icons/lucide/main/icons/video.svg" width="20"/> | **Video** | Client-side media playback | Zero-upload local video loading, HTML5 playback controls, and automatic object URL memory management. |
| <img src="https://raw.githubusercontent.com/lucide-icons/lucide/main/icons/calculator.svg" width="20"/> | **Calculator** | Desktop computation utility | Standard four-function arithmetic, percentage evaluation, sign inversion, arbitrary precision handling, and full physical keyboard input support. |
| <img src="https://raw.githubusercontent.com/lucide-icons/lucide/main/icons/globe.svg" width="20"/> | **Browser** | Curated web navigation portal | Unified address and query bar, URL validation, search engine fallback, and curated bookmarks launching external tabs without iframe sandbox restrictions. |
| <img src="https://raw.githubusercontent.com/lucide-icons/lucide/main/icons/settings-2.svg" width="20"/> | **Settings** | Configuration and personalization | Visual theme switching, wallpaper selection, dock magnification scaling, volume levels, accessibility toggles, and developer documentation. |

<br />

---

## Core Capabilities

### Magnetic Proximity Dock
- **Continuous Distance Interpolation**: Computes a continuous scaling curve across neighboring icons based on cursor distance, creating natural magnification feedback.
- **Process Feedback**: Independent bounce trajectories upon application launch, running indicator markers, and coordinate-linked minimization transitions.
- **Customizable Layout**: Fine-tune resting dimensions and magnification multipliers within System Settings.

### Window Management Engine
- **Spatial Freedom**: Draggable and resizable windows powered by `react-rnd` with viewport boundary enforcement.
- **Z-Index Stacking**: Dynamic elevation stacking based on focus history, mouse interactions, and keyboard switching.
- **Edge Snapping**: Snap windows to split-screen arrangements (left half, right half, or full display) via edge dragging or the titlebar layout controller.
- **Restoration Memory**: Retains unmaximized coordinates and dimensions across maximize/restore cycles.

### Workspaces
- Three independent virtual desktops (`Space 1`, `Space 2`, `Space 3`).
- Isolated window groups per workspace with seamless cross-workspace window reassignment.

### Spotlight Search
- Global command palette accessible via <kbd>Ctrl</kbd> / <kbd>Cmd</kbd> + <kbd>K</kbd>.
- Instant search indexing across applications, filesystem entries, and preference categories.

### Control Center
- Centralized system panel with quick toggles for simulated Wi-Fi and Bluetooth states.
- Dedicated Focus Mode for suppressing desktop toast notifications.
- Linear sliders for master audio output and display brightness simulation.
- Hardware battery integration utilizing the Web Battery Status API when supported by the host browser.

### Acoustic Feedback System
- Audio cues mapped to system events including window creation, window closure, clicks, and navigation.
- Managed by a centralized Web Audio service with volume normalization, clamping, and complete mute support.

### Curated Visual Themes
- Eight signature photographic sceneries:
  - **Chromatic Tide** (Signature abstract composition)
  - **Azure Shores** (Lake Tahoe alpine shoreline)
  - **Alpenglow** (High-altitude mountain summits)
  - **Sandstone Reverie** (Desert rock formations)
  - **Jade Sanctuary** (Forest lake)
  - **Blue Orbit** (Planetary perspective)
  - **Nocturne** (Night sand dunes)
  - **Rose Mirage** (Horizon gradient)

<br />

---

## Keyboard Shortcuts

| Key Combination | Action |
|:---|:---|
| <kbd>Ctrl</kbd> / <kbd>Cmd</kbd> + <kbd>K</kbd> | Toggle Spotlight Search |
| <kbd>Ctrl</kbd> + <kbd>`</kbd> &nbsp;or&nbsp; <kbd>Alt</kbd> + <kbd>Tab</kbd> | Cycle through open windows in current workspace |
| <kbd>Esc</kbd> | Dismiss active panel, overlay, or context menu |
| <kbd>Enter</kbd> / <kbd>=</kbd> | Compute result in Calculator |
| <kbd>Double Click</kbd> | Open file with associated default handler |

<br />

---

## System Architecture

Soul OS is built with a modular, decoupled architecture focused on frame consistency, strict typing, and zero external runtime dependencies:

```
src/
|-- core/                  # System Services and State Stores
|   |-- windows.ts         # Window manager, z-indexing, snap logic, and workspaces
|   |-- settings.ts        # Persisted settings with automated migration schema (v1-v6)
|   |-- filesystem.ts      # Virtual filesystem tree, node operations, and associations
|   |-- sound.ts           # Central Web Audio API acoustic feedback service
|   |-- motion.ts          # Motion springs, timing curves, and accessibility checks
|   |-- battery.ts         # Web Battery Status API integration
|   |-- registry.ts        # Application definitions, wallpaper metadata, and defaults
|   `-- shortcuts.ts       # Global keyboard event orchestrator
|
|-- shell/                 # Desktop Chrome and Shell Overlays
|   |-- Desktop.tsx        # Top-level desktop environment and context handlers
|   |-- TopBar.tsx         # System status bar, clock, and panel anchors
|   |-- Dock.tsx           # Continuous proximity magnetic dock implementation
|   |-- Window.tsx         # Window frame, titlebar controls, and spatial animations
|   |-- ControlCenter.tsx  # Quick settings and status panel
|   |-- Search.tsx         # Spotlight command palette
|   |-- Workspaces.tsx     # Virtual desktop switcher
|   |-- StatusPanels.tsx   # Detailed clock, date, and battery subpanels
|   `-- Boot.tsx           # Entrance view, lock screen, and boot sequence
|
|-- apps/                  # Application Modules
|   |-- Files.tsx          # Virtual file manager with trash lifecycle and imports
|   |-- Notes.tsx          # Local notepad with instant auto-save
|   |-- Gallery.tsx        # Asset showcase and wallpaper assignment tool
|   |-- Video.tsx          # Local video player with blob URL cleanup
|   |-- Calculator.tsx     # Keyboard-driven arithmetic engine
|   |-- Browser.tsx        # Web query interface and external launch hub
|   `-- Settings.tsx       # System preferences and configuration
|
`-- styles.css             # Design tokens, typography, and glassmorphic materials
```

### Technology Stack
- **React 19** and **TypeScript 5.7**: Component-driven UI architecture with strict type safety.
- **Zustand 5**: Decentralized state stores with local storage adapters and version migration pipelines.
- **Motion (v12)**: Physics-based animation springs, spatial trajectory transforms, and reduced-motion enforcement.
- **react-rnd**: Window coordinate constraints and edge manipulation.
- **Lucide Icons**: Uniform SVG iconography.
- **Typography**: Variable font distributions of **DM Sans** and **Manrope**.

<br />

---

## Source Code and Deployment

> [!NOTE]
> The source codebase and build pipelines for **Soul OS** are maintained in a **private repository** for intellectual property and showcase considerations.
>
> This repository ([**akshat96af/SoulOSweb**](https://github.com/akshat96af/SoulOSweb)) serves as the public documentation, architectural overview, and portfolio portal.
>
> The fully compiled, interactive desktop application is deployed on GitHub Pages and can be accessed at:  
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
