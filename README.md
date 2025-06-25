![Venue Preview](images/scene-thumbnail.png)

Absolutely, MrJ. Here's your upgraded and polished markdown version of the **Decentraland Venue Starter Kit**, fully styled to complement your component library while keeping that creative, empowering voice at the forefront:

---

# 🎉 Decentraland Venue Starter Kit  
_The fastest way to launch your virtual club, gallery, or event space — powered by @m1d/dcl-components._

---

## 🧩 Features at a Glance

- **🎛 VideoGuide Component**  
  The scene’s “brain.” Connects to the shared M1D content network and syncs live playback across all visitors. Includes a sleek channel selector UI.

- **📺 Local Content Support**  
  Showcase your own content by adding a playlist to `index.ts`. A “Venue Content” button appears automatically in the UI for a seamless blend of global and local programming.

- **🌀 Custom Mesh Screen**  
  A high-performance, procedurally curved mesh screen for vibrant playback and excellent framerate — even under heavy scene load.

- **🪩 Animated Dance Floor**  
  Energize your venue with a custom shader-driven floor that cycles through pastel color palettes.

- **📐 Single Parcel Layout**  
  Neatly fits a 16×16m plot with optimized geometry and a polished, production-ready feel.

---

## ⚙️ Quick Start

Set up your venue in minutes:

```bash
# 1. Install dependencies
npm install

# 2. Launch locally
dcl start
```

🚀 You’ll be greeted with a working video screen, UI, and a glowing dance floor.

---

## 🧠 Core Logic (`src/index.ts`)

With the power of `@m1d/dcl-components`, you can launch a fully networked video experience in just two steps:

```ts
import { Vector3 } from '@dcl/sdk/math'
import { createCustomCurvedScreen, createVideoGuide } from '@m1d/dcl-components'

export async function main() {
  const videoGuide = await createVideoGuide({
    localPlaylist: [
      {
        src: '', // <-- Replace with your .m3u8 stream URL
        name: 'My Custom Video'
      }
    ]
  })

  createCustomCurvedScreen({
    position: Vector3.create(3.9, 0, 0),
    videoTexture: videoGuide.videoTexture
    // ...other screen properties
  })

  // Load ground, floor, and other assets here...
}
```

---

## ✏️ Customization

Make the space your own:

- 🎬 **Add Your Video**  
  Edit `src/index.ts` and paste your HLS URL (`.m3u8`) into the `localPlaylist`.

- 🧱 **Swap 3D Models**  
  Replace `models/ground1Parcel.glb` or `DF_WithSpinning_Shuffle_Float2.glb` with custom `.glb` assets.

- 🛠 **Reposition Objects**  
  Adjust `position`, `rotation`, and `scale` of elements directly in `index.ts`.

- 🧠 **Add Interactivity**  
  Extend `main()` with your logic, triggers, custom UI, or gameplay mechanics.

Your foundation is set. Now it’s time to create your world.

---

## 🤝 Support & Community

Made with ❤️ by M1D to elevate Decentraland creators.

Join us for support, sneak peeks, and creative inspiration:  
👉 **[M1D Discord](https://discord.gg/FnVxT8cVd2)**

---

**Build boldly. Dance freely. Create something unforgettable.**

---

Want a README version with GitHub badges, or a landing page version with animations? I can help you build that next.
