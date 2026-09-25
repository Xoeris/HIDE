# Horizone IDE Help

Welcome to **Horizone IDE**, a native code editor and AI-assisted development suite by Xoeris. This page covers the basics; for an overview of every feature see the [README](README.md).

## Getting started

1. Download the installer for your system from the [Releases page](https://github.com/Xoeris/Horizone-IDE/releases) and run it.
2. Start Horizone IDE and choose **Open Folder** to open a project, or open a single file.
3. Optional: sign in with a Xoeris account from the avatar in the title bar. Everything except account features works without signing in.

You can also start it from a terminal:

```
HorizoneIDE.exe <folder> [file ...]
```

## Code intelligence (language servers)

Completion, diagnostics (errors and warnings), hover information and go-to-definition work **out of the box**. Horizone IDE ships its own language servers and runtimes, so you don't need to install anything:

TypeScript, JavaScript, HTML, CSS, JSON, YAML, Python, Shell, Dockerfile, C, C++, Rust, Go, Java, C#, Markdown, TOML, XML and plain text (spelling and grammar).

Good to know:

- **Java** and **C#** load your whole project first. The first time you open a project this can take up to a minute or two; later openings are faster.
- **Java** projects are recognised by Maven (`pom.xml`), Gradle (`build.gradle`) or Eclipse (`.project`) files; loose `.java` files also work.
- **Go** uses `go.mod`; **C#** uses `.csproj` / `.sln` files.
- **Rust** needs `cargo` (from [rustup](https://rustup.rs)) to analyse a Cargo project.
- **PHP** needs Intelephense, which can't be bundled for licence reasons: run `npm i -g intelephense` and Horizone IDE finds it.
- A language server you install yourself is used only when Horizone IDE has none bundled for that language.

## Sarah, the AI assistant

Open the Sarah panel to chat, ask about your code or let Sarah edit files and run tools.

1. Go to **Settings → Models** and pick a model: a local GGUF model, Ollama, or any OpenAI-compatible provider (enter its URL and API key).
2. Sarah sends your messages and the files you share **only to the model you picked**. With a local model nothing leaves your computer.
3. Review changes and commands before you approve them.

You can add MCP servers, skills, rules and memories on their own Settings pages, and reset any of them there.

## Settings and keybindings

- **Settings**: account avatar in the title bar → *Settings*.
- **Keyboard shortcuts**: *Settings → Keyboard Shortcuts*; your changes are saved to `%APPDATA%\Horizone IDE\keybindings.json`.
- **Themes**: Dark, Light and Deep Blue, switched live in *Settings → General → Theme*.

## Updates

Choose **Settings → About → Check for Updates**. If a newer release is available, Horizone IDE opens its page on GitHub so you can download it.

## Where your data lives

Settings, chat history and the account session are stored in `%APPDATA%\Horizone IDE\`; language-server and browser caches in `%LOCALAPPDATA%\Horizone IDE\`. See the [Privacy Policy](PRIVACY.md) for details.

## Troubleshooting

| Problem | What to try |
|---|---|
| No completion or errors for a language | Wait for the first project load (Java and C# take longest). Make sure the file has the right extension. |
| "The … server failed to start" | Check `%TEMP%\HorizoneIDE-lsp.log` and include it when you report the issue. |
| Sarah doesn't answer | Check the provider URL, API key and model name in *Settings → Models*. |
| Something else | See [Contact](CONTACT.md). |

## More

- [Terms of Service](TERMS.md) · [Privacy Policy](PRIVACY.md) · [Open Source Software Statement](OPEN-SOURCE.md) · [License](LICENSE.md)
- [Report an issue](https://github.com/Xoeris/Horizone-IDE/issues/new)
