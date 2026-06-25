<div align="center">

<img src="https://iruka.dorienherremans.com/icons/iruka256.png" width="128" alt="Iruka icon"/>

# Iruka

**The file manager for developers who live in the terminal**

Iruka puts a full, synced shell right below your files — so `git status`, `npm install`, and a quick `grep` live in the same window as your directory browser. Built natively in SwiftUI, keyboard-first, no Electron.

[![macOS 14+](https://img.shields.io/badge/macOS-14%2B-black?logo=apple&logoColor=white)](https://iruka.dorienherremans.com)
[![Latest release](https://img.shields.io/github/v/release/dorienh/iruka-releases?label=download&color=blue)](https://github.com/dorienh/iruka-releases/releases/latest)

[iruka.dorienherremans.com](https://iruka.dorienherremans.com)

</div>

---

## Features

### Integrated terminal with smart Sync
Every tab has a persistent shell that follows your navigation. The **Sync** button (bullseye icon) keeps the terminal's working directory in step with the file browser — and automatically pauses when it detects a long-running command so your `npm install` isn't interrupted by a stray `cd`. A banner appears with a one-click Re-enable when the command finishes.

### Tabbed navigation
Open multiple folders in independent tabs, each with its own navigation history, selection, and terminal session. Switch instantly; each tab remembers exactly where you were.

### Rubber-band multi-select
Click-drag in the blank space to the right of any filename to draw a selection rectangle — just like Forklift or PathFinder. Hold ⌘ to add to an existing selection, or Shift-click for range selection. Drag a file by its name to move it; drag from blank space to select.

### Rich preview pane
- **CSV / TSV** — rendered as a proper grid with a bold header row, alternating shading, monospaced cells, and scrolling in both axes
- **Markdown** — rendered with headings, code blocks, blockquotes, lists, inline styling, and **GFM pipe tables** (bordered, with alternating rows)
- **Code** — syntax-aware monospaced view for 40+ languages; JSON is auto pretty-printed
- **Everything else** — Quick Look for images, PDFs, videos, and any format macOS understands

### Git integration
Branch name, dirty file count, ahead/behind badges, and Push/Pull buttons live in the status bar whenever you're inside a repo. Right-click any file to stage it (`git add`), or stage everything at once. The Commit button opens a sheet where you can write a message and optionally stage all changes first — all commands run through the terminal so you see the output.

### SSH connection manager
Save SSH connections in the sidebar (host, user, port, key path, notes). One click opens a new tab with the terminal connected to the remote server. Edit or delete connections from the sidebar's context menu.

### Appearance control
A toolbar button cycles **System → Light → Dark**, with matching icon (half-circle / sun / moon). The terminal theme follows automatically: pick a separate default theme for light mode and dark mode in Settings › Terminal — or use the same one for both.

### Advanced search
Recursive full-filesystem search with live results. Filter by name, extension, and kind (files / folders). Results open directly in a Quick Look panel or reveal in the file browser. Searches `~/Library` and system paths that Spotlight sometimes misses.

### Color labels
Set Finder-compatible colour labels on any file or folder — changes appear in Finder immediately. Seven colours supported, synced via standard macOS extended attributes.

### Archive support
Compress any selection to a `.zip` with one click. Extract `.zip`, `.tar`, `.tar.gz`, `.tar.bz2`, `.tar.xz`, and `.tgz` archives in place.

### Keyboard first
Every action has a shortcut. Navigate with arrow keys, open with ↩, rename with a slow second click or F2, go back/forward with ⌘\[ / ⌘\], jump to any path with ⌘L, Quick Look with Space.

### Sidebar
Quick access to favourites, iCloud Drive, SSH connections, and connected volumes. Drag any folder to add it as a favourite. Eject any volume with a single click — Iruka automatically redirects any tabs browsing inside it.

---

## Keyboard Shortcuts

| Action | Key |
|--------|-----|
| Back / Forward | `⌘[` / `⌘]` |
| Enclosing folder | `⌘↑` |
| Open / navigate into | `↩` |
| Quick Look | `Space` |
| Rename | slow second click |
| Trash selected | `⌫` |
| Permanent delete | `⌘⌫` |
| New File | `⌘⌥N` |
| New Folder | `⌘⇧N` |
| New Tab | `⌘T` |
| Close Tab | `⌘W` |
| Go Home | `⌘⇧H` |
| Go to Folder… | `⌘L` |
| Toggle hidden files | `⌘⇧.` |
| Toggle terminal | `F4` |
| Toggle preview pane | `⌘⌥P` |
| Find… | `⌘F` |
| Advanced Search… | `⌘⇧F` |
| Reveal in Finder | `⌘⇧R` |
| Refresh | `⌘R` |
| Select all | `⌘A` |

---

## System Requirements

| | |
|---|---|
| **macOS** | Sonoma 14.0 or later |
| **Architecture** | Apple Silicon and Intel |
| **Disk space** | < 15 MB |

---

## Download

The latest release is always available on the [Releases](https://github.com/dorienh/iruka-releases/releases) page.

Iruka uses [Sparkle](https://sparkle-project.org) for automatic updates — once installed, you will be notified when a new version is available.

---

## About

Iruka is developed and maintained by **Dorien Herremans**.

Website: [iruka.dorienherremans.com](https://iruka.dorienherremans.com)
