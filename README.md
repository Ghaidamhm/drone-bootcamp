المشكلة إنك نسختي النص من المعاينة، فراحت منه رموز التنسيق مثل `#` و`-` و`|`. عشان كذا GitHub عرضه كفقرة وحدة طويلة بدون عناوين ولا قوائم ولا جدول.

**الحل:**
1. في صفحة المستودع اضغطي القلم ✏️ اللي جنب **README**.
2. احذفي كل النص الموجود: **Cmd + A** ثم **Delete**.
3. انسخي النص من المربع تحت بزر النسخ اللي في زاويته، والصقيه.
4. اضغطي **Commit changes**.

```markdown
# Drone Bootcamp — Interactive Landing Page

An immersive, Arabic-first (RTL) landing page for a drone bootcamp in Riyadh. A real-time 3D globe highlights Saudi Arabia, and a procedurally built drone lifts off from Riyadh in a cinematic opening sequence, then accompanies the visitor through every section of the page.

---

## Highlights

- **Cinematic intro sequence** — the camera opens over the Kingdom, the drone takes off from Riyadh, and the shot transitions seamlessly into the page layout.
- **Real-time 3D globe** — a dotted world map rendered in WebGL, with Saudi Arabia illuminated in the brand accent color.
- **Procedural 3D drone** — modeled entirely in code, with no external model files. Drag to rotate it 360°; click or tap to trigger a barrel roll.
- **Physically informed motion** — the drone's pitch, bank, and heading are derived analytically from its flight path, producing natural acceleration and turns with no frame-rate jitter.
- **Choreographed section transitions** — each section has its own camera framing and a deliberate drone position that never obscures the Kingdom or the content.
- **Fully responsive, RTL layout** — optimized for desktop, tablet, and mobile.
- **Adaptive performance** — rendering resolution scales automatically to the device's actual frame rate.
- **Accessibility** — respects `prefers-reduced-motion` and falls back gracefully when WebGL is unavailable.

## Tech Stack

| Technology | Role |
|---|---|
| **HTML5 / CSS3** | Semantic structure, CSS custom properties, Grid & Flexbox, responsive RTL layout |
| **JavaScript (ES Modules)** | Application logic, navigation, and interaction — no framework |
| **[Three.js](https://threejs.org) r160** | WebGL rendering of the globe, drone, lighting, and materials |
| **Three.js Addons** | `RoundedBoxGeometry`, `RoomEnvironment` (image-based lighting), `GLTFLoader` / `DRACOLoader` (optional GLB model support) |
| **GLSL** | Custom shaders for the atmospheric glow, fresnel rim lighting, and the Riyadh light column |
| **Canvas 2D API** | Procedurally generated textures: dotted map, carbon-fiber weave, battery label |
| **[GSAP](https://gsap.com) 3.12** | Timeline-driven choreography of the intro sequence |
| **IBM Plex Sans Arabic & IBM Plex Mono** | Typography |

## Experience Flow

1. **Lift-off** — Saudi Arabia lights up, the rotors spin up, and the drone climbs out of the map from Riyadh.
2. **Flight** — the camera rises with the drone, keeping the Kingdom in frame, before opening out to the full globe.
3. **Landing** — the drone settles into a hover beside the headline as the content fades in.
4. **Exploration** — scrolling moves the camera and the drone through each section: about, tracks, key figures, timeline, requirements, FAQ, and registration.

## Customization

- **Registration link** — set `CTA_URL` at the top of the main script.
- **Brand colors** — edit the CSS custom properties in `:root` (primary accent: `--accent`).
- **Content** — copy, statistics, and timeline dates are in the corresponding `<section>` elements.
- **Optional assets** — `assets/drone.glb` replaces the procedural drone with a production 3D model; `assets/earth.webp` adds a photographic globe texture; `assets/fallback.webp` provides a static image for devices without WebGL.

## Browser Support

Latest versions of Chrome, Edge, Safari, and Firefox with WebGL enabled.

---

© 2026 Drone Bootcamp
```

ولو تبين أسهل، احذفي ملف `README.md` الحالي من GitHub، وارفعي ملف `README.md` اللي أرسلته لك قبل من **Add file** ثم **Upload files**. الملف فيه التنسيق كامل.
