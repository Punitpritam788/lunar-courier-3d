# 🌕 Lunar Courier 3D

### A 3D Space-Survival Game Built in a Single HTML File

**Pilot the spacecraft. Collect lunar samples. Survive the Solar Storm.**

[![▶ PLAY LIVE DEMO](https://img.shields.io/badge/▶_PLAY-LIVE_DEMO-00C853?style=for-the-badge)](https://punitpritam788.github.io/lunar-courier-3d/)
[![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=for-the-badge&logo=threedotjs)](https://threejs.org/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000000)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML5](https://img.shields.io/badge/HTML5-Single--File-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![WebGL](https://img.shields.io/badge/Graphics-WebGL-990000?style=for-the-badge)](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)
[![GitHub Pages](https://img.shields.io/badge/Hosted_on-GitHub_Pages-222222?style=for-the-badge&logo=githubpages)](https://pages.github.com/)

**🎮 [CLICK HERE TO PLAY LUNAR COURIER 3D](https://punitpritam788.github.io/lunar-courier-3d/)**

---

## 📖 About the Project

Lunar Courier 3D is a browser-based 3D space-survival game developed with JavaScript, Three.js, HTML, CSS, and WebGL.

The player pilots a fictional spacecraft called the *Selene Courier* on a dangerous journey toward lunar orbit. The objective is to collect drifting sample canisters, avoid rocks and debris, manage the spacecraft's shield, choose upgrades, and survive the final Solar Storm challenge.

The project explores how far a self-contained browser game can go using procedural geometry, generated textures, custom GLSL shader effects, browser-native audio, interactive storytelling, and responsive controls.

The implementation is contained in a single HTML page, with Three.js loaded from a CDN. No separate frontend compilation step is required.

### 🌐 Play Online

**Live demo:** https://punitpritam788.github.io/lunar-courier-3d/

Open the game in a modern browser with WebGL support. An internet connection is required to load the Three.js CDN dependency.

---

## ✨ Features

### 🌌 1. Procedural 3D Space Environment

The environment is constructed programmatically using Three.js.

- A cratered Moon built from displaced sphere geometry.
- Procedural surface variation using layered noise.
- Generated textures and vertex colours.
- A textured Earth with additional surface-detail layers.
- Directional sunlight and subtle Earthshine.
- A large star field with varied brightness and colour.
- Drifting ambient space dust and particle effects.
- Camera movement that supports both gameplay and cutscenes.

The environment uses procedural techniques to create visual detail without relying entirely on externally imported 3D models and textures.

### 🚀 2. Spacecraft Engine and Boost Effects

The spacecraft includes a custom animated engine plume implemented with a shader material.

The effect combines a bright central core, a widening plume, procedural noise, internal bright structures, and time-dependent variation.

Boost adds additional visual feedback through ignition flashes, glow, and shock-ring effects. These effects reinforce the player's actions rather than serving only as decoration.

### ☄️ 3. Hazard and Collision Systems

The player must navigate several types of hazards:

| Hazard | Behaviour | Gameplay response |
|---|---|---|
| Rocks | Relatively heavy obstacles that inflict significant damage | Avoid or reposition |
| Debris | Faster-moving hazards | React quickly and maintain clearance |
| Solar flares | Warning phase followed by a dangerous strike | Leave the marked region before impact |

Hazards use different behaviours and damage values, requiring the player to balance collection, movement, and survival.

### 💎 4. Collection and Shield Management

Sample canisters are the primary mission objective.

Collecting samples increases the score and advances progress toward clearing the current wave.

Power cells restore shield strength, allowing the player to recover from some damage. The spacecraft's shield must be managed carefully because losing all shield ends the run.

### ⚡ 5. Boost Ability

Boost provides a short movement burst and temporary invulnerability.

It has a recharge timer, so the player must decide when to use it. Activating it too early may leave the spacecraft vulnerable during a later encounter.

The boost system combines gameplay timing, visual effects, sound feedback, and a visible recharge indicator.

### 🔥 6. Five-Wave Progression

The mission is structured around five waves.

- Early waves establish the basic collection and survival loop.
- Later waves increase the challenge.
- Cleared waves provide an opportunity to choose an upgrade.
- Wave 5 introduces a 25-second Solar Storm survival encounter.

During the Solar Storm, survival takes priority over collecting additional samples.

### 🧰 7. Upgrade System

After clearing a wave, the player selects from three randomly presented upgrades.

| Upgrade | Effect |
|---|---|
| Plating | Adds 25 maximum shield and repairs up to 25 shield |
| Thrusters | Increases movement speed by 12% |
| Sample Magnet | Increases collectible attraction range by 50 game units |
| Quick Boost | Reduces boost recharge time by 25% |
| Dust Shroud | Reduces rock movement speed by 15% |

The upgrade system allows the player to adjust their strategy as the mission progresses.

### 🎬 8. Cinematic Storytelling

The game includes three cinematic outcomes:

**Intro:** Establishes the spacecraft, lunar mission, environmental threats, and story context.

**Victory:** Presents the successful lunar approach and concludes the sample-recovery mission.

**Failure:** Shows the consequences of taking too much damage and losing the spacecraft.

These sequences use camera positioning, changes in field of view, timed captions, and transitions. Cutscenes can be skipped.

### 🎮 9. Multiple Input Methods

The game supports several ways to play.

**Keyboard**
- WASD or arrow keys for movement.
- Space or Shift for boost.
- P or Escape for pause and resume.
- M for mute and unmute.
- F for fullscreen.

**Touch**
- Floating joystick for movement.
- On-screen boost button.
- Touch-friendly pause and audio controls.
- Configurable joystick placement and size.

**Gamepad**
- Left stick for movement.
- A button for boost.
- Start for pause or resume.
- D-pad and A for menu navigation.

### 🎨 10. Settings and Accessibility

The settings menu includes:

- Master volume, music, and sound-effect levels.
- Graphics quality and particle density.
- Screen shake and FPS display.
- Battery-saver mode.
- Movement sensitivity.
- Joystick placement, size, and opacity.
- Boost-button size.
- Vibration.
- Selectable difficulty.
- Tutorial hints.
- Alternative colour palettes.
- Reduced motion and flash reduction.
- High-contrast mode.
- Adjustable interface size.

These options make it possible to customize the presentation and controls for different preferences and hardware.

### 🏆 11. Replayability and Persistence

The game includes:

- Score tracking and a saved best score.
- Replay using the current run's seed.
- Seed sharing.
- Selectable difficulty.
- Upgrade choices that change how the player approaches the mission.
- Persistent settings and high-score data through browser LocalStorage.

---

## 🕹️ Controls

### Desktop

| Action | Key |
|---|---|
| Move up | `W` or `↑` |
| Move down | `S` or `↓` |
| Move left | `A` or `←` |
| Move right | `D` or `→` |
| Boost | `Space` or `Shift` |
| Pause / Resume | `P` or `Esc` |
| Mute / Unmute | `M` |
| Toggle fullscreen | `F` |

### Mobile and Touch Devices

1. Drag on the configured side of the screen to steer.
2. Tap the lightning button to activate boost.
3. Use the pause control to pause the game.
4. Open Settings to adjust touch-control placement and sizing.

### Gamepad

- Left stick: movement.
- A: boost.
- Start: pause or resume.
- D-pad and A: navigate menus.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and canvas |
| CSS3 | Menus, HUD, responsive layout, and transitions |
| JavaScript | Game logic, input, progression, and update loop |
| Three.js r128 | 3D scene, camera, geometry, materials, and rendering |
| WebGL | Real-time 3D rendering |
| GLSL | Engine-plume and solar-flare shader effects |
| Canvas API | Procedural texture generation |
| Web Audio API | Synthesized music and sound effects |
| LocalStorage | Saved settings and high-score data |

### Rendering and Performance

The game uses a browser animation loop to update the simulation and render the 3D scene.

Graphics quality affects rendering resolution and selected particle counts. Automatic quality adjustments can respond to observed performance, while low-power device detection helps select more conservative defaults.

The game also includes optional reduced-motion, flash-reduction, and battery-saver settings.

Actual performance depends on the browser, device, GPU, display resolution, and selected settings.

---

## 🧠 Implementation Details

### Procedural Geometry

The Moon and other generated surface details use programmatic geometry and noise-based variation. Crater calculations displace vertices to produce an irregular surface rather than a perfectly smooth sphere.

### Shader Materials

Custom GLSL fragment shaders generate selected effects, including the animated engine plume and solar-flare visuals.

The shaders use time-dependent calculations and procedural noise to create changing patterns without requiring a separate frame-by-frame animation texture.

### Generated Textures

The Canvas API is used to create texture data programmatically. This helps keep much of the visual content within the HTML implementation.

### Audio Generation

The Web Audio API creates synthesized tones and generated noise for music and sound effects. Separate controls allow the player to adjust or disable music and effects.

### Input Handling

The game uses browser keyboard and pointer events alongside gamepad input. Touch interaction is supported through a floating joystick and a dedicated boost control.

### Persistence

LocalStorage stores supported settings and high-score data. Seed values also support replaying a run and sharing a challenge.

---

## 📂 Project Structure

The repository can remain simple:

```text
lunar-courier-3d/
├── index.html       # Complete game implementation
├── README.md        # Project documentation
├── LICENSE          # Optional; add a chosen license
└── assets/          # Optional screenshots and cover art
```

The game logic, CSS, HTML structure, shader definitions, procedural textures, audio generation, and interface are contained in `index.html`.

The assets folder is optional and can be used for a trailer, screenshots, or future documentation images.

---

## ▶️ Run Locally

### Option 1: Open the HTML File

1. Download the repository.
2. Open `index.html` in a modern browser.
3. Ensure WebGL is supported and the Three.js CDN can be reached.

### Option 2: Use Python's Local HTTP Server

From the project directory, run:

```bash
python3 -m http.server 8000
```

Open the following URL:

```text
http://localhost:8000
```

No Node.js installation, package manager, or separate frontend build step is required.

### Important Dependency Note

Three.js r128 is loaded from cdnjs. The game therefore needs internet access to retrieve the 3D engine when it is not already available in the browser cache.

---

## 🌐 GitHub Pages Deployment

1. Create a GitHub repository named `lunar-courier-3d`.
2. Rename `Lunar Courier 3D.html` to `index.html`.
3. Upload `index.html` and `README.md` to the repository root.
4. Open **Settings → Pages**.
5. Choose deployment from the `main` branch and the root folder.
6. Save and wait for the deployment to finish.

The expected URL format is:

```text
https://YOUR_USERNAME.github.io/lunar-courier-3d/
```

The published demo is available at:

**https://punitpritam788.github.io/lunar-courier-3d/**

---

## 🎥 Gameplay Trailer and Screenshots

Add the gameplay trailer or screenshots here to help visitors understand the experience before opening the game.

- **Live demo:** https://punitpritam788.github.io/lunar-courier-3d/
- **Gameplay trailer:** Add your hosted trailer URL.
- **Repository:** Add your GitHub repository URL.

A good screenshot set would include the lunar environment, spacecraft boost effect, wave HUD, upgrade selection screen, and Solar Storm encounter.

---

## 🗺️ Future Roadmap

Possible future improvements include:

- Additional spacecraft and cosmetic customization.
- More environments and mission types.
- Expanded upgrade trees and new gameplay strategies.
- Additional hazards and encounter variations.
- Richer audio and music themes.
- More detailed mission statistics and challenge modes.
- Further performance testing on mobile devices and different browsers.
- Additional automated and manual gameplay testing.

These are proposed directions, not features claimed to be complete.

---

## 🧪 Testing and Compatibility

The game is designed for modern browsers that support WebGL and the browser APIs used by the implementation.

Useful areas for manual testing include:

- Keyboard movement and boost timing.
- Touch joystick behaviour and mobile layouts.
- Gamepad input and menu navigation.
- Pause, resume, restart, and quit flows.
- Sample collection and shield restoration.
- Wave progression and upgrade selection.
- Solar-flare warning and damage behaviour.
- Victory and failure sequences.
- Audio settings and persistent high scores.
- Performance under different graphics settings.

Compatibility and performance should be verified on the target devices before describing the project as universally supported.

---

## 🤝 Feedback and Community

Lunar Courier 3D is an independent game-development project exploring browser-based 3D graphics, procedural generation, game mechanics, and interactive storytelling.

If you try the game, feedback on the controls, gameplay balance, graphics, and performance is welcome.

If you enjoy the project, consider starring the repository and sharing it with other developers or game enthusiasts.

**What would you add next: more spacecraft, additional missions, deeper upgrades, or more challenging solar events?**

---

## 🙌 Credits

- **Three.js:** https://threejs.org/
- **GitHub Pages:** https://pages.github.com/
- **Web Audio API:** Browser-native audio generation.
- **Inspiration:** Lunar exploration and science-fiction space-survival games.

Lunar Courier 3D is an independent project and is not affiliated with or endorsed by NASA or any space agency.

---

## 📄 License

No open-source license is specified by this README. If you want others to reuse, modify, or redistribute the project, choose an appropriate license and add the corresponding `LICENSE` file before claiming that the project is open source.

---

### 🌕 The Mission Is Waiting

**[PLAY LUNAR COURIER 3D NOW](https://punitpritam788.github.io/lunar-courier-3d/)**

Built with curiosity, procedural graphics, and a love for browser game development. 🚀
