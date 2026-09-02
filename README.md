# Spinning N64 Logo Demo ROM File

Interactive 3D homebrew demo of the classic multicolor **Nintendo 64** logo mark.

## Features

1. **Auto-rotate** on by default (smooth spin).
2. **A** toggles auto ↔ manual. Moving the **Control Stick** also switches to manual and orbits yaw/pitch.
3. **Zoom** with C-Up / C-Down (D-Pad up/down also works).
4. **Graphic modes** (L / C-Left):
   - Smooth lit (default Y/G/R/B logo colors)
   - Flat / unlit (`T3D_FLAG_NO_LIGHT`)
   - **Chrome / reflective** via `t3d_state_set_vertex_fx(T3D_VERTEX_FX_SPHERICAL_UV, …)` + env map
   - Cel shade (`T3D_VERTEX_FX_CELSHADE_COLOR`)
5. **Lighting demos** (R / C-Right) using real Tiny3D light APIs:
   - Single key
   - Two-point key + fill
   - Rim / back light
   - Orbiting + color-shifting lights

<br>

## Controls

| Input | Action |
|-------|--------|
| **A** | Toggle auto-rotate ↔ manual |
| **Stick** | Orbit yaw/pitch (manual; also enters manual) |
| **C-Up / C-Down** | Zoom in / out |
| **D-Pad Up / Down** | Zoom (optional) |
| **L / C-Left** | Cycle graphic mode |
| **R / C-Right** | Cycle lighting demo |
| **START** | Reset view + auto-rotate on |
| **B** | Reverse spin direction |
| **Z** | Show / hide the status + control lines |

## Project layout

```
n64-logo-demo/
  Makefile
  README.md
  TOOLCHAIN.md
  src/main.c
  assets/n64logo.glb      # Sketchfab CC-BY-4.0 N64 logo
  assets/envmap.png       # spherical env map for chrome mode
```


The Filt: `n64_logo_demo.z64`

But wait, there's more. 

Also created is `n64_logo_demo.n64` which has the data in reverse.

<br>

### Run

Tested on Ares, should work on real hardware / flashcart.

###
N64 Logo is property of Nintendo. This is a demonstration of their 3D model that resembles their logo; no Nintendo assets or code were used in this project.
