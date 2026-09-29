<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/header-dark.svg">
  <img alt="Agustin Yarrus — software developer from Argentina. Small, fast, dependency-free software. Into algebra, physics, geometry, graphics and minimal design. Go, C, C++, C#, JavaScript, TypeScript, Python, GLSL." src="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/header-light.svg" width="100%">
</picture>

I write software the way I like mathematics: **small, exact and self-contained**. Native Windows apps measured in kilobytes, a physics engine in plain JavaScript, file-format parsers with no library underneath — and every claim checked against an independent oracle instead of by eye.

**~149,000 lines** of my own code · **~48,000 lines** of tests · **14** public repos · **5** of them build from nothing but a standard library.

## Where the math lives

Algebra, physics, geometry, graphics and minimal design aren't hobbies next to my code — they're how it works. Six figures, each taken from one of my repos:

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/figures-dark.svg">
  <img alt="Six figures: an XPBD distance constraint (Carrona), analytic two-bone IK (Carrona), zoom about the cursor as a homothety (Lux, Lumen), the eight EXIF orientations as the dihedral group D4 (Prisma), a QR code made by clip2qr's own Reed–Solomon encoder over GF(2^8), and a Dijkstra flow field steering a horde (Carrona)." src="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/figures-light.svg" width="100%">
</picture>

| | Where | The idea |
|:--|:--|:--|
| **Physics** | [Carrona](https://github.com/agustinyarrus/carrona) | Ragdolls on my own XPBD solver — 7 substeps per frame, compliant constraints, PD "muscles" with <i>k</i> = 1 − <i>e</i><sup>−130<i>h</i></sup> and a damping ratio <i>ζ</i> ≈ 0.73 |
| **Geometry** | Carrona | Legs placed by analytic two-bone IK: the knee is where two circles meet |
| **Linear algebra** | [Lux](https://github.com/agustinyarrus/lux) · [Lumen](https://github.com/agustinyarrus/lumen) | Zoom is a homothety centered on the cursor; images become mipmap pyramids drawn at a scale kept in [½, 1] |
| **Abstract algebra** | [clip2qr](https://github.com/agustinyarrus/clip2qr) · [Prisma](https://github.com/agustinyarrus/prisma) | Reed–Solomon over GF(2⁸) and BCH codes for QR; the 8 EXIF orientations as the dihedral group <i>D</i><sub>4</sub> |
| **Color science** | [img](https://github.com/agustinyarrus/img) · Prisma · Lux | libwebp's fixed-point BT.601 YUV→RGB reproduced bit for bit; RGB→XYZ from chromaticities with Bradford adaptation; ACES tone mapping |
| **Graph theory** | [pdf-merge](https://github.com/agustinyarrus/pdf-merge) · [killport](https://github.com/agustinyarrus/killport) | PDF objects deduplicated as a Merkle DAG in Tarjan order; process forests rebuilt in <i>O</i>(<i>n</i>); Dijkstra flow fields for hordes |
| **Graphics** | [Chainmate](https://github.com/agustinyarrus/chainmate) · Lux | Godot's Forward+ rebuilt pass by pass in WebGL2 — cascaded shadows, SSAO, SSIL, volumetric fog, glow; GPU-tiled mipmaps in Direct2D |
| **Numerical methods** | Chainmate · [vidsquash](https://github.com/agustinyarrus/vidsquash) | float32 rounding reproduced exactly — even a GPU's inexact reciprocal, <i>a</i>/<i>b</i> = <i>a</i>·rcp(<i>b</i>) — so particles match the original to 2·10⁻⁶; hitting an exact file size with the secant method on size(bitrate) |
| **Minimal design** | all of them | Dark, frameless interfaces; font sizes rounded to whole device pixels; ClearType kept intact |

## Selected work

| Project | What it is | Built with | Proof |
|:--|:--|:--|:--|
| **[Chainmate](https://github.com/agustinyarrus/chainmate)** | A Godot 4.7.2 chess roguelite rebuilt for the web and Android, verified against the original `.exe` | `JavaScript` `three.js` `WebGL2` `WASM` | 258 oracle tests · 28,000+ glyphs bit-identical |
| **[Carrona](https://github.com/agustinyarrus/carrona)** | Top-down zombies where every body is an active ragdoll | `JavaScript` `three.js` `GLSL` | own XPBD engine · 1,207 physics checks |
| **[killport](https://github.com/agustinyarrus/killport)** | Frees a busy port on Windows — process, service, container or WSL — and proves it stays free | `Go` `Win32/NT` | 0 dependencies · 613 tests |
| **[Lux](https://github.com/agustinyarrus/lux)** | Native image viewer built on GPU-tiled mipmap pyramids | `C++17` `Direct2D` `WIC` | 24,000-px panorama at 57–60 fps |
| **[Prisma](https://github.com/agustinyarrus/prisma)** | Any image → the smallest lossless PNG/APNG, transparency done right | `C17` `WIC` | 13 own decoders · 236 end-to-end cases |
| **[Capcom](https://github.com/agustinyarrus/capcom)** | Mission control for local LLMs | `C#` `WinForms/GDI` `llama.cpp` | ~560 KB · 0 NuGet packages |
| **[Folio](https://github.com/agustinyarrus/folio)** · **[Lumen](https://github.com/agustinyarrus/lumen)** · **[Cipher](https://github.com/agustinyarrus/cipher)** | Dark, frameless Markdown reader, image viewer and code viewer | `Go` `WebView2` | 127 formats · 250+ languages |
| **[clip2qr](https://github.com/agustinyarrus/clip2qr)** · **[pdf-merge](https://github.com/agustinyarrus/pdf-merge)** · **[img](https://github.com/agustinyarrus/img)** · **[vidsquash](https://github.com/agustinyarrus/vidsquash)** | Console tools: QR encoder, PDF merger, image converter, target-size video | `Go` | own QR and PDF engines · 0 dependencies |

### [Chainmate](https://github.com/agustinyarrus/chainmate) — the same game, proven

`JavaScript` · `three.js` · `WebGL2` · `WebAssembly` · `AudioWorklet` · `Android`

I took a shipped Godot 4.7.2 game — a 110 MB `.exe`, no project files — and rebuilt it in JavaScript and three.js. The goal wasn't a look-alike remake but *the same game*: same seeds, same frames, same interface, same sound, each one measured against the original executable.

- **The original as an oracle.** The `.exe`, patched with a single hook, runs GDScript probes inside the real engine and answers in JSON: every mesh, glyph and audio sample, the order of every `_process` and `await`, intermediate render targets, particles read back from the GPU. **258 tests** (~30 s, no browser) hold the port to those answers.
- **Logic, bit for bit.** Five full games replayed action by action, with the complete PCG32 state compared after every step — identical.
- **Text, bit for bit.** FreeType 2.14.3 and HarfBuzz 14.2.0 — the versions Godot ships — compiled to WebAssembly with Zig's clang: **28,000+ glyphs identical**.
- **Pixels.** 34 of 39 screenshots of the full tour match and 4 more are within 1 % of pixels; the render-stage captures differ by just **0.006–0.016 / 255** on average in the final frame (≤ 0.12 for any single effect).

<details>
<summary><b>Under the hood</b></summary>

- **Engine semantics, reimplemented:** the SceneTree's exact frame order, GDScript `await` as JavaScript generators, `hash()`, `str(float)`, stable `sort_custom`, and 32-bit float vector math — which decides branches like `size.x > size.z * 1.55` when the arena is built.
- **Forward+, pass by pass:** cascaded shadows, SSAO, SSIL, volumetric fog, subsurface scattering, sky, glow and tone mapping, each compared on its own against the original's intermediate buffers (88 images per run). Compute passes run as fragment passes; fog volumes as filtered slice atlases.
- **GPU particles on the CPU:** the `GPUParticles3D` compute shader re-run in single precision, in the same order — including the reference GPU's divider, where `a / b` is `a × rcp(b)` with 169 reciprocals that don't round correctly (worst error 2·10⁻⁶).
- **Audio:** all 24 effects and the music synthesized sample-exact; Godot's mixer (buses, limiter) running in an AudioWorklet.
- **The detective:** a state trace diffed between both programs pins every random value to the exact generator word it came from. That's how I found that the global `randf()` consumes one PCG word while `RandomNumberGenerator.randf()` consumes two.
- **Deterministic autopilot:** the game's own screenshot tour made deterministic (fixed 1/60 s frames, seeded RNG, no desktop input) and run identically on both sides.
- **Performance parity:** 39.5 / 44 / 39.5 ms per frame at 1600×900 on Iris Xe graphics, against the original's 38.6 / 44.1 / 38.1 ms.
- **Android:** Capacitor 6, targetSdk 36, smoke-tested on an API 36 emulator.

</details>

### Carrona — ragdoll physics from scratch

`JavaScript` · `three.js (rendering only)` · `GLSL` · `Web Audio` · **no npm packages**

A top-down zombie shooter where every body on screen — the player included — is an **active ragdoll**. There isn't a single animation clip, texture file or sound file in the repo: motion comes from physics, textures from noise, sound from a synthesizer.

- **XPBD solver** on flat typed arrays: 7 substeps per frame (<i>h</i> = 1/420 s at 60 fps), one Gauss–Seidel pass per substep, compliance tuned per constraint (bones 4·10⁻⁷, torso braces 2·10⁻⁶, joint limits 2·10⁻⁵ m/N). Nothing in `src/phys` imports three.js.
- **Muscles:** each body is 16 particles, 15 bones and 48 constraints (65 kg), pulled toward an animated pose by PD control — <i>k</i> = 1 − <i>e</i><sup>−130<i>h</i></sup>, damping 1.45√(<i>km</i>), so <i>ζ</i> ≈ 0.73.
- **Walking:** the gait cycle advances with distance walked, so planted feet can't skate (measured: 0.18 m/s); cubic Hermite swing; analytic two-bone IK; recovery steps and falls when the balance error crosses its thresholds.
- **Numbers:** 40 ragdolls + 40 boxes + 12 cylinders simulated in 9 ms per frame; 56 fps on a Redmi Note 14 Pro. **1,207 automated checks** in 19 suites measure physical quantities — foot skate, bone stretch, knees bending backwards, how still a corpse lies.

<details>
<summary><b>Under the hood</b></summary>

- **Collision:** spheres against the floor, yaw-rotated boxes and cylinders; bones as capsules; positional friction (static 0.92, dynamic 0.30); a spatial hash with 0.55 m cells and 16,384 buckets; analytic ray–capsule and ray–box tests for aiming.
- **Stable by construction:** zero restitution, per-substep velocity caps, depenetration limited to the substep's own motion plus 8 mm, and a last pass that re-projects bones to their rest length.
- **Corpses:** limp bodies get rigid-body damping from the full 3×3 inertia tensor — <i>ω</i> = <i>I</i><sup>−1</sup><i>L</i>, each particle pulled toward <i>v</i><sub>cm</sub> + <i>ω</i> × <i>r</i> — which kills jitter without killing momentum.
- **Joint limits without Euler angles:** cones (knees 65°, elbows 80°) in a torso frame rebuilt from the particles by Gram–Schmidt.
- **Hits:** impulses split along the bone and capped per particle; the muscles around a hit go slack for 0.10–0.32 s; off-center shots spin the body by <i>r</i> × <i>J</i>.
- **Ballistics:** falling bodies predict their impact time <i>t</i> = (−<i>v</i> + √(<i>v</i>² + 2<i>gh</i>))/<i>g</i> and reach out with their hands; aimed projectiles solve the launch angle in a form that stays accurate when gravity is small.
- **The horde:** one Dijkstra flow field (0.4 m grid, my own binary heap) steers every zombie; separation and flanking on top; distant bodies skip detailed collision.
- **Rendering:** instanced bodies; my own GLSL (color grading, a sprite batch of camera-, beam- and surface-aligned quads, the flashlight cone); seamless procedural textures baked in Web Workers; every shader compiled behind the menu, so nothing hitches mid-game.
- **Content:** 104 procedurally modeled weapons (hitscan, beams, rails, chain lightning, projectiles, streams, sonic waves), 5 maps, an 8-mission campaign plus endless mode, 25 ways to get up, 23 ways to fall, 21 flinches.
- **Tooling without dependencies:** no bundler; my own ZIP writer, PNG/ICO encoder, Chrome DevTools Protocol client and Google Play upload client (with its own RS256 JWT). Ships as a PWA, a Windows installer and an Android APK.

</details>

### killport — free a port, carefully

`Go` · `Win32 / NT API` · **zero dependencies** · one ~5 MB `.exe`

Finds what really holds a port — a process, a service, a Docker or Podman container, a Linux process inside WSL, an `http.sys` URL, a `portproxy` rule or a Windows reservation — closes it the way a person would (Ctrl+C first, force last) and proves the port stays free.

- **No dependencies at all:** `go.mod` has no `require` lines. 79 Win32/NT functions across 7 DLLs are bound by hand with `syscall.SyscallN` — no `x/sys`, no cgo — and every DLL loads from an absolute System32 path.
- **A process is `{PID, creation time}`,** never a bare PID, and its handle is held until it dies, so a recycled PID can never be killed by mistake.
- **Gentle escalation:** Ctrl+C injected into the target's own console (`AttachConsole` + `GenerateConsoleCtrlEvent`, only if every process sharing that console is fair game) → `WM_CLOSE` → `ControlService(STOP)` for services → `TerminateProcess`, waiting on handles instead of polling.
- **Proof, not hope:** the port has to stay free for 350 ms — a window taken from measurements (a supervisor re-bound a port in 241 ms; `wslrelay` lets go ~315 ms after a container stops). If something respawns the server, killport names the supervisor.
- **613 test functions:** 24.6k lines of tests for 28k lines of code.

<details>
<summary><b>Under the hood</b></summary>

- **Socket tables:** `GetExtendedTcpTable` / `GetExtendedUdpTable` for IPv4 and IPv6, rows parsed by hand; `GetOwnerModuleFrom*Entry` names the service hiding inside a `svchost`.
- **One-call snapshot:** `NtQuerySystemInformation`; image paths without opening a single process; another process's working folder read from its PEB (WOW64-aware) and turned into a project name (`package.json`, `go.mod`, `Cargo.toml`, `pyproject.toml`, `.csproj`) and a git branch (`.git/HEAD`, no git needed).
- **Process forest in <i>O</i>(<i>n</i>):** a parent link counts only if the parent was born first; a lowest-common-ancestor search across before/after snapshots finds the supervisor (nodemon, pm2…) that brought a server back.
- **Docker and Podman:** my own HTTP/1.1 client (content-length, chunked, read-until-close) over overlapped named pipes opened with `SECURITY_IDENTIFICATION`, so a fake pipe server can't impersonate an elevated killport. The engine is found through `DOCKER_HOST`, the active Docker context or the default pipes.
- **WSL:** an embedded POSIX `sh` script reads `ss` or `/proc/net`, confirms the owner by socket inode, and signals SIGINT → SIGTERM → SIGKILL, re-checking the start time before each signal. It never starts a distro.
- **Localised Windows:** the `netsh` parsers anchor on structure — dashed underlines, indentation, SDDL — never on words.
- **Hardened elevation:** UAC through `ShellExecuteExW("runas")`; the elevated copy receives a closed-grammar selection instead of commands, re-plans from its own snapshot, and writes its result with `CREATE_NEW` and reparse-point checks.
- **Impostor detection:** a "system" process name only counts if the image really is `System32\<name>` with the expected parent lineage (MITRE T1036.005).
- **Tests:** seeded property tests against reference implementations (30,000 command lines vs `CommandLineToArgvW`, 500 random process forests…), a discrete-event simulator with a virtual clock, byte-exact fixtures of real Windows output, and end-to-end runs of the real `.exe` against a fake `http.sys` registrant, a fake Docker engine, a fake `wsl.exe` and a real test service.
- **Math in a CLI:** interval-set algebra for port ranges, water-filling column widths by binary search, Damerau–Levenshtein "did you mean", progress bars with 1/8-cell resolution.

</details>

### Lux — a native image viewer

`C++17` · `Win32` · `Direct2D` · `DirectWrite` · `WIC` · `SSE2` · one ~860 KB portable `.exe`

- **Mipmap pyramids on the GPU.** Every image is halved with a 2×2 box filter in premultiplied alpha (exact rounding, SSE2) and cut into 2048-px tiles with 8-px borrowed margins. The level drawn keeps the on-screen scale in [½, 1], which gets past Direct2D's 16,384-px bitmap limit: a **24,000-px panorama pans at 57–60 fps** and a 48 MP photo renders at 60 fps after opening in 335–352 ms.
- **Instant next image:** two decoder threads with their own WIC factories and prefetch in the direction you're browsing — **0.3 ms** when prefetched; JPEGs first decoded at 1/2–1/8 scale through DCT scaling.
- **171 file extensions:** everything WIC decodes, camera RAW, SVG, EMF/WMF, EXR/HDR, DDS/KTX/VTF (with my own BC1–5 decoders), GIMP XCF, FITS/DICOM and retro formats (Amiga, Atari, C64, ZX Spectrum, PlayStation).

<details>
<summary><b>Under the hood</b></summary>

- **Frame budget:** 6 ms of tile uploads per frame, from the center out; missing tiles borrow from coarser levels; a 768 MB GPU cap with LRU eviction; the image cache sized to 1/16 of RAM.
- **Exact premultiplication:** (<i>t</i> + (<i>t</i> ≫ 8)) ≫ 8 with <i>t</i> = <i>c</i>·<i>a</i> + 128, verified on all 65,536 pairs.
- **No seams:** a test sweeps 400 random scales and offsets and checks that every screen column is drawn by exactly one tile.
- **Zoom:** a homothety about the cursor, ×1.18 per wheel notch, with the origin snapped to whole pixels so 100 % is pixel-exact; high-quality cubic filtering, nearest-neighbor from 300 %.
- **HDR files:** exposure from a log-luminance histogram → ACES filmic curve → sRGB through a lookup table.
- **Frameless but native:** custom `WM_NCCALCSIZE` / `WM_NCHITTEST`, `DwmExtendFrameIntoClientArea` to keep the system shadow, DWM dark mode and rounded corners; an opaque render target so ClearType stays sharp.
- **Dependencies:** single-header libraries only (stb_image, nanosvg, qoi, tinyexr); MSVC with `/O2 /GL` and `/LTCG /OPT:REF,ICF`.

</details>

### Prisma · image2png — transparency, done right

`C17` · `clang-cl + LLD, full LTO` · `WIC` · one dependency (libdeflate) · one ~800 KB `.exe`

Turns any image into the smallest lossless PNG or APNG, and understands transparency however the source stores it — alpha channel, color key, palette alpha, 1-bit mask, premultiplied color, color matted on white, AVIF/HEIC auxiliary alpha.

- **13 decoders of my own** (PNG/APNG, GIF, BMP, ICO, TGA, PSD, DDS with BC1–BC7 and BC6H, QOI, PNM, farbfeld, SGI, PCX, Radiance HDR); everything else through WIC, chosen by content, never by extension.
- **AVIF/HEIC alpha recovery:** Windows' codec drops the alpha item, so Prisma walks the ISOBMFF boxes itself, rewrites `pitm` in a copy so the same codec decodes the alpha plane, aligns it with the image's rotation and mirroring, and unpremultiplies it.
- **Faster and smaller than Pillow:** a 4K JPEG → PNG in 843 ms / 2,231 KB (Pillow: 1,242 ms / 2,367 KB); a 72-frame GIF → APNG in 113 KB (Pillow: 235 KB); a folder of screenshots 2.5× faster.

<details>
<summary><b>Under the hood</b></summary>

- **Color:** ITU-T H.273 code points; RGB→XYZ derived from chromaticities with Bradford adaptation; PNG's new `cICP` chunk; and a fix for Windows' AV1 decoder, which guesses the YCbCr matrix from the primaries: <i>C</i> = <i>M</i><sub>declared</sub><sup>−1</sup> <i>M</i><sub>709</sub>.
- **Encoder:** the smallest lossless color type; nine row-filter strategies, three of them raced on a 16×8-row sample; DEFLATE in parallel 1 MB chunks (pigz-style) with the checksums combined mathematically.
- **Palette math:** colors are compared composited over black *and* over white — a positive-definite quadratic form, so k-means minimizes it exactly: median cut → Lloyd iterations → Floyd–Steinberg or Bayer 8×8.
- **Background removal:** alpha is the least-squares projection of each pixel onto the subject–background line, with the subject color spread outward by BFS.
- **Symmetry:** the 8 EXIF orientations as <i>D</i><sub>4</sub> — 2×2 integer matrices whose inverse is their transpose (fig. 4).
- **Robustness:** a thread pool with nested parallel loops, per-file SEH isolation, memory-mapped inputs from 64 MB, AVX2 filters, and a salvage inflater that recovers the readable rows of truncated PNGs.
- **Tests:** 236 end-to-end cases against exact references, Pillow/OpenCV and my own reference PNG writer — also under AddressSanitizer — plus unit tests and mutation fuzzing.

</details>

### Capcom — mission control for local LLMs

`C#` · `.NET Framework 4.8` · `WinForms, owner-drawn GDI` · `llama.cpp` · **0 NuGet packages** · one ~560 KB `.exe`

A desktop console for local GGUF models, styled like Apollo mission control: it starts `llama-server`, streams tokens over SSE and draws every pixel itself.

- **Streaming done right:** a background thread appends tokens while the UI repaints on a 60 ms timer instead of once per token; text layout is cached by width and version; generation can be cancelled at any moment.
- **Telemetry:** tokens/s, time to first token, context and memory use, a GO/NO-GO board; a 20-question benchmark in 9 categories, with code answers executed in Node under `--permission` and a 10 s limit.
- **Hand-made everything:** Markdown renderer, syntax highlighter, JSON writer, SSE client; Hugging Face downloads with HTTP `Range` resume and SHA-256 checks; the access token encrypted with DPAPI; Apollo "Quindar" tones (2525 / 2475 Hz) synthesized in memory.
- **Design:** near-black `#07080b`, muted pastels, Cascadia weights chosen by final pixel size, letter-spacing drawn by hand (GDI has none), a graph-paper grid and segmented instrument bars.

### Folio · Lumen · Cipher — a family of quiet Windows apps

`Go` · `WebView2` · `Win32 / DWM / COM` · 100 % offline

Three dark, frameless viewers on one architecture: a Go backend on a random loopback port, a WebView2 front end, a window that is frameless from creation (CBT hook + subclassing) yet keeps Aero Snap, no white flash on startup, and single-instance hand-off.

- **[Folio](https://github.com/agustinyarrus/folio)** — a Markdown reader for **127 file extensions** (JSON/JSON5, CSV with delimiter detection, reST, AsciiDoc, Org, MediaWiki, docx, odt, epub and HTML, all converted to Markdown). My own goldmark extensions: TeX math, GitHub alerts, `==mark==` `^sup^` `~sub~`, Obsidian wikilinks resolved by BFS over the vault, `:::` containers, and abbreviations matched by a hand-written **Aho–Corasick** automaton. KaTeX and mermaid load lazily behind LRU caches; live reload keeps you on the paragraph you were reading.
- **[Lumen](https://github.com/agustinyarrus/lumen)** — an image viewer whose window is sized to the photo before it appears (it reads only the header); zoom about the cursor, <i>t′</i> = <i>c</i> + (<i>t</i> − <i>c</i>)·<i>s′</i>/<i>s</i>, with exponential wheel steps <i>s</i>·<i>e</i><sup>−0.0015Δ<i>y</i></sup>; natural sort, neighbor preloading, crossfades.
- **[Cipher](https://github.com/agustinyarrus/cipher)** — a code viewer: 250+ languages through chroma's lexers and my own streaming formatter (byte-identical to chroma's HTML), the first 256 KB highlighted up front and the rest in 256-line chunks by a background job that carries the lexer state across chunks. From 1.0 to 1.1, a 12 MB log went from **69 s to 0.1 s** and language detection from **66 s to 3 ms**. Java `.class` files open as source through CFR.
- **Typography:** every font size lands on a whole number of device pixels, with the weight stepped up at small sizes; Folio keeps an opaque scroll layer so Chromium rasterizes with ClearType instead of gray anti-aliasing (measured: 0 % of glyph pixels with subpixel color before, 37–89 % after).

### Console tools for Windows

`Go` · one `.exe` each · a shared hand-written terminal UI: 24-bit pastel palette, 1/8-cell progress bars, CJK-aware widths, `NO_COLOR`, no escape codes when piped.

- **[clip2qr](https://github.com/agustinyarrus/clip2qr)** — clipboard → QR code in the terminal, from **my own ISO/IEC 18004 encoder**: arithmetic in GF(2⁸) modulo `0x11d` with doubled exp/log tables, Reed–Solomon generators ∏<sub><i>i</i></sub> (<i>x</i> − <i>α</i><sup><i>i</i></sup>), versions 1–40, numeric/alphanumeric/byte modes, levels L–H, BCH(15,5) format and BCH(18,6) version codes, all 8 masks scored by the 4 penalty rules; `▀▄█` half-blocks draw two modules per character cell. zxing-cpp decodes **72 of 72** oracle codes, versions 1 to 40. Zero dependencies — the QR in fig. 5 is its output.
- **[pdf-merge](https://github.com/agustinyarrus/pdf-merge)** — **my own tolerant PDF reader and writer:** xref tables and streams, object streams, incremental updates, broken-xref recovery by scanning, Flate with PNG/TIFF predictors, decryption R2–R6 (RC4, AES-128/256, ISO 32000-2 Algorithm 2.B); page selection (`file.pdf@1-3,5`), outlines, named destinations and AcroForm fields merged without collisions; **Merkle-DAG deduplication** — SHA-256 over a canonical form in which children are replaced by their hashes, in iterative-Tarjan order so cycles stay safe. Checked by a triple oracle: qpdf, pypdf and a PDFium pixel diff. Zero dependencies.
- **[img](https://github.com/agustinyarrus/img)** — a batch image converter whose WebP colors match **libwebp bit for bit**: a port of its 14-bit fixed-point BT.601 YUV→RGB and 9-3-3-1 chroma upsampling (U and V packed in one `uint32`, so a single add interpolates both), where Go's stock conversion is off by up to 20 levels. Animated GIFs composited per disposal method; a `NumCPU` worker pool. Only `golang.org/x/image`.
- **[vidsquash](https://github.com/agustinyarrus/vidsquash)** <sub>in progress</sub> — fits a video under a hard size limit (Discord, WhatsApp, Gmail…): a bitrate budget <i>R</i> = 8(<i>B</i> − <i>O</i>)/<i>d</i> with an MP4 overhead model, a bits-per-pixel ladder that picks resolution and frame rate, two-pass encoding corrected with the secant method, HDR → SDR tone mapping and a VMAF/SSIM check. ffmpeg underneath, no Go dependencies.

## Zero dependencies, by the numbers

| Project | Lines of my code | Third-party code | Written by hand instead |
|:--|--:|:--|:--|
| killport | 28.3k Go | **none** — standard library only | 79 Win32/NT bindings, HTTP/1.1 client, named-pipe `net.Conn`, flag parser, terminal UI |
| pdf-merge | 6.9k Go | **none** | PDF lexer, parser and writer, decryption, Merkle deduplication |
| clip2qr | 3.8k Go | **none** | QR encoder, GF(2⁸) arithmetic, Reed–Solomon, BCH |
| vidsquash | 3.9k Go | **none** (ffmpeg at run time) | rate-control planner, ffprobe parsing, quality check |
| Capcom | 12.6k C# | **none** — .NET Framework in-box | Markdown renderer, highlighter, JSON writer, SSE client, GDI interface |
| Carrona | 21.5k JS | three.js, for rendering | XPBD engine, IK, flow fields, synthesizer, ZIP/PNG/ICO writers, CDP client |
| Prisma | 14.7k C | libdeflate | 13 decoders, PNG/APNG encoder, ISOBMFF parser, color management, quantizer |
| Lux | 6.1k C++ | stb_image, nanosvg, qoi, tinyexr | tiled mipmap renderer, BCn/XCF/retro/scientific decoders, SIMD |
| img | 3.8k Go | `golang.org/x/image` | libwebp-exact color, GIF compositor, globbing |

<sub>Non-blank lines; tests and vendored code excluded. The four Go console tools share a ~2.6k-line terminal layer.</sub>

## How I verify

I don't eyeball; I measure against something that already knows the answer.

| Project | Oracle |
|:--|:--|
| [Chainmate](https://github.com/agustinyarrus/chainmate) | the original `.exe`, answering 20+ probes from inside the real engine — 258 tests |
| clip2qr | zxing-cpp, decoding every version from 1 to 40 |
| img | libwebp, bit for bit — 18 of 18 stress cases |
| pdf-merge | qpdf's strict check, pypdf's text order and a PDFium pixel diff |
| killport | recorded real Windows output, `CommandLineToArgvW`, a virtual-clock simulator — 613 tests |
| Carrona | physical measurements: foot skate, bone stretch, joint limits — 1,207 checks |
| Prisma | Pillow, OpenCV and a reference PNG writer, AddressSanitizer, mutation fuzzing — 236 cases |
| Lux | exhaustive where it can be: all 65,536 premultiply pairs, 400 random tile layouts |

## Stack

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/stack-dark.svg">
  <img alt="My stack as a periodic table of 64 elements. Languages: Go, C, C++, C#, JavaScript, TypeScript, Python, Java. More languages: PowerShell, GLSL, WebAssembly, SQL, POSIX sh, GDScript, HTML, CSS. Graphics: Direct2D, DirectWrite, WIC, WebGL2, three.js, FreeType, HarfBuzz, SIMD. Windows: Win32, NT native API, COM, DWM, WebView2, GDI/GDI+, Service Control Manager, named pipes. Systems: Docker Engine API, WSL, TCP/UDP tables, http.sys, HTTP/1.1, Server-Sent Events, Job Objects, UAC. Web and mobile: Node.js, Vite, Web Audio, AudioWorklet, Web Workers, PWA, Chrome DevTools Protocol, Android. Formats: PNG/APNG, WebP, AVIF/HEIF, PDF, QR, GIF, DEFLATE, EXR/HDR. Tools and AI: Git, GitHub Actions, MSVC, clang/LLD, Zig cc, AddressSanitizer, ffmpeg, llama.cpp. Twenty of the symbols are also real chemical elements." src="https://raw.githubusercontent.com/agustinyarrus/agustinyarrus/main/stack-light.svg" width="100%">
</picture>

## How I build

- **Small is a feature.** Startup time and binary size are measured, not guessed.
- **Dependencies earn their place.** If I can write it correctly — a QR encoder, a PDF parser, an HTTP/1.1 client — I do.
- **Exact beats close.** Bit-exact colors, pixel-exact zoom, sample-exact audio, glyph-exact text.
- **Measure, then decide.** Timeouts, thresholds and cache sizes come from measurements, not from habit.
- **Quiet interfaces.** Dark, frameless, no clutter — the content is the UI.

## Currently

- Working on backend services and CI/CD pipelines.
- Finishing **vidsquash** and growing the family of native Windows tools.

---

<sub>[LinkedIn](https://www.linkedin.com/in/ayarrus/) · This README has no dependencies either: no badge services, no trackers — every image is a hand-made SVG in this repo, the QR code comes from clip2qr's encoder, and the cloth in the header is simulated with XPBD at 7 substeps per frame, like Carrona.</sub>
