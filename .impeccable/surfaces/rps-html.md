---
version: 1
slug: "rps-html"
primary_target: "rps.html"
related_targets: []
---

# rps.html surface brief

Scope: rps.html, the whole game screen. Visitor mode: Experience (the player is inside the game).
Audience and job: classmates in class or presentations, mostly on phones (portrait, touch), sometimes projected. Job: play rounds against the computer and enjoy each outcome.
Constraints: keep every feature (scoreboard, final screen, streak + best, chatty computer, speed mode, sound + mute, win/lose effects). Bright and fun, never dark or scary. Korean UI copy.
Critique inputs: fix the layout jump (result below buttons), low-contrast lilac text, and false-affordance streak chip as part of the redesign. Speed-mode clarity and the best-of-5 rule change come in later passes.

## Direction contract

THESIS: The phone is the front of an early-80s arcade cabinet (Pac-Man, Galaga, Donkey Kong at the craft bar): marquee on top, CRT screen in the middle, control deck with round arcade buttons at the bottom. It refuses the pastel sticker card stack and the layout where the result pushes the buttons around.

OWN-WORLD: Pac-Man cabinet yellow body with a faint maze side-art; red lit marquee with chasing bulbs; navy CRT screen framed by maze-blue double walls, light scanlines; ghost red, pink, cyan and orange as accents; ink outlines; Press Start 2P for digits and Latin, Galmuri11 for Hangul; pixel sprites drawn on canvas (hands, ghost CPU, trophy, flame); square pixel sparks; every motion uses steps().

STORY: The player sees two "?" slots and a ghost saying hello, taps a big arcade button, watches the CPU slot shuffle and land, reads the verdict and the ghost's line in a dialog box, then plays again until a champion or game-over screen appears on the CRT.

FIRST VIEWPORT: Top: marquee with the title 가위바위보! (about 10% height). Middle: CRT screen (about 45%), with a HUD row (나 score, best streak, 컴퓨터 score), an arena (my sprite, VS or the big countdown digit, the CPU sprite), the verdict line, and the ghost dialog box. Bottom: control deck with three round buttons (가위, 바위, 보) in the thumb zone, and a coin-door strip with the speed mode and sound switches.

FORM: canon direction (user chose the standing exit "정통 8비트 오락실", bar: Pac-Man, Galaga, Donkey Kong cabinets); degraded roll, seed 74c9267e; code-led.

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
