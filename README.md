<div align="center">

# HIDE

**A fast, native-feeling code editor and AI-assisted development suite, built with C# and Avalonia.**

Yours to run, yours to own.

[Features](#features) · [Getting started](#getting-started) · [Platform status](#platform-status) · [Feedback](#feedback) · [License](#license)

</div>

---

## Overview

HIDE is a desktop IDE that pairs a custom **native text-editing engine** (C++ / Direct2D / DirectWrite) with a modern **Avalonia 12** interface. It ships with **SARAH**, an agentic AI assistant that can run against a local model, a self-hosted server or any OpenAI-compatible provider, so your code and your data stay under your control.

HIDE began as a C# WPF application and has been carried over to Avalonia, phase by phase, with full behavioural parity.

| | |
|---|---|
| **UI framework** | Avalonia 12.1 (FluentTheme, code-first views) on .NET 10 |
| **Editor engine** | `HIDEEditorCore` - native C++ / Direct2D, hosted in a `NativeControlHost` |
| **AI** | SARAH agent: Ollama, OpenAI-compatible endpoints, local GGUF models through LLamaSharp, MCP tools |
| **Themes** | Dark, Light, Deep Blue (switched live) |
| **Platforms** | Windows (primary); Linux and macOS builds and packages are produced by the build scripts (see [Platform status](#platform-status)) |

## Features

### Editor
- Native rendering engine with syntax colouring, gutter, minimap, sticky scope headers, indent guides, whitespace markers and matching-bracket highlight.
- Multi-cursor editing, find and replace, refactoring helpers, code folding, split editors and drag-to-reorder tabs with preview and pinned tabs.
- Language Server Protocol client (completion, hover, go to definition, diagnostics and more), including multi-root `workspaceFolders`.
- Configurable font, size, tab width, word wrap and format-on-save. Fonts shipped in `resources/fonts` (Clear Sans by default) are loaded directly by the native editor, so nothing has to be installed on the system.

### Workspace
- Explorer with multi-select, drag and drop (move, or copy with Ctrl), rename, delete, copy/cut/paste and reveal in the OS file manager.
- Multi-root workspaces (`.code-workspace` files, including from the command line), recent workspaces and last-workspace restore.
- Workspace-wide symbol index and find in files with include/exclude globs.
- Integrated Git: status, staging, commit, and a source-control view that follows the folder of the file you are editing.
- Integrated terminal with multiple sessions, split panes, profile selection (PowerShell, PowerShell Core, Command Prompt, Git Bash, WSL) and dockable into either sidebar or the bottom panel.

### SARAH - AI assistant
- Agentic chat with tool use, an effort slider, chat history, attachments and slash commands.
- **Bring your own model:** Ollama, any OpenAI-compatible endpoint (routers, hosted APIs, local servers) or local GGUF models. Model lists are fetched from each provider automatically.
- Model Context Protocol (MCP) servers, skills and persistent memories, all configurable and resettable from Settings.
- Awareness of every folder in a multi-root workspace.

### Built-in viewers
- **Aurevia** - a tabbed web browser with incognito tabs, tab groups (named and colour-coded) and per-tab mute.
- **Medialux** - image and video viewing, with video trim and export (needs an `ffmpeg` executable next to HIDE).
- PDF, DOCX and archive viewers open right in the editor area.

### Dualarity
A document-similarity analyser: compare a document against reference files or web sources, sentence by sentence, and review the best matches in a scored results grid with a report.

### Customisation
- **Themes:** Dark, Light and Deep Blue, applied live from *Settings -> General -> Theme*.
- **Keymaps:** the default Xoeris profile or a VS Code compatibility profile, with per-command overrides and two-step chord recording.
- **Layout:** every panel can be docked left, right or bottom; sidebars and panels toggle from the title bar.
- **Settings:** a searchable settings UI, plus everything stored in a plain `settings.json` you can edit by hand.

## Getting started

### Install

Download the installer for your platform from the [Releases](https://github.com/Xoeris/HIDE/releases) page and run it. The installer offers a per-user install (no elevation) or an all-users install, and can create desktop and start-menu shortcuts.

| Platform | Artifact |
|---|---|
| Windows | `HIDE-Installer.exe` |
| Linux | `HIDE-Installer-linux-<arch>.tar.gz`, or the `.deb` / `.tar.gz` / AppImage packages |
| macOS | `HIDE-Installer-osx-<arch>.tar.gz`, or the `.app` zip / `.dmg` |

> **macOS:** builds are not notarized, so Gatekeeper will warn on first launch (right-click -> Open).

### First run

On first launch a short wizard lets you import editor settings from VS Code, then HIDE opens. Use **File -> Open Folder** to start working. Press **Ctrl+Shift+P** for the command palette and **Ctrl+,** for Settings.

### Command line

```text
HIDE [path ...]     open files, folders or a .code-workspace file
HIDE --first-run    show the first-run wizard again
```

## Platform status

| Platform | Status |
|---|---|
| **Windows** | Primary target, fully featured. |
| **Linux / macOS** | Build, package and installer pipelines are in place. The native editor engine is currently Direct2D / DirectWrite (Windows-only), so the editor surface on these systems is the part still being ported. |

## Configuration and data

| What | Where (Windows) |
|---|---|
| Settings | `%APPDATA%\HIDE\settings.json` |
| Custom keybindings | `%APPDATA%\HIDE\keybindings.json` |
| Account session | `%APPDATA%\HIDE\auth.json` |
| Browser cache | `%LOCALAPPDATA%\HIDE\EBWebView` |

Both files are also reachable from *Settings -> General*. SARAH never sends anything anywhere you have not configured: model endpoints and MCP servers are entirely your choice.

## Feedback

HIDE is currently closed-source; this repository hosts releases, the license and documentation. Bug reports and feature requests are welcome in [Issues](https://github.com/Xoeris/HIDE/issues).

## Acknowledgements

HIDE builds on outstanding open-source work, including [Avalonia](https://avaloniaui.net/), [LLamaSharp](https://github.com/SciSharp/LLamaSharp), [LibVLCSharp](https://github.com/videolan/libvlcsharp), [PdfPig](https://github.com/UglyToad/PdfPig), [Docnet.Core](https://github.com/GowenGit/docnet), [CommunityToolkit.Mvvm](https://github.com/CommunityToolkit/dotnet), the [Inter](https://rsms.me/inter/) typeface and the fonts shipped in `resources/fonts`.

## License

HIDE is released under the [MIT License](LICENSE). Third-party components keep their own licenses.
