# Godot 3D Character Controller Template

<img width="1183" height="607" alt="image" src="https://github.com/user-attachments/assets/f27e9077-11c6-4aa7-917a-8c13f00ee35c" />

This repository provides a robust, ready-to-use first-person 3D character controller for Godot Engine. It is designed to be easily integrated into your own Godot projects, with a focus on smooth movement, sprinting, crouching, sliding, jumping, and head-bobbing effects.

## Features

- **First-person movement**: Walk, sprint, crouch, slide, and jump with smooth transitions.
- **Head bobbing**: Realistic camera movement for immersion.
- **Free look**: Look around independently while sliding or crouching.
- **Customizable speeds**: Easily adjust walking, sprinting, and crouching speeds.
- **Aggressive/soft landing animations**: Responsive to fall velocity.
- **Easy integration**: The entire controller is self-contained in the red `Player` folder.

## Quick Start / Setup

1. **Copy the Player Folder**
	- The red `Scenes/Player` folder contains everything you need for the character controller.
	- Copy the entire `Player` folder into your own Godot project (keep the folder structure).

<img width="265" height="156" alt="image" src="https://github.com/user-attachments/assets/a8cc33a4-7af6-4ed6-9dc7-17c1563e828b" />


2. **Add the Player Scene to Your World**
	- In your main scene, instance the `player.tscn` scene from `Scenes/Player`.
	- Position it as needed in your world.

3. **Input Map Setup**
	- The following input actions are required (already set up in this template's `project.godot`):
	  - `forward` (default: W)
	  - `backward` (default: S)
	  - `left` (default: A)
	  - `right` (default: D)
	  - `sprint` (default: Shift)
	  - `crouch` (default: C)
	  - `ui_accept` (default: Space, for jump)
	- If you copy the controller to a new project, make sure to add these actions in **Project > Project Settings > Input Map**.


<img width="1194" height="428" alt="image" src="https://github.com/user-attachments/assets/8c05d251-8710-4d4f-80a0-7499e67c47e2" />


4. **Test the Controller**
	- Press play. Use WASD to move, Shift to sprint, C to crouch/slide, and Space to jump.

## How It Works

The controller is implemented in `Player.gd` (attached to `player.tscn`).

- **Movement**: Uses Godot's `CharacterBody3D` for physics-based movement. Handles walking, sprinting, crouching, and sliding states.
- **Camera/Head**: Mouse look is handled by rotating the head and neck nodes. Free look is enabled during sliding/crouching.
- **Head Bobbing**: Simulates natural camera movement while walking, sprinting, or crouching.
- **Jumping & Gravity**: Jumping is handled with velocity changes; gravity is synced with project settings.
- **Collisions**: Uses separate collision shapes for standing and crouching.
- **Animations**: Plays jump and landing animations for added feedback.

## Folder Structure

```
Scenes/
  Player/
	 Player.gd         # Main controller script
	 player.tscn       # Player scene (instanciate this)
	 ...               # Supporting nodes/resources
```

## Customization

- All movement speeds, head bobbing, and mouse sensitivity are exposed as exported variables in the `Player.gd` script for easy tuning in the Godot editor.
- You can further expand the controller with your own features (e.g., add weapons, inventory, etc.).

## Credits

Created by [RasyaDevansyah](https://github.com/RasyaDevansyah)

---

Feel free to use, modify, and share this template in your own Godot projects!

