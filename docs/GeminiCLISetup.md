# Gemini CLI Setup Guide

This guide provides comprehensive instructions for setting up Google's Gemini CLI on your machine.

## Official Resources

- **GitHub Repository**: [https://github.com/google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli)
- **Official Documentation**: [https://google-gemini.github.io/gemini-cli/](https://google-gemini.github.io/gemini-cli/)
- **NPM Package**: [https://www.npmjs.com/package/@google/gemini-cli](https://www.npmjs.com/package/@google/gemini-cli)
- **Getting Started Guide**: [https://geminicli.com/docs/get-started/](https://geminicli.com/docs/get-started/)

## Prerequisites

Before installing Gemini CLI, ensure you have the following:

| Requirement | Details |
|-------------|---------|
| **Operating System** | Windows 10/11, macOS 10.15+, Linux (Ubuntu 18.04+), or WSL2 |
| **Node.js** | Version 18.0 or later |
| **npm** | Version 7.0+ (bundled with Node.js) |
| **Google Account** | Required for authentication or API key from Google AI Studio |

## Installation Methods

### 1. Global Installation via NPM (Recommended)

Open your terminal and run:

```bash
npm install -g @google/gemini-cli
```

Verify the installation:

```bash
gemini --version
```

> **Note for macOS/Linux users**: If you encounter permission issues, you can either:
> - Use sudo: `sudo npm install -g @google/gemini-cli`
> - Configure npm to use a different directory to avoid using sudo

### 2. Alternative Package Managers

**Using Yarn:**
```bash
yarn global add @google/gemini-cli
```

**Using pnpm:**
```bash
pnpm install -g @google/gemini-cli
```

### 3. Run Directly Without Installation (NPX)

For quick access without permanent installation:

```bash
npx @google/gemini-cli
```

### 4. Build from Source

Clone and build from the official repository:

```bash
git clone https://github.com/google-gemini/gemini-cli.git
cd gemini-cli
npm install
npm run build
npm link
```

## Authentication & Configuration

### Authenticate with Google Account

On first run, the CLI will prompt you:

1. Select "How would you like to authenticate for this project?"
2. Choose "Login with Google"
3. Select your Google account and sign in via the browser

### Using an API Key

Get your API key from [Google AI Studio](https://aistudio.google.com).

**Set as environment variable:**

```bash
# Linux/macOS
export GEMINI_API_KEY="YOUR_API_KEY"

# Windows (PowerShell)
$env:GEMINI_API_KEY="YOUR_API_KEY"

# Windows (CMD)
set GEMINI_API_KEY=YOUR_API_KEY
```

**Or configure via CLI:**

```bash
gemini config set api-key YOUR_API_KEY
```

## First-Time Setup

After installation, launch Gemini CLI:

```bash
gemini
```

You'll be guided through:
1. Selecting a theme
2. Choosing a sign-in method
3. Authentication process

### Basic Commands

```bash
# Display help
gemini --help

# Start a chat conversation
gemini chat "Hello!"

# Check version
gemini --version
```

## Troubleshooting

### Command Not Found

- Ensure Node.js and npm are installed correctly
- Verify that your npm global/bin directory is in your PATH
- Restart your terminal after installation

### Permission Denied

- Configure npm to use a local directory
- Use a Node.js version manager (like nvm) to avoid permission issues

### API Errors

- Double-check your API key configuration
- Verify Google account authentication
- Ensure your API key has the necessary permissions

## Additional Resources

- [Dev.to Step-by-Step Tutorial with Images](https://dev.to/auden/google-gemini-cli-tutorial-how-to-install-and-use-it-with-images-4phb)
- [Google AI Studio](https://aistudio.google.com) - Get your API key here
- [Gemini API Documentation](https://ai.google.dev/docs)
