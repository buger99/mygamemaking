---
name: 가위바위보! Arcade Cabinet
description: An early-80s Pac-Man cabinet on a phone, with a lit marquee, a navy CRT and round arcade buttons, drawn in pixels and moving in steps.
colors:
  cab: "#ffcf1a"
  cab-deep: "#e9ac00"
  marquee: "#e5261d"
  wall: "#3442ff"
  deck: "#2b39e8"
  yellow: "#ffe14a"
  red: "#ff3b3b"
  pink: "#ffb8de"
  cyan: "#3ee8ff"
  orange: "#ffb347"
  ink: "#16112b"
  screen: "#0b0e3c"
  metal: "#cfd3df"
  white: "#ffffff"
  dim: "#aab3ff"
typography:
  display:
    fontFamily: "Galmuri11, Press Start 2P, monospace"
    fontSize: "44px"
    fontWeight: 400
    lineHeight: 1.15
    letterSpacing: "0.02em"
  headline:
    fontFamily: "Galmuri11, Press Start 2P, monospace"
    fontSize: "33px"
    fontWeight: 400
    lineHeight: 1.2
  title:
    fontFamily: "Galmuri11, Press Start 2P, monospace"
    fontSize: "22px"
    fontWeight: 400
    lineHeight: 1.2
  digits-xl:
    fontFamily: "Press Start 2P, Galmuri11, monospace"
    fontSize: "48px"
    fontWeight: 400
    lineHeight: 1
  digits-lg:
    fontFamily: "Press Start 2P, Galmuri11, monospace"
    fontSize: "32px"
    fontWeight: 400
    lineHeight: 1
    fontFeature: "tnum"
  digits-md:
    fontFamily: "Press Start 2P, Galmuri11, monospace"
    fontSize: "24px"
    fontWeight: 400
    lineHeight: 1
  digits-sm:
    fontFamily: "Press Start 2P, Galmuri11, monospace"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  body:
    fontFamily: "Galmuri11, Press Start 2P, monospace"
    fontSize: "0.95rem"
    fontWeight: 400
    lineHeight: 1.45
  label-button:
    fontFamily: "Galmuri11, Press Start 2P, monospace"
    fontSize: "1.05rem"
    fontWeight: 400
  label:
    fontFamily: "Galmuri11, Press Start 2P, monospace"
    fontSize: "0.8rem"
    fontWeight: 400
rounded:
  inner: "4px"
  frame: "6px"
  crt: "10px"
  dome: "50%"
spacing:
  xs: "4px"
  sm: "8px"
  md: "10px"
  lg: "12px"
  xl: "16px"
components:
  marquee:
    backgroundColor: "{colors.marquee}"
    textColor: "{colors.yellow}"
    typography: "{typography.display}"
    padding: "8px 10px 10px"
  crt-screen:
    backgroundColor: "{colors.screen}"
    textColor: "{colors.white}"
    rounded: "{rounded.crt}"
    padding: "16px 16px 14px"
  crt-bezel:
    backgroundColor: "{colors.ink}"
    rounded: "{rounded.frame}"
    padding: "8px"
  hud-score-me:
    textColor: "{colors.yellow}"
    typography: "{typography.digits-lg}"
  hud-score-cpu:
    textColor: "{colors.cyan}"
    typography: "{typography.digits-lg}"
  arena-vs:
    textColor: "{colors.red}"
    typography: "{typography.digits-md}"
  arena-countdown:
    textColor: "{colors.yellow}"
    typography: "{typography.digits-xl}"
  arena-countdown-hurry:
    textColor: "{colors.red}"
    typography: "{typography.digits-xl}"
  verdict-win:
    textColor: "{colors.yellow}"
    typography: "{typography.headline}"
    height: "44px"
  verdict-lose:
    textColor: "{colors.red}"
    typography: "{typography.headline}"
    height: "44px"
  verdict-draw:
    textColor: "{colors.white}"
    typography: "{typography.headline}"
    height: "44px"
  ghost-dialog:
    textColor: "{colors.white}"
    typography: "{typography.body}"
    rounded: "{rounded.inner}"
    padding: "8px 12px"
  control-deck:
    backgroundColor: "{colors.deck}"
    rounded: "{rounded.frame}"
    padding: "18px 10px 14px"
  arcade-button-scissors:
    backgroundColor: "{colors.red}"
    textColor: "{colors.white}"
    typography: "{typography.label-button}"
    rounded: "{rounded.dome}"
    width: "clamp(78px, 23vw, 96px)"
  arcade-button-rock:
    backgroundColor: "{colors.yellow}"
    textColor: "{colors.white}"
    typography: "{typography.label-button}"
    rounded: "{rounded.dome}"
    width: "clamp(78px, 23vw, 96px)"
  arcade-button-paper:
    backgroundColor: "{colors.pink}"
    textColor: "{colors.white}"
    typography: "{typography.label-button}"
    rounded: "{rounded.dome}"
    width: "clamp(78px, 23vw, 96px)"
  coin-door:
    backgroundColor: "{colors.metal}"
    rounded: "{rounded.frame}"
    padding: "10px"
  coin-door-switch:
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.inner}"
    padding: "9px 8px"
    height: "46px"
  coin-door-lamp-on:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.yellow}"
    typography: "{typography.digits-sm}"
    padding: "4px 5px"
  again-button:
    backgroundColor: "{colors.yellow}"
    textColor: "{colors.ink}"
    padding: "12px 26px"
  again-button-hover:
    backgroundColor: "{colors.white}"
    textColor: "{colors.ink}"
  banner:
    backgroundColor: "{colors.screen}"
    textColor: "{colors.orange}"
    typography: "{typography.headline}"
    padding: "12px 18px"
  final-screen:
    backgroundColor: "{colors.screen}"
    textColor: "{colors.yellow}"
    typography: "{typography.display}"
    padding: "20px"
---

# Design System: 가위바위보! Arcade Cabinet

## Overview

**Creative North Star: "The Cabinet in Your Pocket"**

The phone is the front of an early-80s arcade cabinet in the Pac-Man, Galaga and Donkey Kong line. The page stacks the way the machine does. A red marquee with chasing bulbs sits on top, a navy CRT screen framed in maze-blue walls fills the middle, a blue control deck with three round arcade buttons sits in the thumb zone, and a steel coin door holds the switches. The cabinet body behind everything is Pac-Man yellow, with a faint maze-and-dots side-art tiled across it.

Everything is made of pixels and ink. Objects have solid ink outlines. Shadows are hard and unblurred. Sprites (hands, the ghost CPU, trophy, flame) are drawn on canvas from character maps and enlarged only by whole numbers. Motion jumps from frame to frame with `steps()` the way old hardware does; nothing eases. The world stays bright. The only dark surface is the CRT glass, and it is navy rather than black, so the game reads as a lit cabinet in a bright room and never as something dark or scary.

The density is cabinet-tight: one column, max 460px wide, with fixed-height zones so a result never pushes the controls around.

**Key Characteristics:**
- Yellow cabinet body, red lit marquee, navy CRT, blue deck, steel coin door, stacked top to bottom.
- Ink outlines on every object; hard, zero-blur shadows only.
- Two pixel faces: Galmuri11 for Hangul, Press Start 2P for digits and Latin.
- Canvas pixel sprites at integer scales only.
- Every animation and transition is stepped.
- Ghost colors (red, pink, cyan, orange) plus power-pellet yellow are the accent voice.

## Colors

A bright arcade palette: a saturated yellow body, a red sign, maze blues, the four ghost colors, and one deep ink that outlines everything.

### Primary
- **Pac-Man Cabinet Yellow** (cab): the body of the machine and the page background. It carries the maze side-art, drawn in a slightly deeper yellow (#ebb100) as square-capped 4px walls and 4px pellet dots on a 128px tile.
- **Cabinet Shadow Gold** (cab-deep): the darker body tone, for shade and pellets on the cabinet.

### Secondary
- **Lit Marquee Red** (marquee): the sign panel behind the title, ringed inside by a 3px power-pellet yellow trim.
- **Maze Wall Blue** (wall): the double wall around the CRT (border plus inset outline) and the color the walls flash white on a win.
- **Control Deck Blue** (deck): the button panel. A deeper well blue (#10178f) rings each arcade button.

### Tertiary
- **Power Pellet Yellow** (yellow): the "lit" color. Bulbs, the title, the player's score, the countdown, win verdicts, active lamps, and the 다시 하기 button.
- **Blinky Red** (red): the VS mark, lose verdicts, the hurry countdown, GAME OVER, and the scissors button.
- **Pinky Pink** (pink): the player's side labels, cheer lines, the paper button, and the focus ring on the final screen.
- **Inky Cyan** (cyan): the computer's side labels and score, and the lose-screen headline.
- **Clyde Orange** (orange): the streak banner frame and text, and the hot streak counter.

### Neutral
- **Cabinet Ink** (ink): every outline, the CRT bezel, text on light surfaces, lamp housings, and the selection background.
- **CRT Navy** (screen): the screen glass, the banner fill, and the final screen. Never pure black.
- **Coin-Door Steel** (metal): the coin-door plate. Its switches sit on a lighter steel face (#e8ebf3).
- **Phosphor White** (white): primary text on the CRT, dialog frame, and the wall flash.
- **Dim Phosphor** (dim): secondary text on the CRT (best record line, the 5-round goal line).

### Named Rules
**The Lit Cabinet Rule.** The cabinet is bright and the CRT is the only dark surface. Dark navy lives inside the bezel and nowhere else.

**The Ghost Sides Rule.** The player's side speaks in pink and yellow, and the computer's side speaks in cyan. Keep that split on every surface that shows both sides.

**The Ink Outline Rule.** Every object on the cabinet has a solid ink edge: 4px on cabinet panels and domes, 3px on inner frames and switches, 2px rings on bulbs and sparks.

## Typography

**Display Font:** Galmuri11 (with Press Start 2P, monospace)
**Body Font:** Galmuri11 (with Press Start 2P, monospace)
**Label/Mono Font:** Press Start 2P (with Galmuri11, monospace) for digits and Latin

**Character:** Two self-hosted OFL pixel faces split by script. Galmuri11 carries all Korean copy, and Press Start 2P carries scores, countdowns, VS, ON/OFF and GAME OVER, so numbers look like they came out of the machine's own ROM. Weight is always regular. Pixel faces get their emphasis from size and color, never bold.

### Hierarchy
- **Display** (400, 44px, 1.15): the marquee title 가위바위보! and the final-screen headline. The title has a 3px eight-way ink outline plus a hard ink drop, like an arcade logo. Steps down to 33px on short or narrow screens.
- **Headline** (400, 33px, 1.2): round verdicts (이겼다 / 졌다 / 비겼다) and the streak banner.
- **Title** (400, 22px): the idle prompt, long verdicts, long banners, and the 준비 state in the VS slot.
- **Digits XL / LG / MD / SM** (Press Start 2P, 48 / 32 / 24 / 16px, line-height 1): countdown digit / HUD scores (tabular) / VS / best record, lamps, final score and GAME OVER.
- **Body** (400, 0.95rem, 1.45): the ghost's dialog line, HUD labels, switch labels, banner sub-lines.
- **Label** (400, 0.8rem to 1.05rem): the goal line and best-record caption (0.8rem, dim), and arcade-button captions (1.05rem, white with a 2px hard ink drop).

### Named Rules
**The Script Split Rule.** Hangul is set in Galmuri11, and digits and Latin are set in Press Start 2P. A mixed line switches face per run (e.g. 최고 **0** 연승), and neither face is bolded.

**The Pixel Ladder Rule.** Display and digit sizes sit on whole-pixel rungs of each face's grid. Press Start 2P uses multiples of 8 (16, 24, 32, 48) and Galmuri11 display uses multiples of 11 (22, 33, 44). To shrink, drop a whole rung (44 to 33), never to an in-between size. Reading copy (body and label) is the one exception: it uses rem sizes so it scales with the user's text setting.

## Layout

A single centered column (100% up to 460px) on the yellow body, top-anchored with 10px 16px page padding, and 10px gaps between the four cabinet parts: marquee, CRT, deck, coin door. Inside the CRT a vertical stack with 10px gaps runs HUD, goal line, arena, verdict, dialog, then the timer track.

- **HUD:** a three-column grid (`1fr auto 1fr`) with the player on the left, best and current streak in the center, and the computer right-aligned.
- **Arena:** the same three-column grid with a fixed height of `clamp(118px, 30vw, 140px)`. Player sprite, VS/countdown, CPU sprite (mirrored).
- **Verdict:** fixed 44px tall. Long strings drop to the 22px rung instead of wrapping.
- **Deck:** a three-column grid of equal arcade buttons, 8px gaps. **Coin door:** a `3fr 2fr` grid holding the speed and sound switches.
- **Overlays:** the banner and the final screen are positioned inside the CRT, so results always appear on the screen and never as page-level modals.

Spacing works on a small rhythm of 4, 8, 10, 12 and 16px. The buttons add their own larger gaps (22px dome-to-label, 18px deck top padding) for the physical skirt.

Responsive behavior: at ≥600px wide, arena sprites go from ×4 to ×5. Short wide screens (≥600px wide and ≤780px tall, i.e. laptops and projectors) tighten the stack: title to 33px, arena 108px with sprites back to ×4, domes 76px, smaller deck and coin-door padding. Below 360px wide, the title and final headline drop to 33px.

### Named Rules
**The Fixed Arena Rule.** Everything that changes per round (sprites, countdown, verdict, dialog line) lives in a fixed-height slot. The deck and coin door never move when a result appears.

## Elevation & Depth

Depth comes from physical layering and hard shadows, never from blur. Panels sit flat on the body, and the CRT sits recessed inside an ink bezel. The arcade domes are the only things that stand proud: each has a solid ink skirt below it and a deep-blue well ring around it, and pressing a dome pushes it down into its skirt. The scanline overlay (a 4px hard-stop white stripe at 4.5% opacity) gives the glass its texture.

### Shadow Vocabulary
- **Dome skirt** (`box-shadow: 0 0 0 6px #10178f, 0 9px 0 6px var(--ink)`; pressed `0 0 0 6px #10178f, 0 3px 0 6px var(--ink)` with `translateY(6px)`): the arcade buttons only.
- **Marquee trim** (`box-shadow: inset 0 0 0 3px var(--yellow)`): the lit inner edge of the sign.
- **Ink ring** (`box-shadow: 0 0 0 2px var(--ink)`): marquee bulbs and pixel sparks.
- **Logo extrusion** (eight 3px ink text-shadows plus `5px 6px 0 var(--ink)`): the marquee title only.
- **Caption drop** (`text-shadow: 2px 2px 0 var(--ink)`): white captions under the arcade buttons, set on deck blue.
- **Double wall** (3px wall border plus 3px wall outline at -9px offset): the CRT frame. The banner uses an orange border with an ink outline in the same way.

### Named Rules
**The Hard Edge Rule.** Every shadow, ring and gradient stop has zero blur. A gradient is allowed only as a hard-stop pixel fill (scanlines, the dome's highlight disc), never as a soft fade or glow.

## Shapes

Square pixel geometry in rounded cabinet housings. Radii follow the hardware: the CRT glass curves the most (10px), cabinet panels and the bezel are slightly rounded (6px), and inner frames such as the dialog and switches are barely softened (4px). The arcade buttons are the only circles. Each dome face is a flat disc with a hard-stop lower shade and a small square highlight in its upper left. Pixel elements (bulbs, sparks, lamps, the timer track, the banner, 다시 하기) are square-cornered.

### Named Rules
**The Integer Sprite Rule.** Canvas sprites are drawn one character per pixel and displayed at `width = columns × scale` with `image-rendering: pixelated`. Scale is always a whole number (×2 streak flame, ×3 dome hands, dialog ghost and banner flame, ×4 to ×5 arena hands, ×8 final trophy or ghost). Sprites 8 columns wide or narrower are drawn at double columns first. A fractional scale is never allowed.

## Components

Chunky, outlined and mechanical. Every control looks like a part you could unscrew from a cabinet.

### Motion Grammar
**The Steps-Only Rule.** Every animation and transition uses `steps()`. Bulbs chase in `steps(1)` at 1.2s (0.3s in party mode), domes press in `.06s steps(1)`, sprites land in `steps(3)`, scores and verdicts blink with `steps(1)`, the final trophy hops in `steps(2)`, sparks fly in `steps(16)`, and the cabinet shakes in `steps(8)`. `prefers-reduced-motion` turns off every animation and transition.

### Buttons
- **Arcade buttons (가위 / 바위 / 보):** a circular dome (`clamp(78px, 23vw, 96px)`, 76px on short screens) with a 4px ink border, a deep-blue well ring and an ink skirt, carrying a ×3 hand sprite. Each hand has its own color, with a light highlight and a dark lower shade: scissors red, rock power-pellet yellow, paper pink. A white Galmuri11 caption sits 22px below.
- **Hover / Active / Focus:** hover (pointer devices only) brightens the dome by 8%. Active pushes the dome down 6px into its skirt. Focus draws a 4px dashed white ring 10px outside the dome. Disabled domes desaturate (`saturate(.35) brightness(.85)`).
- **Restart (다시 하기):** square, yellow with ink text and a 3px white border, 12px 26px padding. Hover turns it white, active nudges it 2px down, focus draws a 4px dashed pink ring.

### Coin-Door Switches
- **Style:** light steel face, 3px ink border, 4px radius, minimum height 46px, with a Galmuri11 label and an inset ink lamp holding Press Start 2P ON/OFF.
- **State:** lamp text is grey (#8d93a8) when off and power-pellet yellow when lit. The speed switch is `role="switch"`, and sound is a pressed toggle. Active nudges the switch 2px down, and focus draws a 4px dashed ink ring.

### Marquee
A red sign with a 4px ink border and a yellow inner trim. A row of 8px square bulbs runs above and below the title, chasing between yellow and white in three phases.

### CRT Screen
An ink bezel (8px padding, 6px radius) holds the navy glass with a double maze-blue wall and scanlines. A win flashes the walls white three times. A loss flashes the glass deep maroon (#4a0d2e) once.

### HUD and Arena
HUD labels are set in Galmuri11 and scores in Press Start 2P, with the player in yellow and the computer in cyan. Scores blink three times when they change. The arena shows the two hand sprites facing each other, with the VS mark between them. In speed mode the VS mark becomes the 48px countdown digit, which turns red at 1, while a 10px timer track below the dialog drains from yellow to red. Before the first round both slots show a "?" sprite.

### Verdict and Ghost Dialog
The verdict is a single 44px-tall line: yellow for a win, red for a loss, white for a draw, and a slow yellow blink while idle. Below it the ghost dialog has a 3px white frame and 4px radius, with the ×3 red ghost sprite (or its scared form) beside the computer's line.

### Banner and Final Screens
The streak banner appears over the CRT on a navy fill with a 4px orange border and 4px ink outline. It holds an orange headline with a flame sprite and a white sub-line, blinks in, holds, and clears in `steps(1)`. The final screen covers the whole CRT. On a win it shows a ×8 hopping trophy and a headline cycling yellow, pink, cyan and orange. On a loss it shows a ×8 ghost, a cyan headline and red GAME OVER. Both show the final score in Press Start 2P and the 다시 하기 button.

### Pixel Sparks
Celebrations throw 8px or 12px square sparks in ghost colors, power-pellet yellow and white, each with a 2px ink ring. Their travel snaps to a 4px grid and they fall in `steps(16)`.

## Do's and Don'ts

### Do:
- **Do** outline every new object in ink: 4px on panels and domes, 3px on inner frames, 2px rings on small pixel bits.
- **Do** set Hangul in Galmuri11 and digits and Latin in Press Start 2P, at regular weight, on the 8px and 11px ladders (16/24/32/48 and 22/33/44).
- **Do** draw new imagery as canvas pixel sprites from the shared palette, scaled by whole numbers only.
- **Do** animate with `steps()` and respect `prefers-reduced-motion` by switching animation off.
- **Do** put new per-round content into fixed-height slots on the CRT so the deck never moves.
- **Do** keep the player's side pink and yellow and the computer's side cyan.

### Don't:
- **Don't** blur anything: no soft box-shadows, glows, or smooth gradients. Hard-stop fills and zero-blur offsets only.
- **Don't** ease motion with `ease`, `linear` tweening or cubic-bezier curves.
- **Don't** use emoji, icon fonts or system glyphs as imagery. Hands, ghost, trophy and flame are pixel sprites.
- **Don't** darken the cabinet. Navy belongs to the CRT glass, and the page never goes black.
- **Don't** scale sprites by fractional amounts or let the browser smooth them.
- **Don't** bold either pixel face or set display and digit text at sizes between ladder rungs.
