# Horizone IDE Open Source Software Statement

*Last updated: 25 September 2026*

Horizone IDE is proprietary software by Xoeris (see the [License](LICENSE.md)), but it is built on, and ships with, open-source software. Each component below is licensed under its own licence, which applies to that component only and is not changed by the Horizone IDE License. Nothing in the Horizone IDE License limits the rights these licences give you.

## Application libraries

| Component | Licence | Source |
|---|---|---|
| Avalonia | MIT | https://github.com/AvaloniaUI/Avalonia |
| Avalonia WebView | MIT | https://github.com/AvaloniaUI/Avalonia |
| LLamaSharp | MIT | https://github.com/SciSharp/LLamaSharp |
| llama.cpp (LLamaSharp CPU backend) | MIT | https://github.com/ggml-org/llama.cpp |
| LibVLCSharp | LGPL-2.1 | https://github.com/videolan/libvlcsharp |
| LibVLC (VLC media engine) | LGPL-2.1-or-later | https://code.videolan.org/videolan/vlc |
| PdfPig | Apache-2.0 | https://github.com/UglyToad/PdfPig |
| Docnet.Core | MIT | https://github.com/GowenGit/docnet |
| CommunityToolkit.Mvvm | MIT | https://github.com/CommunityToolkit/dotnet |
| Inter typeface | OFL-1.1 | https://rsms.me/inter/ |
| .NET runtime | MIT | https://github.com/dotnet/runtime |

The fonts distributed in `resources/fonts` keep their own licences, included next to each font.

## Bundled language servers and runtimes

So that code intelligence works without installing anything, Horizone IDE ships these programs, unmodified, in its `LanguageServers` folder. It starts them as separate processes and talks to them over the Language Server Protocol.

| Language(s) | Component | Licence | Source |
|---|---|---|---|
| (runtime) | Node.js | MIT | https://github.com/nodejs/node |
| TypeScript, JavaScript | typescript-language-server, TypeScript | MIT, Apache-2.0 | https://github.com/typescript-language-server/typescript-language-server |
| HTML, CSS, JSON | vscode-langservers-extracted | MIT | https://github.com/hrsh7th/vscode-langservers-extracted |
| YAML | yaml-language-server | MIT | https://github.com/redhat-developer/yaml-language-server |
| Python | Pyright | MIT | https://github.com/microsoft/pyright |
| Shell | bash-language-server | MIT | https://github.com/bash-lsp/bash-language-server |
| Shell diagnostics | ShellCheck | GPL-3.0 | https://github.com/koalaman/shellcheck |
| Dockerfile | dockerfile-language-server-nodejs | MIT | https://github.com/rcjsuen/dockerfile-language-server |
| C, C++ | clangd | Apache-2.0 WITH LLVM-exception | https://github.com/clangd/clangd |
| Rust | rust-analyzer | MIT OR Apache-2.0 | https://github.com/rust-lang/rust-analyzer |
| Markdown | Marksman | MIT | https://github.com/artempyanykh/marksman |
| Plain text | Harper | Apache-2.0 | https://github.com/Automattic/harper |
| TOML | Taplo | MIT | https://github.com/tamasfe/taplo |
| XML | Eclipse LemMinX | EPL-2.0 | https://github.com/eclipse-lemminx/lemminx |
| Java | Eclipse JDT Language Server | EPL-2.0 | https://github.com/eclipse-jdtls/eclipse.jdt.ls |
| Java (runtime) | Eclipse Temurin JRE | GPL-2.0 WITH Classpath-exception-2.0 | https://github.com/adoptium/jdk21u |
| Go | gopls | BSD-3-Clause | https://github.com/golang/tools |
| Go (toolchain) | Go | BSD-3-Clause | https://github.com/golang/go |
| C# | csharp-ls | MIT | https://github.com/razzmatazz/csharp-language-server |
| C# (SDK) | .NET SDK | MIT | https://github.com/dotnet/sdk |

The full list, including every npm package, Go module and NuGet package these programs contain, with the complete text of each licence, is in **`LanguageServers/THIRD-PARTY-NOTICES.txt`** in your Horizone IDE installation.

PHP support uses [Intelephense](https://intelephense.com/), which is **not** bundled because its licence does not allow redistribution. Install it yourself (`npm i -g intelephense`) and Horizone IDE will find it.

## Source code for copyleft components

- **ShellCheck (GPL-3.0)** and **Eclipse Temurin (GPL-2.0 with Classpath Exception)** are shipped unmodified. Their complete source code is available from the links above for the exact versions listed in `THIRD-PARTY-NOTICES.txt`, and on request from Xoeris for at least three years (see [Contact](CONTACT.md)).
- **Eclipse JDT Language Server** and **Eclipse LemMinX (EPL-2.0)** are shipped unmodified; their source code is at the links above.
- **LibVLCSharp and LibVLC (LGPL)** are used as separate, dynamically loaded libraries that you may replace with your own build. Their source code is at the links above.

## Questions

If you believe a notice is missing or wrong, please [open an issue](https://github.com/Xoeris/Horizone-IDE/issues/new).
