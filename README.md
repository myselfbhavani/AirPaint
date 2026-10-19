# AirPaint🖐️✨

> **Zero-dependency, browser-native Air Canvas powered by MediaPipe and HTML5 Canvas.**  
> Draw, erase, cycle vibrant color palettes, switch dynamic brushes, and navigate history using natural hand gestures through your webcam.

---

## 🌟 Highlights

- **Instant Double-Click Execution:** Runs natively in any modern browser without local server setups, terminal commands, or runtime dependencies.
- **Pure Solid Background:** Choose between deep high-contrast black or gallery clean white with one-click toggling.
- **7 Expressive Brushes:** Solid, Neon Glow, Calligraphy, Spray / Particle, Dotted, Highlighter, and Rainbow hue-cycle.
- **12 Curated Colors:** Instant gesture-based palette switching with visual color preview indicators.
- **Graceful Hardware Release:** Clean camera track termination and resource disposal upon exiting.

---

## 🎯 Gesture Reference Table

| Action | Hand Gesture | Description |
| :--- | :--- | :--- |
| **Draw** | ☝️ **Index Up Only** | Track index fingertip to paint lines with the active brush & color. |
| **Erase** | 🖐️ **Open Palm (5 Fingers)** | Broad eraser centered on palm coordinates reverting pixels to canvas background. |
| **Color Switch** | ✌️ **Two Fingers (Index + Middle)** | Cycle forward through the 12-shade curated palette (debounced). |
| **Brush Switch** | 🤏 **Pinch (Thumb + Index Tip)** | Cycle through all 7 brush rendering styles. |
| **Undo** | 🤟 **Three Fingers (Index + Middle + Ring)** | Revert canvas to the previous stroke state. |
| **Redo** | 👍 **Thumbs Up (Only Thumb Extended)** | Restore previously undone strokes. |
| **Quit** | ✊ **Closed Fist** | Shuts down video tracks, terminates the camera feed, and exits. |

---

## 🎨 Creative Toolkit

### Brush Types
1. **Solid:** Clean, consistent geometric line art.
2. **Neon Glow:** Dual-pass stroke with dynamic blurred outer halo.
3. **Calligraphy:** Flat-nib simulated stroke responding to angle offsets.
4. **Spray / Particle:** Airbrush dispersion using stochastic radial offsets.
5. **Dotted:** Segmented precision dash arrays.
6. **Highlighter:** Wide-band translucent overlay with 35% global alpha.
7. **Rainbow:** Dynamic hue-cycling stroke shifting along the continuous trajectory.

### Available Palette
- 🔵 **Electric Blue** (`#007bff`)
- 🟢 **Emerald Green** (`#00e676`)
- 🔴 **Crimson Red** (`#ff1744`)
- 🟡 **Amber Yellow** (`#ffd600`)
- 🟣 **Magenta** (`#f50057`)
- 🩵 **Bright Cyan** (`#00e5ff`)
- 🟠 **Sunset Orange** (`#ff6d00`)
- ⚪ **Pure White** (`#ffffff`)
- 🔮 **Deep Purple** (`#7c4dff`)
- 🩷 **Hot Pink** (`#ff4081`)
- 🍏 **Lime Glow** (`#76ff03`)
- ⚫ **Charcoal** (`#212121`)

---

## 🚀 Quick Start

1. Clone or download this repository:
   ```bash
   git clone https://github.com/your-username/GestureCanvas.git
   ```
2. Navigate to the project directory:
   ```bash
   cd GestureCanvas
   ```
3. Double-click `index.html` to open it directly in **Google Chrome**, **Microsoft Edge**, **Brave**, or **Mozilla Firefox**.
4. Grant webcam permissions when prompted.
5. Step back so your hand is clearly visible in good ambient lighting, and begin creating!

---

## 🛠️ Architecture & Tech Stack

- **Computer Vision:** [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) (WebGL / WASM runtime).
- **Core Engine:** Vanilla JavaScript (`CanvasRenderingContext2D`, `requestAnimationFrame`).
- **Webcam Pipe:** `@mediapipe/camera_utils` streaming at `1280x720` target resolution.
- **State Management:** Frame-debounced finite state transitions with array-buffered undo/redo stacks.

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).
