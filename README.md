# create-copilot-workspace

An **npx-runnable CLI tool** that scaffolds GitHub Copilot configuration files into any existing project directory.

## Usage

```bash
npx create-copilot-workspace
```

Run the command inside your project root. The tool will:

1. **Auto-detect** your project type (Next.js, Python API, etc.) by inspecting your files
2. **Prompt** you interactively if the type is ambiguous or if you want to customise
3. **Write** the appropriate Copilot configuration files — never overwriting existing ones

## What gets scaffolded

| File | Description |
|------|-------------|
| `.github/copilot-instructions.md` | Project-specific instructions for GitHub Copilot |
| `.github/prompts/*.prompt.md` | Reusable prompt files for common tasks |
| `.vscode/mcp.json` | MCP server configuration for Copilot tooling |

## Modes

- **Interactive** — answer a short series of questions to customise the output
- **Auto-detect** — the tool inspects `package.json`, `requirements.txt`, etc. and picks the best preset automatically

## Design Principles

- **Never overwrite** existing files — safe to run multiple times
- **Fast** — no unnecessary dependencies, finishes in under a second
- **Idempotent** — running twice produces the same result

## Supported Presets

| Preset | Detected by |
|--------|-------------|
| Next.js | `next` in `package.json` dependencies |
| Python API | `requirements.txt` or `pyproject.toml` present |
| Generic | Fallback for any other project |

## Development

```bash
npm install
npm run build
npm start
```

## Contributing

Contributions are welcome! Please open an issue to discuss your idea before submitting a pull request.

## License

MIT
