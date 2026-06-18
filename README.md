# CS2 Tactical Coach & Replay Analyzer

Welcome to the Defiant Eagles CS2 AI Coach! This application is a premium tactical analysis dashboard designed to help Counter-Strike 2 players automatically analyze their gameplay, track performance trends over time, review 2D positional vector maps, and generate AI-powered tactical advice based on GSI (Game State Integration) telemetry and demo replays.

---

## About

The **Defiant Eagles CS2 AI Coach** leverages advanced AI heuristics to scan Counter-Strike 2 match data. It bridges the gap between raw match records and player improvement by parsing `.dem` replay files and receiving live in-game event telemetry. The application automatically generates tactical report cards, evaluates recoil control, detects reaction deltas, and isolates critical game mistakes.

---

## Features

*   **Live Game State Integration (GSI)**: Built-in GSI listener automatically captures matches in real time, detecting player deaths, kills, map changes, and round transitions without user intervention.
*   **AI-Annotated Highlight Clips**: Automatically extracts 5-second video clips of mistakes (e.g., deaths) using FFmpeg and superimposes overlay metrics like reaction time, recoil alerts, and danger zones.
*   **100% VAC-Safe**: Runs entirely out-of-process, reading standard OS lists and utilizing official Game State Integration APIs. It does not touch CS2 memory space or modify game code, ensuring zero conflict with Valve Anti-Cheat.
*   **Auto-Launch Gateway**: Features a configurable autostart permission gateway that can launch the app minimized at Windows startup, staying ready to analyze matches the moment CS2 starts.
*   **Centralized State & Trend Analysis**: Interactive plots track team ratings and performance indices over multiple matches to monitor long-term gameplay improvement.
*   **2D Tactical Map Panel**: Renders positional retake vectors, utility feeds, kill locations, and player travel paths on 2D map rads.

---

## Screenshots

*(Screenshots will be added in a future release)*

---

## Installation & Usage

### 1. Download & Launch
1. Download `CS2_AI_Coach_Release_v1.0.0.zip` and extract the contents to a folder of your choice.
2. Launch `CS2_AI_Coach_v1.0.0.exe`.

### 2. Startup Preference Selection
On the first launch, the app prompts you with a permission popup:
*   **Always Enable**: Registers the app to start minimized with Windows, checking for CS2 launches to automatically capture live gameplay.
*   **Ask Me Next Time**: Prompts you again on the next launch.
*   **Manual Mode Only**: Disables autostart and lets you run the application and parser entirely on demand.

### 3. Demo Replay Analysis
1. To parse a downloaded demo replay, select your active **Steam ID Profile** (or create one using the `+` button in the sidebar).
2. Drag and drop any CS2 `.dem` file onto the dashboard or click the import panel to browse and select a file.
3. The parser will process the demo and automatically populate the **Match Overview**, **2D Map & Heatmap**, and **AI Tactical Coach** tabs.

### 4. Live Match Analysis & Highlights
*   Keep the application running (or minimized to the background) while playing CS2.
*   When a round event occurs, the integrated GSI server compiles highlight clips of your gameplay and saves them automatically into your profile matches folder.
*   Review generated highlights directly in the **Mistake Highlights** tab.
