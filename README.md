# playwright_study

A sandbox project for learning and experimenting with [Playwright](https://playwright.dev/) — a modern end-to-end testing framework by Microsoft.

## What is Playwright?

Playwright is an open-source automation library that lets you write reliable end-to-end tests for modern web applications. It supports:

- **Cross-browser testing** — Chromium (Chrome, Edge), Firefox, and WebKit (Safari) out of the box.
- **Cross-platform** — runs on Windows, macOS, and Linux, locally or in CI.
- **Multi-language** — TypeScript, JavaScript, Python, .NET, and Java.
- **Auto-waiting** — Playwright automatically waits for elements to be actionable before performing actions, reducing flaky tests.
- **Powerful tooling** — codegen (record-and-playback), trace viewer, UI mode, and built-in HTML reporter.

This project uses **Playwright Test** (`@playwright/test`) with TypeScript.

## Prerequisites

Before installing Playwright, make sure you have:

- **Node.js 18+** (LTS recommended) — [nodejs.org](https://nodejs.org/)
- **npm** (bundled with Node.js)
- **Git** (optional, for cloning the repository)

Check your versions:

```bash
node -v
npm -v
```

## Installation

### macOS

1. Install Node.js via [Homebrew](https://brew.sh/):
   ```bash
   brew install node
   ```
2. Clone and enter the project:
   ```bash
   git clone https://github.com/JaxzTan/playwright_study.git
   cd playwright_study
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Install Playwright browsers:
   ```bash
   npx playwright install
   ```

### Windows

1. Install Node.js from [nodejs.org](https://nodejs.org/) (use the LTS installer), or via [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/):
   ```powershell
   winget install OpenJS.NodeJS.LTS
   ```
2. Open PowerShell or Command Prompt, then clone and enter the project:
   ```powershell
   git clone https://github.com/JaxzTan/playwright_study.git
   cd playwright_study
   ```
3. Install dependencies:
   ```powershell
   npm install
   ```
4. Install Playwright browsers:
   ```powershell
   npx playwright install
   ```

### Linux (Ubuntu / Debian)

1. Install Node.js (via NodeSource for an up-to-date version):
   ```bash
   curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
   sudo apt-get install -y nodejs
   ```
2. Clone and enter the project:
   ```bash
   git clone https://github.com/JaxzTan/playwright_study.git
   cd playwright_study
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Install Playwright browsers **and required system libraries**:
   ```bash
   npx playwright install --with-deps
   ```
   > The `--with-deps` flag installs the OS-level dependencies Playwright browsers need on Linux.

## Running Tests

All commands below are run from the project root.

| Command | What it does |
| --- | --- |
| `npx playwright test` | Run every test across all configured browsers (Chromium, Firefox, WebKit). |
| `npx playwright test --headed` | Run tests with a visible browser window. |
| `npx playwright test --ui` | Open Playwright's interactive UI mode — great for debugging. |
| `npx playwright test --debug` | Run in debug mode with the Playwright Inspector. |
| `npx playwright test example.spec.ts` | Run a specific test file. |
| `npx playwright test -g "has title"` | Run tests whose name matches the pattern. |
| `npx playwright test --project=chromium` | Run tests on a single browser only. |
| `npx playwright show-report` | Open the last HTML report. |
| `npx playwright codegen https://example.com` | Record actions and generate test code. |

## Project Structure

```
playwright_study/
├── tests/                  # test specs (*.spec.ts)
├── playwright.config.ts    # Playwright configuration
├── playwright-report/      # generated HTML report
├── test-results/           # traces, screenshots, videos from failed runs
└── package.json
```

## Useful Links

- [Playwright Docs](https://playwright.dev/docs/intro)
- [Writing Tests](https://playwright.dev/docs/writing-tests)
- [Locators Guide](https://playwright.dev/docs/locators)
- [Trace Viewer](https://playwright.dev/docs/trace-viewer)
