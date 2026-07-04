<div align="center">

<img src="https://iruka.dorienherremans.com/icons/iruka256.png" width="128" alt="Iruka icon"/>

# Iruka

**The modern macOS file explorer you've been waiting for**

Iruka is a fast, native macOS file manager inspired by KDE's Dolphin — with a terminal that follows your folder, one-click git & SSH shortcuts, beautiful Markdown and code previews, and grep-powered search. The cleaner, faster alternative to Path Finder and ForkLift.

[![macOS 14+](https://img.shields.io/badge/macOS-14%2B-black?logo=apple&logoColor=white)](https://iruka.dorienherremans.com)
[![Latest release](https://img.shields.io/github/v/release/dorienh/iruka-releases?label=download&color=blue)](https://github.com/dorienh/iruka-releases/releases/latest)

 [🐛 Bug Reports](https://github.com/dorienh/iruka-releases/discussions/categories/bug-reports) · [💡 Feature 
  Requests](https://github.com/dorienh/iruka-releases/discussions/categories/feature-requests) · [🤝 Ambassador 
  Program](https://github.com/dorienh/iruka-releases/discussions/categories/ambassador-applications)
  
[iruka.dorienherremans.com](https://iruka.dorienherremans.com)

</div>

---

## Features

### Integrated terminal with smart sync
Every tab has a persistent shell that follows your navigation. The **Sync** button keeps the terminal's working directory in step with the file browser — and automatically pauses when it detects a long-running command so your `npm install` isn't interrupted by a stray `cd`. A banner appears with a one-click Re-enable when the command finishes.

### Three view modes
- **List view** — sortable columns (Name, Modified, Size, Kind), resizable widths, rubber-band multi-select. Folders show `›` disclosure triangles that expand inline with 16 pt-per-level indentation.
- **Icon grid** — adaptive grid of file icons at 80–100 pt.
- **Column view** (⌘3) — Finder-style 3-pane browser; each folder click opens a new column; preview pane shows the selected file.

### Tabbed navigation
Open multiple folders in independent tabs, each with its own navigation history, selection, and terminal session. Switch instantly; each tab remembers exactly where you were.

### Rubber-band multi-select
Click-drag in the blank space to draw a selection rectangle. Hold ⌘ to add to an existing selection, or Shift-click for range selection. Drag a file by its name to move it.

### Rich preview pane
- **CSV / TSV** — rendered as a proper grid with a bold header row, alternating shading, monospaced cells, and scrolling in both axes
- **Markdown** — headings, code blocks, blockquotes, lists, inline styling, and GFM pipe tables (bordered, with alternating rows)
- **Code** — syntax-highlighted monospaced view for 60+ languages and text formats; JSON is auto pretty-printed
- **Everything else** — Quick Look for images, PDFs, videos, and any format macOS understands

### Editable preview pane
Any text-based file (`.md`, `.py`, `.js`, `.ts`, `.tex`, `.bib`, `.sql`, `.tf`, `.vue`, `.svelte`, and 60+ more) gets an **Edit** button in the preview toolbar. The inline editor auto-saves after 1.5 s of inactivity, supports ⌘S, and shows a Saved / Unsaved / Saving… indicator.

### Git integration
Branch name, dirty file count, ahead/behind badges, and Push/Pull buttons live in the status bar whenever you're inside a repo. Right-click any file to stage it, or stage everything at once. The Commit button opens a sheet where you can write a message — all commands run through the terminal so you see the output.

### SSH connection manager
Save SSH connections in the sidebar (host, user, port, key path, notes). One click opens a new tab with the terminal connected to the remote server. Mount remote servers as SFTP volumes and browse them like a local folder.

### Appearance control
A toolbar button cycles **System → Light → Dark**. The terminal theme follows automatically: pick a separate default theme for light mode and dark mode in Settings › Terminal.

### Advanced search
Recursive full-filesystem search with live results. Filter by name, extension, and kind. Results open directly in a Quick Look panel or reveal in the file browser.

### Color labels
Set Finder-compatible colour labels on any file or folder. Seven colours supported, synced via standard macOS extended attributes.

### Archive support
Compress any selection to a `.zip` with one click. Extract `.zip`, `.tar`, `.tar.gz`, `.tar.bz2`, `.tar.xz`, and `.tgz` archives in place.

### Keyboard first
Every action has a shortcut. Navigate with arrow keys, open with ↩, rename with a slow second click or F2, Quick Look with Space, permanent delete with ⌘⌫.

### Sidebar
Quick access to favourites, iCloud Drive, SSH connections, and connected volumes. Drag any folder to add it as a favourite. Eject any volume with a single click.

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
| List view | `⌘1` |
| Icon view | `⌘2` |
| Column view | `⌘3` |
| Go Home | `⌘⇧H` |
| Go to Folder… | `⌘L` |
| Toggle hidden files | `⌘⇧.` |
| Toggle terminal | `F4` |
| Toggle preview pane | `⌘⌥P` |
| Find… | `⌘F` |
| Advanced Search… | `⌘⇧F` |
| Reveal in Finder | `⌘⇧R` |
| Get Info | `⌘I` |
| Refresh | `⌘R` |
| Select all | `⌘A` |

---

## What's New in 0.4.0

- **New File / New Folder prompt** — name your item before it's created; no inline rename step
- **Newly created items are selected and scrolled into view** automatically
- **⌘Delete works reliably** from anywhere in the window, even with terminal focus
- **Terminal typing no longer breaks** after clicking a file row

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
