# Faust Language Support for VS Code

A VS Code extension that provides language support for [Faust](https://faust.grame.fr/), a functional programming language specifically designed for real-time signal processing and digital audio applications.

## About Faust

Faust (Functional Audio Stream) is a domain-specific purely functional programming language for creating digital signal processing algorithms and music applications. It compiles to various targets including C++, JavaScript, WebAssembly, and more, making it ideal for audio software development.

## Features

- **Syntax Highlighting**: Rich syntax highlighting for Faust code (.dsp and .lib files)
- **Language Server Integration**: Advanced language features powered by [faustlsp](https://github.com/carn181/faustlsp)
- **Auto-completion**: Intelligent code completion (when faustlsp is configured)
- **Error Detection**: Real-time syntax and semantic error reporting
- **Code Navigation**: Go-to-definition and symbol navigation support

## Prerequisites

- [VS Code](https://code.visualstudio.com/) version 1.75.0 or later
- [faustlsp](https://github.com/carn181/faustlsp) installed and available in your system PATH (required for advanced language features)

## Installation

### From VS Code Marketplace (Recommended)
1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X / Cmd+Shift+X)
3. Search for "Faust"
4. Click Install

### Manual Installation
1. Download the latest `.vsix` file from the releases page
2. Open VS Code
3. Go to Extensions view
4. Click on "..." menu and select "Install from VSIX..."
5. Select the downloaded `.vsix` file

## Configuration

For advanced language server features, you need to:

1. **Install faustlsp**: Follow the installation instructions at [faustlsp repository](https://github.com/carn181/faustlsp)

2. **Create a configuration file**: Add a `.faustcfg.json` file in your Faust project's root directory. This file configures the language server for your project.

Example `.faustcfg.json`:
```json
{
  "includePaths": ["./lib", "./examples"],
  "compilerOptions": {
    "architecture": "default"
  }
}
```

## Usage

1. Open any `.dsp` or `.lib` file in VS Code
2. The extension will automatically activate and provide syntax highlighting
3. If faustlsp is installed and configured, you'll get additional features like:
   - Auto-completion
   - Error diagnostics
   - Go-to-definition
   - Hover documentation

## Supported File Types

- `.dsp` - Faust DSP files
- `.lib` - Faust library files

## Troubleshooting

### Language Server Not Starting
If you see a warning about faustlsp not being found:
1. Ensure faustlsp is installed and in your system PATH
2. Restart VS Code after installing faustlsp
3. Check that you have a `.faustcfg.json` file in your workspace root

### No Syntax Highlighting
1. Ensure your file has a `.dsp` or `.lib` extension
2. Try reloading the window (Ctrl+Shift+P / Cmd+Shift+P → "Developer: Reload Window")

## Resources

- [Faust Official Website](https://faust.grame.fr/)
- [Faust Documentation](https://faustdoc.grame.fr/)
- [Faust Language Server (faustlsp)](https://github.com/carn181/faustlsp)
- [Faust Tutorials](https://faust.grame.fr/doc/manual/index.html)

## Development

### Building from Source

1. Clone this repository
2. Run `npm install` to install dependencies
3. Open the project in VS Code
4. Press `F5` to launch a new Extension Development Host window
5. Open a Faust project in the new window to test the extension

### Testing

```bash
npm run compile    # Compile TypeScript
npm run lint      # Run ESLint
npm run test      # Run tests
```  
