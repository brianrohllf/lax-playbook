# Ossining Women's Lacrosse Playbook

An interactive, animated playbook for the Ossining high school women's lacrosse program. Built as a single self-contained HTML file — no internet connection, no server, and no dependencies required.

## Features

- **Animated X's and O's** — watch plays unfold in real time with smooth keyframe interpolation
- **7 offensive players** (M1–M3, A1–A4) in a 3-2-2 formation, plus **8 defenders** (D1–D7, G)
- **Show/hide offense and defense** independently with toggle checkboxes
- **Playback controls** — play, pause, reset, scrub, and adjust speed (0.5x–2x)
- **Movement paths** with dashed trails and directional arrows (color-coded by team)
- **Ball tracking** — ball follows the carrier and animates passes between players
- **Annotations** — coaching notes appear on screen at each keyframe
- **Built-in edit mode** — drag players, add/delete keyframes, set ball carriers, and edit annotations directly in the browser
- **Create and delete plays** from within the app
- **Auto-save** — all edits are saved to localStorage automatically
- **Save to File** — download an updated HTML file with your changes baked in
- **Fully offline** — works without any internet connection

## Plays Included

| Play | Category | Concept |
|------|----------|---------|
| Skittles | Settled | Pick & roll — A4/A2 two-man game at GLE |
| Nike | Settled | Ball reversal to settle the offense |
| Syracuse | Motion | Weave with pass-or-screen exchanges |
| Carolina | Motion | CCW attack wheel — drive and dish cycle |
| T-Bone | Stack | Picket fence — cutters peel off stack around 8m arc |
| Mercy | ISO | Clear out — create a wide driving lane for M3 |

## How to Use

1. Open `index.html` (or `playbook.html`) in any modern browser
2. Select a play from the sidebar
3. Press **Play** or hit **Space** to animate
4. Use the scrubber to jump to any point in the play
5. Toggle **Off** / **Def** checkboxes to show or hide teams
6. Toggle **Paths** to show or hide movement trails

## Editing Plays

1. Click **Edit** (or press **E**) to enter edit mode
2. **Drag any player** (offense or defense) to reposition them at the current keyframe
3. Use **Prev / Next** (or arrow keys) to navigate between keyframes
4. **+ Add KF** inserts a new keyframe; **× Del KF** removes the current one
5. Set the **ball carrier**, **time**, and **annotation** for each keyframe
6. Edit play metadata (name, category, formation, description, coaching notes) in the details panel
7. Click **Save to File** to download your updated playbook

## Creating New Plays

1. Click **+ New Play** at the bottom of the sidebar
2. All players start in the base 3-2-2 formation with 3 starter keyframes
3. Rename the play and set its category in the metadata editor
4. Drag players at each keyframe to choreograph the play

## Hosting on Google Sites

To share the playbook with your team via Google Sites:

1. Upload `index.html` to a **GitHub repository** (public)
2. Enable **GitHub Pages** in the repo's Settings → Pages
3. Copy the live URL (e.g. `https://yourname.github.io/ossining-playbook/`)
4. In Google Sites, use **Insert → Embed → By URL** and paste the link
5. Resize the embed to fill the page

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| Space | Play / Pause |
| R | Reset to start |
| E | Toggle edit mode |
| ← / → | Previous / Next keyframe (edit mode) |

## Technical Notes

- Single HTML file — all CSS, JS, and play data are self-contained
- Canvas-based rendering with a women's lacrosse field (8m arc, 12m fan, goal circle, GLE, restraining line)
- Field coordinates are in yards (70 × 44 visible area)
- Keyframes use sparse storage — only changed positions are stored per keyframe, resolved by accumulating from base formations
- Eased interpolation between keyframes for natural-looking movement
- Touch support for tablet/iPad editing
