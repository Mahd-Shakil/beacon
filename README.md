# Beacon

**AI-Powered Screen Tutorial Guide**

Beacon is an intelligent desktop assistant that provides real-time, step-by-step guidance for any task on your screen. Simply describe what you want to do, and Beacon will analyze your screen, create a plan, and guide you through each step with visual overlays.

[Devpost Link](https://devpost.com/software/beacon-hyv46n)

## Features

### 🤖 AI-Powered Task Planning
- Powered by Google Gemini AI to understand natural language tasks
- Automatically generates step-by-step plans based on your screen context
- Adapts to your current application and UI state

### 👁️ Smart Element Detection
- **OCR-based text detection** - Finds buttons, labels, and UI text
- **AI-powered region detection** - Custom algorithm using Gemini for intelligent UI element identification
- **Hybrid locator** - Combines multiple detection methods for accuracy
- **Region-aware** - Understands screen regions (menu bar, dock, main content)

### 🎯 Visual Overlay Interface
- Non-intrusive transparent overlay
- Highlights UI elements you need to interact with
- Shows step progress and instructions
- Click-through design that doesn't interfere with your workflow

### 🚀 Real-time Guidance
- Takes screenshots to understand your current context
- Provides contextual help based on what's on screen
- Guides you through complex multi-step workflows

## Use Cases

- **Learn new software** - Get guided tours of unfamiliar applications
- **Workflow assistance** - Step-by-step help for complex tasks
- **UI automation preparation** - Plan and visualize automation sequences
- **Accessibility** - Visual guidance for navigation and interaction
- **Documentation** - Record and share step-by-step procedures

## How It Works

1. **Describe your task** - Type what you want to do in natural language
2. **AI analyzes your screen** - Beacon captures your screen and uses AI to understand the context
3. **Plan generation** - Creates a step-by-step plan to accomplish your task
4. **Visual guidance** - Highlights elements and shows instructions in real-time
5. **Progress tracking** - Follow along as Beacon guides you through each step

## Tech Stack

- **Frontend**: Electron - Cross-platform desktop app with transparent overlay
- **Backend**: Python - AI processing, vision, and OCR
- **AI**: Google Gemini - Natural language understanding and task planning
- **Vision**:
  - Tesseract OCR - Text detection
  - Custom region detection algorithm with Gemini - AI-powered UI element identification
  - PIL/Pillow - Image processing
- **Platform**: macOS (with Quartz framework for window management)

## Quick Start

1. Clone the repository
2. Follow the [build instructions](BUILD.md)
3. Set up your Google API key
4. Run `npm start` in the client directory
5. Start getting guided!

For detailed setup instructions, see [BUILD.md](BUILD.md).

## Architecture

```
┌─────────────────────────────────────┐
│   Electron Desktop App (Client)    │
│  - Transparent overlay              │
│  - User input capture               │
│  - Visual highlighting              │
└─────────────┬───────────────────────┘
              │
              ▼
┌─────────────────────────────────────┐
│    Python Engine (Backend)          │
│  ┌───────────────────────────────┐  │
│  │  Planner (Gemini AI)          │  │
│  │  - Task understanding         │  │
│  │  - Plan generation            │  │
│  └───────────────────────────────┘  │
│  ┌───────────────────────────────┐  │
│  │  Locators                     │  │
│  │  - OCR (Tesseract)            │  │
│  │  - Region detection (Gemini)  │  │
│  │  - Hybrid locator             │  │
│  └───────────────────────────────┘  │
│  ┌───────────────────────────────┐  │
│  │  Region Manager               │  │
│  │  - Screen region detection    │  │
│  │  - Context awareness          │  │
│  └───────────────────────────────┘  │
└─────────────────────────────────────┘
```

## Project Status

Beacon is currently in active development (v0.1.0). Core features are functional, but the project is evolving rapidly.

### Current Capabilities
- ✅ Task planning with AI
- ✅ Screen capture and analysis
- ✅ Element detection (OCR + icons)
- ✅ Visual overlay system
- ✅ macOS support

### Roadmap
- 🔄 Enhanced element detection accuracy
- 🔄 Interactive tutorial mode
- 🔄 Multi-monitor support
- 📋 Windows/Linux support
- 📋 Tutorial recording and playback
- 📋 Cloud sync for saved tutorials

## Contributing

Beacon is an open-source project. Contributions are welcome! See [BUILD.md](BUILD.md) for development setup.

## License

MIT License - See LICENSE file for details

## Credits

Built with:
- [Electron](https://www.electronjs.org/)
- [Google Gemini AI](https://ai.google.dev/)
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- [PyObjC](https://pyobjc.readthedocs.io/)

---

**Note**: Beacon requires accessibility permissions on macOS to capture screenshots and detect UI elements. You'll be prompted to grant these permissions when you first run the app.
