# Project structure

```
boredum-busters/
├── index.html                  The entire website: HTML, CSS and JavaScript in one file
├── media/
│   └── fill.mp4                Fill-loader video used by the intro and the phone mockup (1 MB)
│
├── brand-kit/
│   ├── identity/
│   │   └── Boredum-Busters-Brand-Identity.pdf     10-page vector brand book (editable text, embedded fonts)
│   │
│   ├── logo/
│   │   ├── svg/                Vector masters, scale to any size
│   │   │   ├── boredum-busters-mark-white.svg     For dark backgrounds
│   │   │   ├── boredum-busters-mark-black.svg     For light backgrounds
│   │   │   └── boredum-busters-mark-orange.svg    Accent use only
│   │   └── png/                Transparent 2048 px exports, plus the store icon
│   │       ├── boredum-busters-mark-white-2048.png
│   │       ├── boredum-busters-mark-black-2048.png
│   │       ├── boredum-busters-mark-orange-2048.png
│   │       └── boredum-busters-app-icon-1024.png  White mark on black, store-ready
│   │
│   ├── loading-animations/     4-second seamless loops
│   │   ├── boredum-busters-fill-loader-4K.mp4         2160x2160, 60 fps
│   │   ├── boredum-busters-fill-loader-1080.gif
│   │   ├── boredum-busters-controller-loader-4K.mp4   2160x2160, 60 fps
│   │   └── boredum-busters-controller-loader-1080.gif
│   │
│   ├── board-images/           2x PNG of each page of the identity PDF, for quick sharing
│   │   ├── 01-Brand-cover.png
│   │   ├── 02-Logo-system.png
│   │   ├── 03-Color.png
│   │   ├── 04-Typography-and-voice.png
│   │   ├── 05-App-icon-and-store-page.png
│   │   ├── 06-Social-and-web.png
│   │   ├── 07-Game-launch-assets.png
│   │   ├── 08-Merch-and-print.png
│   │   ├── 09-Loading-animation.png
│   │   └── 10-Simple-fill-loader.png
│   │
│   └── fonts/                  Web font files (.woff2) and SIL Open Font Licenses
│       ├── unbounded-latin-500/700/900-normal.woff2
│       ├── manrope-latin-400/600/800-normal.woff2
│       ├── Unbounded-LICENSE.txt
│       └── Manrope-LICENSE.txt
│
├── README.md                   Repository front page: what the site does and what to fill in
├── STRUCTURE.md                This file
├── UPLOAD_INSTRUCTIONS.md      How to put this on GitHub and turn on the free live link
└── .gitignore                  Keeps system junk files out of the repository
```

## How `index.html` is organised

The file is self-contained. Fonts load from Google Fonts. Its only local dependency is `media/fill.mp4`, which must stay next to it in the `media/` folder.

Inside the `<script>` at the bottom, each feature is a labelled block (search for the `=====` banners):

| Block | What it controls |
|---|---|
| `PRELOAD (fill loader) -> HERO` | The intro counter and the logo hand-off into the hero |
| `MASCOT` | Eye tracking, blinking, speech bubbles, the 10-click burst and the baby |
| `CURSOR` | The crosshair and click hit-markers |
| `DRAG SLASH TRAIL` | The orange trail and sparks when dragging |
| `TILT + MAGNET` | 3D card tilt and magnetic buttons |
| `XP BAR + LEVEL` | Scroll progress and the level label in the top bar |
| `LIGHT / DARK` | The theme switch |
| `STORE BUTTONS` | App Store and Google Play buttons |
| `ARCADE` | All four mini-games, the Random game button and the sound switch |
| `CHEAT CODE` | The keyboard code, the mobile gamepad and the three cheats |
| `PITCH FORM` | Form validation and summary (connect a form service here) |

Colours and fonts are CSS variables at the top of the `<style>` block (`--ink`, `--white`, `--orange` and so on). Change them there to restyle the whole site.
