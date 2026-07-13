# React 3D · Hello World

A minimal 3D "Hello World" environment built with **React** and **react-three-fiber** (a React renderer for **Three.js**).

## What's in the scene

- A floating **"Hello, World!"** 3D text label
- A spinning, interactive cube (hover to recolor, click to grow)
- A starfield background
- Orbit controls — drag to rotate, scroll to zoom

## Run it

No build step and no install required. Just open the file in a browser:

```bash
# from the project root
open index.html          # macOS
# or serve it locally (recommended, avoids any module/CORS quirks):
python3 -m http.server 8000
# then visit http://localhost:8000
```

> The page loads React, Three.js, and react-three-fiber from an ESM CDN via an
> [import map](https://developer.mozilla.org/docs/Web/HTML/Element/script/type/importmap),
> so an internet connection is needed the first time you open it.

## Tech

| Library | Role |
| --- | --- |
| `react` / `react-dom` | UI runtime |
| `three` | WebGL / 3D engine |
| `@react-three/fiber` | React renderer for Three.js |
| `@react-three/drei` | Helpers (`Text`, `OrbitControls`, `Stars`, `Float`) |

## Customize

Everything lives in `index.html`:

- Change the greeting in the `HelloText` component.
- Swap `boxGeometry` for `sphereGeometry`, `torusKnotGeometry`, etc. in `SpinningCube`.
- Adjust lights, colors, and camera in the `Scene` / `App` components.
