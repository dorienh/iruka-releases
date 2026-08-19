<div align="center">

<img src="https://iruka.sh/icons/iruka256.png" width="128" alt="Iruka icon"/>

# Iruka

**The modern macOS file explorer you've been waiting for**

Iruka is a fast, native macOS file manager inspired by KDE's Dolphin — with a terminal that follows your folder, a git review pane for reading back what a coding agent just did, file and folder diffs, SSH/SFTP/FTP/cloud mounts, beautiful Markdown and code previews, and grep-powered search. The cleaner, faster alternative to Path Finder and ForkLift.

[![macOS 14+](https://img.shields.io/badge/macOS-14%2B-black?logo=apple&logoColor=white)](https://iruka.sh)
[![Latest release](https://img.shields.io/github/v/release/dorienh/iruka-releases?label=download&color=blue)](https://github.com/dorienh/iruka-releases/releases/latest)

 [📖 Documentation](https://iruka.sh/docs) · [🐛 Bug Reports](https://github.com/dorienh/iruka-releases/issues) · [💡 Feature Requests](https://github.com/dorienh/iruka-releases/issues) · [🤝 Ambassador Program](https://github.com/dorienh/iruka-releases/discussions/categories/ambassador-applications)

[iruka.sh](https://iruka.sh)

</div>

---

## Features

### Git, built for reading back what an agent just did
Iruka is a file manager for people whose repositories are being rewritten by coding agents, so git is a first-class citizen rather than a badge.

- **Review pane** (⇧⌘U) — every file that differs from your last commit, listed down one side, the diff of whichever you pick on the other. Untracked files are included in full as additions, deleted files too. It refreshes itself while an agent works beside you.
- **Build a commit out of exactly the files you want** — a checkbox per row, half-ticked when a file was staged and then edited again, and a **Commit…** button right there. Unticking only changes what the next commit records; your edits are never touched.
- **Status strip** — branch, dirty count, ahead/behind, and a red **MERGING** / **REBASING** / **CHERRY-PICKING** pill when the repository is mid-operation, telling you which command finishes the job.
- **Stage, unstage, discard, restore** from any right-click menu. Discard asks first and tells you what you're losing — how many lines, that staged work goes too, and that it doesn't go to the Trash.
- **Fetch, Push, Pull, Add Remote…, Initialize Git Repository Here…**, and **Create Pull Request** when GitHub's `gh` is installed and logged in.
- Worktrees, nested repositories and SHA-256 repositories are handled properly.

[Full git documentation →](https://iruka.sh/docs/git)

### Compare and diff
Select two files and press **⇧⌘C** for a side-by-side diff in a pane of its own — GitHub-style full-width bands with word-level highlighting on partially-changed lines. Select **one** file in a repository and you get what you've changed since your last commit. Select **two folders** and Iruka walks both trees and reports what's only on the left, only on the right, and changed in both, with `+35 −24` line counts per file, streaming in as it goes. In dual-pane mode, ⇧⌘C with nothing selected compares the two folders you're looking at. The comparison **only ever tells you** — nothing in it copies, moves or deletes. Hand any pair to **FileMerge** when you want to edit rather than read.

### SSH, SFTP, and SCP
Save SSH connections in the sidebar (host, user, port, key path, notes).

- **SSH** — one click opens a tab with the terminal connected to the remote server
- **SFTP mount** — browse the remote filesystem like a local folder. Inside a mount, the terminal's **network button** opens an SSH session that stays in step as you browse, so each folder maps to its path on the server
- **Mount as root (sudo)** — for the times the interesting files aren't the ones your login user owns. Needs one passwordless-sudo line on the server; Iruka checks for it when mounting and tells you the exact `sudoers` line if it's missing, and warns you plainly that everything you do in that volume runs as root
- **Host key verification** — mounts check `~/.ssh/known_hosts` and refuse a changed key
- **SCP Send / Receive** — right-click any file, selection or folder to transfer to or from a saved connection, with a live command preview

[SSH & SFTP documentation →](https://iruka.sh/docs/ssh)

### Network volumes and cloud storage
**Connect to Server…** (⌘K) mounts SMB, AFP, NFS and WebDAV straight through macOS — nothing to install. **FTP** and **cloud storage** (S3, Backblaze B2, Cloudflare R2, MinIO) mount through rclone plus a FUSE layer; Iruka checks for both before you enter any credentials and lists the setup steps still outstanding, each with its command to copy. [Requirements →](https://iruka.sh/docs/remote#requirements)

### Integrated terminal with smart sync
Every tab has a persistent shell that follows your navigation. **Sync** keeps the terminal's working directory in step with the file browser — and pauses automatically when it detects a long-running command, so your `npm install` isn't interrupted by a stray `cd`. A banner offers one-click Re-enable when the command finishes. **Go Here** fires a one-shot `cd` without touching the Sync state. Dual-pane layout, per-tab sessions, configurable shell, fonts, themes and scrollback. [Terminal documentation →](https://iruka.sh/docs/terminal)

### Three view modes
- **Icon grid** (⌘1) — adaptive grid of file icons
- **List view** (⌘2) — sortable columns (Name, Modified, Size, Kind), resizable widths, rubber-band multi-select, and `›` triangles that expand folders inline
- **Column view** (⌘3) — Finder-style browser; a selected folder's contents stay open beside it, and the chain follows your selection

### Folder sizes
Nothing on disk records how much a folder holds, so Iruka walks it — one folder at a time, in the background, below everything else, dropped the moment the answer stops being wanted. Sizes appear in the **Size** column, the status bar and the preview pane from a single measurement. Select things and the status bar totals them, folders included. Applications are measured too. Turn it off in Settings → General.

### Rich preview pane
- **CSV / TSV** — a proper grid with a bold header row, alternating shading and scrolling in both axes
- **Markdown** — headings, code blocks, blockquotes, lists, and GFM pipe tables
- **Code** — syntax highlighting for 60+ languages; JSON auto pretty-printed
- **PDFs, images and SVGs zoom** — ⌘−, ⌘=, ⌘0, with grab-and-drag panning and scroll bars that stay put
- **An Info strip** under every preview — kind, exact byte size, created and modified dates, owner and group, permissions in both `rwxr-xr-x` and octal, image dimensions, an app's version and bundle identifier, and what a symlink points at. All selectable text
- **Folders get a real preview** — what's inside at the top level, and the recursive size
- **Editable** — any text-based file gets an **Edit** button; auto-saves after 1.5 s, supports ⌘S

### Drop Stack
A shelf to park files on while you navigate. Add from anywhere — different folders, different tabs, different volumes — then copy or move the whole pile in one go, or only the part of it you want. [Drop Stack guide →](https://iruka.sh/docs/drop-stack)

### Batch rename
Find & replace, prefix & suffix, and numbering, applied in that order, with a live preview of every resulting name before you commit and undo after. Extensions are never touched. [Batch rename guide →](https://iruka.sh/docs/batch-rename)

### Finder integration
An **Open in Iruka** entry in Finder's right-click menu and an optional toolbar button, via a Finder extension you switch on in System Settings. [Setup →](https://iruka.sh/docs/finder-integration)

### Navigating
- **Tabs** — independent history, selection and terminal session each. Drag files onto a tab to move or copy them there; hover a folder for 750 ms while dragging and it **spring-loads** open
- **A clickable path** — the path bar's folder icon drops the whole path down as a list, so any ancestor is one click away; an optional **breadcrumb bar** whose `›` separators list sibling folders
- **Mouse side buttons** navigate back and forward
- **Show Package Contents** — browse inside an app or any bundle, while double-click still launches it

### Power search
Quick filter (⌘F) in the current folder, and **Advanced Search** (⌘⇧F) in a movable, resizable window you can leave running beside the file list. Filter by name, extension and kind, or search *contents* with grep-powered regex. [Search documentation →](https://iruka.sh/docs/search)

### File tools
- **Copy Full Path / Copy Relative Path** — the relative one measured from the git repository root, which is the form you paste into an agent or an issue
- **Open in External Terminal** — Terminal, iTerm, Ghostty, WezTerm, kitty, Alacritty, Warp and others
- **Checksum…** — SHA-256 and MD5 with copy buttons; pick exactly two files and it answers *identical* or *different* directly, by comparing contents rather than hashing both to the end
- **Color labels** — Finder-compatible, seven colours, via standard macOS extended attributes
- **Archives** — compress any selection to `.zip`; extract `.zip`, `.tar`, `.tar.gz`, `.tar.bz2`, `.tar.xz` and `.tgz` in place

### Appearance
A toolbar button cycles **System → Light → Dark**, and the terminal theme follows — pick a separate default for light and dark in Settings → Terminal.

### Keyboard first
Every action has a shortcut. Navigate with arrow keys, open with ↩, rename with F2 or a slow second click, Quick Look with Space, permanent delete with ⌘⌫.

### Sidebar
Favourites, recent folders, places, iCloud Drive, SSH connections, cloud connections and mounted volumes. Every section collapses, with state persisted across launches. Recent tracks your last visited directories; drag any folder in to make it a favourite; eject any volume with one click.

---

## Keyboard Shortcuts

A selection — the [full reference](https://iruka.sh/docs/keyboard-shortcuts) covers drag-and-drop
modifiers, the Drop Stack, column view and the rest.

| Action | Key |
|--------|-----|
| Back / Forward | `⌘[` / `⌘]` — or the **mouse side buttons** |
| Enclosing folder | `⌘↑` |
| Open / navigate into | `↩` |
| Open in default app | `⌘↓` |
| Quick Look | `Space` |
| Rename | `F2` or slow second click |
| Trash selected | `⌫` |
| Permanent delete | `⌘⌫` |
| Undo | `⌘Z` |
| New File | `⌘⌥N` |
| New Folder | `⌘⇧N` |
| New Window | `⌘N` |
| New Tab | `⌘T` |
| Close Tab | `⌘W` |
| Icon view | `⌘1` |
| List view | `⌘2` |
| Column view | `⌘3` |
| Toggle dual pane | `⌘\` |
| Switch pane | `Tab` |
| Copy to other pane | `F5` or `⌘⌥C` |
| **Compare / close the diff pane** | `⌘⇧C` |
| **Review every change in the repository** | `⌘⇧U` |
| **Next / previous file in the review** | `⌥↓` / `⌥↑` |
| Zoom the preview or the diff | `⌘−` / `⌘=` / `⌘0` |
| Go Home | `⌘⇧H` |
| Go to Folder… | `⌘L` |
| Toggle hidden files | `⌘⇧.` |
| Toggle terminal | `F4` |
| Focus terminal ↔ file browser | `⌘⌥T` |
| Toggle preview pane | `⌘⌥P` |
| Light / dark mode | `⌘⌥A` |
| Find… | `⌘F` |
| Advanced Search… | `⌘⇧F` |
| Reveal in Finder | `⌘⇧R` |
| Get Info | `⌘I` |
| Refresh | `⌘R` |
| Select all | `⌘A` |
| Connect to Server… | `⌘K` |
| Add SSH Connection… | `⌘⌥K` |

---

## What's New

Every release is written up for users — what changed and why it's worth updating — on the
[Releases page](https://github.com/dorienh/iruka-releases/releases). The same notes appear in the
app's own update window when Sparkle offers you a new version.

---

## Community

[🐛 Bug Reports](https://github.com/dorienh/iruka-releases/issues) · [💡 Feature Requests](https://github.com/dorienh/iruka-releases/issues) · [🤝 Ambassador Program](https://github.com/dorienh/iruka-releases/discussions/categories/ambassador-applications)

---

## System Requirements

| | |
|---|---|
| **macOS** | Sonoma 14.0 or later |
| **Architecture** | Apple Silicon and Intel |
| **Download** | ~12 MB (DMG) |

---

## Download

The latest release is always available on the [Releases](https://github.com/dorienh/iruka-releases/releases) page.

Or install with Homebrew:

```bash
brew install --cask dorienh/iruka/iruka
```

Iruka uses [Sparkle](https://sparkle-project.org) for automatic updates — once installed, you will be notified when a new version is available. [Installation guide →](https://iruka.sh/docs/installation)

---

## License

Iruka requires a license key for continued use after the 30-day free trial. Personal (up to 3 Macs) and Team (up to 10 Macs) plans are available at [iruka.sh/#pricing](https://iruka.sh/#pricing).

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

Website: [iruka.sh](https://iruka.sh) · [Terms of Use](TERMS.md) · [Privacy Policy](PRIVACY.md)
