<p align="center">
  <img src="Assets/game%20icon.png" alt="ESC key icon" width="220">
</p>

<h1 align="center">ESC to Escape</h1>

<p align="center">
  <i>It's all a dream.</i><br>
  A first-person 3D puzzle platformer where the pause button is part of the puzzle.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Unity-6000.0.66f1-000000?logo=unity&logoColor=white" alt="Unity 6">
  <img src="https://img.shields.io/badge/C%23-239120?logo=csharp&logoColor=white" alt="C#">
  <img src="https://img.shields.io/badge/Render_Pipeline-URP-222222" alt="URP">
  <img src="https://img.shields.io/badge/Tuwaiq_Academy-3--week_course-5B2C83" alt="Tuwaiq Academy">
</p>

---

Three of us built this game in **three weeks** for Tuwaiq Academy's game design and programming course.

## The idea

In most games, pressing **ESC** stops everything and opens a menu. Here, ESC **freezes time inside the level**. Lasers stop mid-sweep, turrets hold their fire, and the pause menu appears in front of you as **physical blocks**: *Resume*, *Settings* and *Exit*. You can pick them up, carry them, rotate them and throw them. To unpause, you press ESC again or walk into the Resume block.

The game asks you to use the pause button as a tool to get through each stage.

## Gameplay

- **3 stages** linked by teleporters, ending back at the main menu
- **Hazards:** sweeping lasers, rotating turrets that fire bullets, spinning blades and bridges that blink out from under you
- **Movement:** walking, jumping, automatic ledge vaulting, head bob, and walk and strafe animations
- **Physics interaction:** pick up, rotate and throw objects with outline highlighting
- **Death counter** and fade-to-black respawns, with sound effects for jumps, pickups, teleports and the time freeze
- **Settings** for audio and mouse sensitivity, saved between sessions

## Controls

| Key | Action |
|---|---|
| `W` `A` `S` `D` | Move |
| Mouse | Look around |
| `Space` | Jump |
| `Esc` | Freeze time and spawn the menu blocks |
| `E` | Pick up / drop the block you're looking at |
| Hold `R` + mouse | Rotate the held block |
| Left click | Throw the held block |

## Open the project

1. Install **Unity 6000.0.66f1** (Unity 6) through Unity Hub.
2. Clone the repository:
   ```bash
   git clone https://github.com/SultanAbdulaziz/TuwaiqProgramGame_ESC_to_Escape.git
   ```
3. In Unity Hub, choose **Add → Add project from disk** and select the cloned folder.
4. Open `Assets/Scenes/Menu.unity` and press **Play**.

> The repository is large (~730 MB) because it includes art, audio and asset-store packages.

## Code tour

All gameplay scripts are in [`Assets/Scripts`](Assets/Scripts):

| Script | Responsibility |
|---|---|
| `GameManager.cs` | Singleton that tracks the stage, the time-freeze state and saved settings |
| `PlayerManager.cs` | Movement, jumping, ESC handling, spawning the menu blocks, death and teleport triggers |
| `ObjectHoldManager.cs` | Raycast pickup, holding, rotating and throwing physics objects |
| `LaserManager.cs` | Lasers moving between two points that pause while time is frozen |
| `TurretManager.cs` | Rotating turrets that fire bullets while time runs |
| `BridgeController.cs` | Bridges that blink, disappear and come back |
| `Vaulting.cs` | Ledge detection and climbing |
| `HUDManager.cs` | Interaction prompts, fade transitions, settings panel and death counter |
| `AudioManager.cs`, `MusicManager.cs` | Sound effects and background music |

## Team

- [Sultan Aleidan](https://github.com/SultanAbdulaziz)
- Turki
- Ziyad

## Credits

Environment art, skyboxes, turrets, obstacles, UI buttons and the outline effect come from free Unity Asset Store packs. They're in [`Assets/Downloads`](Assets/Downloads) and belong to their respective authors.
