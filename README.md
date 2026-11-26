# Joint Space

Joint Space is an interactive, single-page course on hexapod leg kinematics. It walks through angles and `atan2`, forward kinematics, two-link and three-joint inverse kinematics, the coxa/femur/tibia split, and a simple walking gait, one short step per screen with a live drawing to drag and quick checks along the way. It ends with code you can copy in Python, JavaScript, C++, C#, Rust or Go. It uses the real leg of my [VANTA hexapod](https://github.com/Built-By-Gio/vanta-hexapod): coxa 68 mm, femur 76.7 mm, tibia 101 mm.

Built by Gio ([Built-By-Gio](https://github.com/Built-By-Gio)).

## Status (2026-11-25)

Working:
- Built on 2026-11-06 as one HTML file.
- The Python and JavaScript inverse-kinematics code samples pass random round-trip tests, FK(IK(p)) == p: about 26,000 in Python and 20,000 in JavaScript, with zero failures (run on 2026-11-06).

Not compiled yet:
- The C++, C#, Rust and Go samples. They are line-for-line ports of the tested Python and JavaScript code.

Notes:
- The leg mount directions follow the VANTA URDF, with the body's +y axis forward and each coxa mount pointing radially outward.

## What you need

- A modern web browser.
- An internet connection when the page loads, for these external files:
  - [anime.js](https://animejs.com/) 3.2.2 from cdnjs: `https://cdnjs.cloudflare.com/ajax/libs/animejs/3.2.2/anime.min.js`
  - Google Fonts (Outfit, IBM Plex Sans, IBM Plex Mono): `https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;800&family=IBM+Plex+Sans:wght@400;500&family=IBM+Plex+Mono:wght@400;500&display=swap`

Nothing to install and no build step.

## How to run

1. Download or clone this repo.
2. Open `index.html` in your browser (double-click it, or drag it into a browser window).
3. Use Back/Next to move through the steps. Your place in the course, finished steps and chosen code language are saved in your browser's local storage only. The "Start over" button at the bottom removes them.

## Repo layout

```
index.html   the whole app: page, styles, drawings, solver and code samples
```

## Roadmap / future plans

Nothing else planned for now.

## Credits and license

- Animation: [anime.js](https://github.com/juliangarnier/anime) by Julian Garnier (MIT License), loaded from cdnjs.
- Fonts: Outfit, IBM Plex Sans and IBM Plex Mono (SIL Open Font License), loaded from Google Fonts.
- Leg dimensions come from my [VANTA hexapod](https://github.com/Built-By-Gio/vanta-hexapod).

This project is released under the MIT License. See `LICENSE`.
