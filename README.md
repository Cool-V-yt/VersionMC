# VersionMC — Full Feature List

Everything you get with VersionMC, categorized. Website: <https://v.rizv.de>

---

## 🚀 Launcher

### Core
- Sleek, mostly-transparent **glass UI** with a purple diamond identity
- **Loading splash + smooth opening reveal** animation on startup
- Page transitions, staggered card animations, hover motion throughout
- **Maximize** switches to a solid fill with a glassy blurred sidebar
- Frameless custom title bar (minimize / maximize / close)

### Accounts
- **Microsoft login required** — the launcher won't start the game without a signed-in account (no offline mode)
- Session **auto-refreshes** across restarts (log in once)
- Player head avatar + name in the sidebar

### Profiles & Library (Modrinth-app style)
- Unlimited **profiles**, each with its own color, version, loader and renderer
- **Fully isolated per profile:** mods, worlds, resource packs, shaders, `options.txt`, and configs all live separately
- **Library** grid with per-profile play button, edit, delete, and an "active" badge
- Click a profile → **profile detail page**

### Per-profile settings
- **Loader:** ✦ Version Client (Fabric + the VersionMC client mod), Fabric, or Vanilla
- **Renderer:** VulkanMod, Sodium, or None — auto-installed and swapped on launch
- **Performance mods** toggle: Lithium, FerriteCore, Krypton, EntityCulling (+ ImmediatelyFast on non-Vulkan profiles)
- **RAM** override (or use the global default)
- Shows the **Java runtime** the profile will use

### Auto-management
- Correct **Java runtime auto-installed** per Minecraft version (Adoptium/Temurin)
- **Fabric loader** installed automatically for modded profiles
- VersionMC client mod + Fabric API auto-installed for Version Client profiles
- **Optimized JVM flags** (tuned G1GC) toggle for smoother frametimes

### Content installers (per profile)
- Browse & one-click install **Mods**, **Resource Packs**, and **Shaders**
- Sources: **Modrinth** (out of the box) and **CurseForge** (free API key)
- Automatic **required-dependency** resolution
- Enable / disable / delete installed content per profile
- Files land in the correct folders automatically

### Other launcher settings
- Accent color, window opacity, default RAM slider
- Show-snapshots toggle (lists snapshot versions)
- CurseForge API key field
- Java path override
- Quick-open buttons: game data / profile folder / mods folder
- Console with live game log
- v.rizv.de link

### Distribution
- **One-click EXE installer** (NSIS) that launches the app when done
- Custom diamond `.ico` on installer, app, and shortcuts
- **Auto-updater** — checks on startup, downloads in the background, "Restart & update" in Settings
- Ships all client-mod jars bundled

---

## 🎮 In-Game Client (Version Client)

Zero mixins, **works alongside VulkanMod, Sodium and ImmediatelyFast.**
Supported version families: **26.2, 1.21.11, 1.21.1, 1.20.4.**

### HUD Modules
| Module | Notes |
|---|---|
| **FPS** | Threshold colors (red under 30 / green over 60), custom label template |
| **Coordinates** | X Y Z |
| **Ping** | Latency in ms, threshold colors |
| **Memory** | Used / max, threshold colors |
| **CPS** | Left \| Right clicks, polled every frame |
| **Speed** | Blocks per second |
| **Reach** | Shows the distance of your last landed hit |
| **Keystrokes** | WASD + mouse buttons + spacebar |
| **Armor Status** | Durability %, horizontal or vertical layout |
| **Potion Effects** | Color-chip icons, hides hidden/ambient effects |
| **Direction** | Facing + axis |
| **Biome** | Current biome |
| **Clock** | Real-world time |
| **Session Time** | Time since launch |
| **World Day** | In-world day counter |
| **ToggleSprint** | Auto-hold sprint |
| **Fullbright** | Night-vision based — **works under VulkanMod** |
| **Zoom** | Hold C, smooth easing, scroll to change magnification |
| **Time Changer** | Client-side sky time (Sunrise/Day/Noon/Sunset/Night/Midnight) |
| **Chat** | Smooth chat, mention highlight + ping, custom size & colors |
| **Scoreboard** | Custom sidebar (fixed right-center) |
| **Tab List** | Custom, ping bars, VersionMC icon on client users |
| **Nametag Logo** | Diamond next to VersionMC users' names |

### HUD Editor (Right Shift)
- Opens as a lone **diamond "V"** in the middle of the screen → click to expand the hub (animated)
- **Three tabs:** Modules · Profiles · Settings
- **Module cards** with hand-drawn pixel icons, toggle switches and gear buttons
- **Big or compact** card view, plus a **search** bar
- Drag modules to move; right-click to disable; disabled modules are fully hidden

### Per-module customization
- **Enable** and **Visible** toggles (works-but-invisible mode)
- **Custom text template** (`{v}` = the value, e.g. `www : {v}`)
- **Text color** and **background color** with a full color picker
- **Color picker:** hue bar + shade bar + **transparency (alpha)** + typeable **hex** input
- **Per-module opacity** and **scale** (0.5×–2×)
- **Threshold colors** for numeric modules (custom low/high values + colors)
- **Module-specific controls** (e.g. Chat's width, focused/unfocused line counts, ping-sound toggle; Armor layout; Tab List icon side; Time Changer sky)

### HUD Profiles (layouts)
- Save / apply / delete named HUD layouts
- **Shareable** — drop `.json` files into `config/versionmc-huds` to import

### Global HUD settings
- HUD opacity, accent color, text shadow, rounded corners
- Animations toggle, nametag icon toggle, nametag background transparency
- Reset layout
- **Toast** popups for every action

### Custom Main Menu
- Replaces the vanilla title screen entirely
- Animated background: gradient + slowly **drifting diamonds**
- **Intro animation:** "VersionMC" starts centered, eases up into the title, then buttons fade/slide in one by one
- Glowing purple **MC** wordmark
- Custom buttons: Singleplayer / Multiplayer / Options / Quit

### Custom Loading Screen
- Branded animated overlay on world load, server connect, and level generation
- Gradient + drifting diamonds + breathing wordmark + sliding progress bar + animated "Loading…" dots

### Branding
- Diamond logo across the editor, main menu, and loading screen
- **VersionMC watermark** bottom-right of in-game menus (inventory, pause, crafting…)
- Diamond icon next to VersionMC players' names (nametags + tab list)
- Ships as a real custom **font glyph**

---

## 🔢 Version Support
- **26.2** (unobfuscated / newest API)
- **1.21.11** (primary target)
- **1.21.1**
- **1.20.4**

Each Version Client profile auto-installs the matching build.
