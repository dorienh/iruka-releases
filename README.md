<div align="center">

<img src="https://iruka.dorienherremans.com/icons/iruka256.png" width="128" alt="Iruka icon"/>

# Iruka

**The modern macOS file explorer you've been waiting for**

Iruka is a fast, native macOS file manager inspired by KDE's Dolphin — with a terminal that follows your folder, one-click git & SSH shortcuts, beautiful Markdown and code previews, and grep-powered search. The cleaner, faster alternative to Path Finder and ForkLift.

[![macOS 14+](https://img.shields.io/badge/macOS-14%2B-black?logo=apple&logoColor=white)](https://iruka.dorienherremans.com)
[![Latest release](https://img.shields.io/github/v/release/dorienh/iruka-releases?label=download&color=blue)](https://github.com/dorienh/iruka-releases/releases/latest)

 [📖 Documentation](https://iruka.dorienherremans.com/docs) · [🐛 Bug Reports](https://github.com/dorienh/iruka-releases/issues) · [💡 Feature Requests](https://github.com/dorienh/iruka-releases/issues) · [🤝 Ambassador Program](https://github.com/dorienh/iruka-releases/discussions/categories/ambassador-applications)

[iruka.dorienherremans.com](https://iruka.dorienherremans.com)

</div>

---

## Features

### Integrated terminal with smart sync
Every tab has a persistent shell that follows your navigation. The **Sync** button keeps the terminal's working directory in step with the file browser — and automatically pauses when it detects a long-running command so your `npm install` isn't interrupted by a stray `cd`. A banner appears with a one-click Re-enable when the command finishes. A **Go Here** button fires a one-shot `cd` to the current folder without affecting the Sync state.

### Three view modes
- **List view** (⌘1) — sortable columns (Name, Modified, Size, Kind), resizable widths, rubber-band multi-select. Folders show `›` disclosure triangles that expand inline with 16 pt-per-level indentation.
- **Column view** (⌘2) — Finder-style 3-pane browser; each folder click opens a new column; preview pane shows the selected file.
- **Icon grid** (⌘3) — adaptive grid of file icons at 80–100 pt.

### Tabbed navigation
Open multiple folders in independent tabs, each with its own navigation history, selection, and terminal session. Switch instantly; each tab remembers exactly where you were. Drag files directly onto a tab to move or copy them there. Hover over a folder while dragging for 750 ms and it **spring-loads** open automatically, so you can navigate deep hierarchies without dropping first.

### Rubber-band multi-select
Click-drag in the blank space to draw a selection rectangle. Hold ⌘ to add to an existing selection, or Shift-click for range selection. Drag any file by its name to move it; dragging a multi-selection moves all selected files at once.

### Rich preview pane
- **CSV / TSV** — rendered as a proper grid with a bold header row, alternating shading, monospaced cells, and scrolling in both axes
- **Markdown** — headings, code blocks, blockquotes, lists, inline styling, and GFM pipe tables (bordered, with alternating rows)
- **Code** — syntax-highlighted monospaced view for 60+ languages and text formats; JSON is auto pretty-printed
- **Everything else** — Quick Look for images, PDFs, videos, and any format macOS understands

### Editable preview pane
Any text-based file (`.md`, `.py`, `.js`, `.ts`, `.tex`, `.bib`, `.sql`, `.tf`, `.vue`, `.svelte`, and 60+ more) gets an **Edit** button in the preview toolbar. The inline editor auto-saves after 1.5 s of inactivity, supports ⌘S, and shows a Saved / Unsaved / Saving… indicator.

### Git integration
Branch name, dirty file count, ahead/behind badges, and Push/Pull buttons live in the status bar whenever you're inside a repo. Right-click any file to stage it, or stage everything at once. The Commit button opens a sheet where you can write a message — all commands run through the terminal so you see the output.

### SSH, SFTP, and SCP
Save SSH connections in the sidebar (host, user, port, key path, notes). From the **Connections** menu or sidebar:
- **SSH** — one click opens a new tab with the terminal connected to the remote server
- **SFTP mount** — browse the remote filesystem like a local folder; the volume appears in the sidebar under Volumes
- **SCP Send** — right-click any file or selection and choose **Send via SCP…** to upload to a saved remote connection
- **SCP Receive** — right-click any folder and choose **Receive via SCP…** to download files from the remote into the current directory; wildcard paths supported with a live command preview

### Network volumes (SMB, FTP, AFP, NFS, WebDAV)
Use **Connections → Connect to Server…** (⌘K) to mount any network share — Samba / Windows shares (SMB), FTP, Apple Filing Protocol (AFP), NFS, or WebDAV. Mounted volumes appear in the sidebar Volumes section and browse exactly like local folders.

### Appearance control
A toolbar button cycles **System → Light → Dark**. The terminal theme follows automatically: pick a separate default theme for light mode and dark mode in Settings › Terminal.

### Power search
Recursive full-filesystem search with live results. Filter by name, extension, kind, and content — grep-powered content search scans file contents with regex support. Results open directly in a Quick Look panel or reveal in the file browser.

### Color labels
Set Finder-compatible colour labels on any file or folder. Seven colours supported, synced via standard macOS extended attributes.

### Archive support
Compress any selection to a `.zip` with one click. Extract `.zip`, `.tar`, `.tar.gz`, `.tar.bz2`, `.tar.xz`, and `.tgz` archives in place.

### Keyboard first
Every action has a shortcut. Navigate with arrow keys, open with ↩, rename with F2 or a slow second click, Quick Look with Space, permanent delete with ⌘⌫.

### Sidebar
Quick access to **recent folders**, favourites, iCloud Drive, SSH connections, and connected volumes. All sections (Favorites, Recent, Places, Connections, Volumes) are collapsible with state persisted across launches. The Recent section automatically tracks your last 6 visited directories; right-click to remove any entry. Drag any folder to add it as a favourite. Eject any volume with a single click.

---

## Keyboard Shortcuts

| Action | Key |
|--------|-----|
| Back / Forward | `⌘[` / `⌘]` |
| Enclosing folder | `⌘↑` |
| Open / navigate into | `↩` |
| Quick Look | `Space` |
| Rename | `F2` or slow second click |
| Trash selected | `⌫` |
| Permanent delete | `⌘⌫` |
| New File | `⌘⌥N` |
| New Folder | `⌘⇧N` |
| New Tab | `⌘T` |
| Close Tab | `⌘W` |
| List view | `⌘1` |
| Column view | `⌘2` |
| Icon view | `⌘3` |
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
| Connect to Server… | `⌘K` |
| Add SSH Connection… | `⌘⌥K` |

---

## What's New in 0.7.0

- **Spring-loaded folders** — hover over any folder while dragging files for 750 ms and it opens automatically, letting you navigate deep without dropping first
- **Multi-file drag** — dragging a selection of files to another tab or into a folder now moves or copies all selected files, not just the one you grabbed
- **F2 rename** — press F2 to rename the selected item
- **Collapsible sidebar sections** — Favorites, Recent, Places, Connections, and Volumes sections can be collapsed; state persists across launches
- **Copy / Paste fixed** — file clipboard operations now work reliably; the previous build silently skipped them due to an AppKit responder chain issue
- **Navigation shortcuts fixed** — ⌘↑ (Enclosing Folder), ⌘[/⌘] (Back/Forward), ⌘⇧H (Home) now work from the file list
- **Get Info (⌘I)** — info window now appears in front of Iruka
- **Sidebar icons** — always shown in blue accent colour, matching PathFinder / ForkLift
- **Favorites deduplication** — items already shown in Places are hidden from Favorites
- **30-day free trial** with trial badge in sidebar and countdown in Settings → License

---

## Community

[🐛 Bug Reports](https://github.com/dorienh/iruka-releases/issues) · [💡 Feature Requests](https://github.com/dorienh/iruka-releases/issues) · [🤝 Ambassador Program](https://github.com/dorienh/iruka-releases/discussions/categories/ambassador-applications)

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

## License

Iruka requires a license key for continued use after the 30-day free trial. Personal (up to 3 Macs) and Team (up to 10 Macs) plans are available at [iruka.dorienherremans.com/#pricing](https://iruka.dorienherremans.com/#pricing).

### Activation
Enter your license key in **Settings → License** or at the prompt that appears on first launch. The key is validated online and stored securely in the macOS Keychain; activation works offline for up to 30 days after the last successful check. To move your license to a new Mac, use **Deactivate this Mac** in Settings → License first.

### FAQ

**Can I use Iruka on more than one Mac?**  
Yes — each license covers either 3 Macs (Personal) or 10 Macs (Team). Deactivate on a machine you no longer use to free up a slot.

**What happens when the update window expires?**  
The app continues to work exactly as it did; you just won't receive future updates. Renew your update window at any time from Settings → License.

**Is there a refund policy?**  
Yes — 14-day no-questions-asked refund via LemonSqueezy.

---

## About

Iruka is developed and maintained by **Dorien Herremans**.

Website: [iruka.dorienherremans.com](https://iruka.dorienherremans.com) · [Terms of Use](TERMS.md) · [Privacy Policy](PRIVACY.md)
