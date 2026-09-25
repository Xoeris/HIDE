# Horizone IDE Privacy Policy

*Last updated: 25 September 2026*

This policy explains what data **Horizone IDE** keeps on your computer, what it sends over the network, and to whom. Horizone IDE is made by **Xoeris**.

**In short:** Horizone IDE has no telemetry, analytics or crash reporting. Your code stays on your machine unless you send it somewhere yourself, for example to an AI provider you configured.

## 1. Data stored on your computer

| What | Where (Windows) |
|---|---|
| Settings, recent folders and files | `%APPDATA%\Horizone IDE\settings.json` |
| Custom keybindings | `%APPDATA%\Horizone IDE\keybindings.json` |
| Account session (if you sign in) | `%APPDATA%\Horizone IDE\auth.json` |
| Sarah chat history, memories, skills and rules | `%APPDATA%\Horizone IDE\` |
| Language-server workspace data (for example the Java index) | `%LOCALAPPDATA%\Horizone IDE\lsp-data\` |
| Built-in browser cache and cookies | `%LOCALAPPDATA%\Horizone IDE\EBWebView` |

This data never leaves your computer by itself. Deleting these folders removes it; uninstalling Horizone IDE does not delete your own project files.

## 2. Data sent over the network

Horizone IDE only connects to the network for the features below.

### Xoeris account (optional)

If you sign in, Horizone IDE sends your username, email address, password (as a hash) and one-time codes to the Levelist service at `api.xoeris.com` / `auth.xoeris.com` to create your account, sign you in and update your profile (for example your display name). Xoeris uses this data only to run your account. Horizone IDE works without an account.

### Sarah, the AI assistant

Sarah sends your prompts, the files and code you share with it, and tool results **only to the model provider you selected**: a local model (nothing leaves your computer), a server you host, or a third-party provider such as an OpenAI-compatible endpoint. That provider handles the data under its own privacy policy. MCP servers you add receive the requests Sarah makes to them.

### Web search and the built-in browser

The built-in browser loads the pages you open. Its default homepage and search provider is Aurevia (`aurevia.xoeris.com`); you can switch to Google, DuckDuckGo, Bing or Baidu in *Settings*. Searches go to the provider you picked. When Sarah searches the web, the query goes to the search service configured in Settings.

### Extensions

Browsing or installing extensions queries the Visual Studio Marketplace (`marketplace.visualstudio.com`) with your search terms.

### Language servers

The bundled language servers run on your computer and do not send your code anywhere. Some may download what a project asks for when you open it, for example Go modules through the Go toolchain or NuGet packages when a .NET project is restored, in the same way the normal command-line tools would.

### Update check

*Check for Updates* contacts GitHub (`github.com`) to read the latest release of Horizone IDE. Only the normal request data that any web request carries (such as your IP address) is involved.

## 3. What Xoeris does not do

- No telemetry, usage analytics or crash reports are collected.
- Your code, files and chats are not uploaded to Xoeris.
- Xoeris does not sell your data or use it for advertising.

## 4. Your choices and rights

- Use Horizone IDE without an account, and with a local AI model, to keep everything on your computer.
- Sign out at any time from the account menu; this deletes the local session.
- To access, correct or delete your Xoeris account data, contact us (see below). Depending on where you live, you may have further rights under data-protection law.

## 5. Children

Horizone IDE is not directed at children under 13, and Xoeris does not knowingly create accounts for them.

## 6. Changes to this policy

We may update this policy. The current version is always in this file, and its history is visible in this repository.

## 7. Contact

Privacy questions or requests: see [Contact](CONTACT.md).

© 2018 - 2026 Xoeris. All rights reserved.
