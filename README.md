# MXU

**MXU** is a universal GUI client based on the [MaaFramework PI V2](https://github.com/MaaXYZ/MaaFramework/blob/main/docs/zh_cn/3.3-ProjectInterfaceV2%E5%8D%8F%E8%AE%AE.md) protocol, built with Tauri + React + TypeScript.

It can parse any `interface.json` file conforming to the PI V2 standard and provide out-of-the-box graphical interfaces for automation projects in the MaaFramework ecosystem.

## ✨ Features

- 📋 **Task Management** - Visualize and configure task lists with drag-and-drop reordering support
- 🔧 **Multi-Instance Support** - Manage multiple independent running instances simultaneously (tabbed multi-open)
- 🎮 **Multiple Controller Types** - Support for Adb, Win32, PlayCover, and Gamepad
- 🌍 **Internationalization** - Built-in multi-language UI with automatic translation loading from `interface.json`
- 🎨 **Light/Dark Themes** - Support for switching between Light and Dark themes
- 📱 **Real-Time Screenshots** - Display real-time device screen with customizable frame rate
- 📝 **Execution Logs** - View task execution logs and Agent output
- ⏰ **Scheduled Tasks** - Support for configuring scheduled execution policies
- 🔄 **Auto-Update** - Support automatic downloads from MirrorChyan and GitHub
- 🤖 **Agent Support** - Support for MaaAgentClient to implement custom recognizers and actions

## 🚀 Quick Start

### Dependencies

[MXU Releases](https://github.com/MistEO/MXU/releases) provides a single executable file (mxu.exe). You need to configure the following dependencies:

- [MaaFramework](https://github.com/MaaXYZ/MaaFramework/releases) runtime library ( >= `v5.5.0-beta.1` ). Extract the `bin` folder contents from the archive into the `maafw` folder
- [interface.json](https://github.com/MaaXYZ/MaaFramework/blob/main/sample/interface.json) and related resource files. Please refer to the [PI Protocol Documentation](https://github.com/MaaXYZ/MaaFramework/blob/main/docs/zh_cn/3.3-ProjectInterfaceV2%E5%8D%8F%E8%AE%AE.md) for configuration

Directory structure as follows:

```text
your-project/
├── mxu.exe (or mxu / mxu.app)
├── maafw/
│   ├── MaaFramework.dll (Windows)
│   ├── MaaToolkit.dll
│   └── ... other dependencies
├── interface.json
└── resource/
```

Then double-click to open `mxu.exe`!

### User Files

User configuration is saved in the `config` folder, and debug logs are saved in the `debug` folder. You can also open the folder directly from Settings - Debug.

## 📖 Development & Debugging

### Install Dependencies

**Node.js** (>= 18)

```bash
# macOS (Homebrew)
brew install node

# Windows (winget)
winget install OpenJS.NodeJS
```

**pnpm** (>= 8)

```bash
npm install -g pnpm
```

**Rust** (>= 1.70)

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```

**Project Dependencies**

```bash
pnpm install
```

### Development Debugging

```bash
pnpm tauri dev
```

Start the frontend development server and Tauri desktop application with hot reload support.

### Production Build

```bash
pnpm tauri build
```

Build artifacts are located in the `src-tauri/target/release/` directory.

## 🔧 Tech Stack

| Category | Technology |
| -------- | --------------------------------------------------- |
| Desktop Framework | [Tauri](https://tauri.app/) v2 |
| Backend Language | [Rust](https://www.rust-lang.org/) 1.70+ |
| Frontend Framework | [React](https://react.dev/) 19 |
| Type System | [TypeScript](https://www.typescriptlang.org/) 5.8 |
| Styling | [Tailwind CSS](https://tailwindcss.com/) 4 |
| State Management | [Zustand](https://zustand-demo.pmnd.rs/) |
| Internationalization | [i18next](https://www.i18next.com/) + react-i18next |
| Drag & Drop | [@dnd-kit](https://dndkit.com/) |
| Icons | [Lucide React](https://lucide.dev/) |
| Build Tool | [Vite](https://vitejs.dev/) 7 |

## 🤝 Related Projects

- [MaaFramework](https://github.com/MaaXYZ/MaaFramework) - Automated black-box testing framework based on image recognition

## 📄 License

[GNU Affero General Public License v3.0](LICENSE)
