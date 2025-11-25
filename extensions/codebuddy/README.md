# CodeBuddy Extension for Zed

This extension adds support for [CodeBuddy](https://github.com/nicepkg/codebuddy) as an ACP (Agent Coding Protocol) agent server in Zed.

## Installation

1. Open the Zed Extensions panel
2. Search for "CodeBuddy"
3. Click Install

## Usage

Once installed, CodeBuddy will be available as an agent server option in Zed's agent panel. The extension will automatically download and manage the CodeBuddy binary for your platform.

## Configuration

You can customize the CodeBuddy agent behavior in your Zed settings:

```json
{
  "agent_servers": {
    "CodeBuddy": {
      "type": "extension",
      "default_mode": null,
      "default_model": null
    }
  }
}
```

## Alternative: Using a Custom Command

If you prefer to use a locally-installed `codebuddy` binary instead of the extension-managed one, you can configure a custom agent server:

```json
{
  "agent_servers": {
    "CodeBuddy": {
      "type": "custom",
      "command": "codebuddy",
      "args": ["--acp"],
      "env": {}
    }
  }
}
```

## Requirements

- Zed v0.150.0 or later
- CodeBuddy ACP binary (automatically installed by this extension)

## License

Licensed under the Apache License, Version 2.0.
