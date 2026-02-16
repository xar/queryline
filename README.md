<h1 align="center">Queryline</h1>

<p align="center">
  <strong>The database client you deserve</strong><br>
  A fast, native desktop client for PostgreSQL, MySQL, SQLite, and Firestore
</p>

<p align="center">
  <a href="https://www.producthunt.com/posts/queryline">
    <img src="https://img.shields.io/badge/Product%20Hunt-Launch-orange?style=flat-square&logo=producthunt" alt="Product Hunt">
  </a>
  <a href="https://discord.gg/Ez4QtYKGz4">
    <img src="https://img.shields.io/discord/1234567890?style=flat-square&logo=discord&logoColor=white&label=Discord&color=5865F2" alt="Discord">
  </a>
  <a href="https://github.com/xar/queryline/releases">
    <img src="https://img.shields.io/github/v/release/xar/queryline?style=flat-square" alt="Release">
  </a>
  <a href="https://github.com/xar/queryline/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/xar/queryline?style=flat-square" alt="License">
  </a>
</p>

<p align="center">
  <a href="https://queryline.dev">Website</a> •
  <a href="https://github.com/xar/queryline/releases">Download</a> •
  <a href="https://discord.gg/Ez4QtYKGz4">Discord</a>
</p>

---

<p align="center">
  <img src="https://queryline.dev/queryline.png" alt="Queryline Screenshot" width="800">
</p>

---

## Features

### Multi-Database Support
Connect to **PostgreSQL**, **MySQL**, **SQLite**, and **Firestore** from a single app. No more switching between tools.

### Native Performance
Built with **Rust** and **Tauri** — not an Electron app. Smooth scrolling through 100k+ rows, instant query execution.

### Secure by Design
- Credentials stored in your **OS keychain** (not plain text)
- **SSH tunnel** support for secure remote connections
- All data stays local — no cloud sync, no telemetry

### Professional SQL Editor
- Syntax highlighting with Monaco Editor
- Multiple query tabs per connection
- Automatic query history
- Execute with `Cmd+Enter`

### Visual Data Exploration
- **Filter bar** (`Cmd+F`) — build WHERE conditions without SQL
- **Foreign key navigation** — click through table relationships
- **Row detail panel** — inspect any row's complete data
- **Column sorting** — click headers to sort

### Smart Copy & Export
- Export to **CSV**, **JSON**, or **SQL INSERT**
- Copy rows as **TypeScript types** or **Zod schemas**
- Database-aware SQL generation (proper quoting per dialect)

### Spaces — Analytical Notebooks
Import tables from any database into local **DuckDB** workspaces. Mix SQL cells with Markdown documentation. Query across PostgreSQL and MySQL data together.

### Data Editing
- Inline row editing
- Add, duplicate, delete rows
- Column DDL (add, rename, drop, modify)
- Index and foreign key management

---

## Installation

### macOS

Download the latest `.dmg` from [Releases](https://github.com/xar/queryline/releases).

```bash
# Or install via Homebrew (coming soon)
brew install --cask queryline
```

### Windows & Linux

Coming soon.

---

## Development

### Prerequisites

- [Node.js](https://nodejs.org/) 18+
- [Rust](https://rustup.rs/) 1.70+
- [Tauri CLI](https://tauri.app/v1/guides/getting-started/prerequisites)

### Setup

```bash
# Install dependencies
npm install

# Run in development mode
npm run tauri dev

# Build for production
npm run tauri build
```

### Testing

```bash
# Run Rust tests (no Docker needed)
cd src-tauri && cargo test --test driver_sqlite --test export --test cache_duckdb \
  --test connection_manager --test history --test settings -- --test-threads=1
```

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | [Tauri 2](https://tauri.app/) |
| Frontend | [Vue 3](https://vuejs.org/) + TypeScript |
| UI | [shadcn-vue](https://www.shadcn-vue.com/) + [Tailwind CSS](https://tailwindcss.com/) |
| Editor | [Monaco Editor](https://microsoft.github.io/monaco-editor/) |
| Backend | Rust |
| Database Drivers | [sqlx](https://github.com/launchbadge/sqlx) (PostgreSQL, MySQL, SQLite) |
| Analytics Engine | [DuckDB](https://duckdb.org/) |
| Credential Storage | OS Keychain via [keyring](https://crates.io/crates/keyring) |

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Cmd+K` | Open command palette |
| `Cmd+Enter` | Execute query |
| `Cmd+F` | Open filter bar |
| `Cmd+T` | New query tab |
| `Cmd+W` | Close current tab |

---

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## Community

- [Discord](https://discord.gg/Ez4QtYKGz4) — Get help, share feedback, connect with other users
- [Product Hunt](https://www.producthunt.com/posts/queryline) — Support us with an upvote!
- [GitHub Issues](https://github.com/xar/queryline/issues) — Report bugs or request features

---

## License

[MIT](LICENSE) © Queryline

---

<p align="center">
  Made with ❤️ for developers who work with databases
</p>
