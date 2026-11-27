ECLIPSE + VESPER / BROWSER SHOWCASE REBUILDS
==========================================

QUICK START (WINDOWS)
1. Right-click Visual-Showcases-Rebuilt.zip and choose Extract All.
2. Open START-HERE.html in current Chrome or Microsoft Edge.
3. Choose ECLIPSE (Minecraft-style voxel scene) or VESPER (material gallery).
   You can also open either showcase HTML directly.
4. Keep three.min.js beside both HTML files. No npm, server, CDN, login,
   downloaded textures, or internet connection is required.

Your supplied three.min.js.txt has been copied to the correct three.min.js
filename without changing its library code. The original uploads are untouched.
Post-processing code is embedded directly in each showcase HTML.

RECOMMENDED FOR YOUR RTX 5070 TI
- Turn on browser graphics/hardware acceleration and relaunch the browser.
- Start at your normal desktop resolution with ULTRA selected.
- Ultra renders at device pixel ratio up to 2; a high-DPI display may render
  substantially more pixels than the window's CSS dimensions suggest.
- If necessary select BALANCED before reducing your monitor resolution.
- chrome://gpu or edge://gpu should show WebGL as hardware accelerated.
- If Windows/browser selects a different adapter, choose the browser under
  Windows Settings > System > Display > Graphics settings > High performance.
- Allow initial material/shader compilation to finish before judging smoothness.
  First use of a different lighting preset can also compile shaders.

ECLIPSE / MINECRAFT-STYLE SHOWCASE
- Click the scene: capture mouse. ESC: release mouse.
- WASD or arrow keys: move. SPACE: jump. SHIFT: sprint.
- Left-click: break a block. Right-click or E: place selected block.
- F: toss a block. 1-9 / mouse wheel: select hotbar item.
- H or RENDER SETTINGS: open/close the lighting panel.
- Day, sunset and night presets; exposure, bloom, fog and sun-angle controls.
- Ultra / Balanced / Performance quality choices.
- Changes to the voxel world are session-only, not saved to disk.

Major changes:
- Replaced per-block rendering with chunk meshes, hidden-face removal,
  per-corner voxel ambient occlusion, and local chunk rebuilds when editing.
- Procedural 512x512 material tiles assembled into 2048x2048 atlases:
  albedo, normal, roughness and glow maps. These are generated textures,
  not scanned commercial texture assets.
- Rebuilt terrain, cabin, shoreline, path, tree canopies, vegetation,
  flowers, distant terrain and water composition.
- Actual mirrored scene rendering on water with Fresnel mixing and ripples.
- Prefiltered sky environment lighting, 4096 shadow map on Ultra,
  firefly particles, glass cutouts, dropped blocks and break particles.
- Embedded HDR bloom, depth-based screen-space AO, edge smoothing,
  vignette and final ACES-style tone mapping.
- Fixed hotbar canvases being erased by HTML updates and grass/log face maps.

VESPER / ARCHITECTURAL MATERIAL GALLERY
The old ue5-showcase.html has been replaced with a new Three.js scene,
not renamed Unreal technology.
- Starts in a slow guided orbit. Click scene / EXPLORE: free-flight camera.
- WASD: horizontal flight. Q/E: down/up. SHIFT: faster movement.
- ESC: release mouse. GUIDED: return to orbit.
- H: hide/show interface. SAVE PNG: save the current rendered canvas.
- Blue-hour/daylight presets; exposure, bloom and quality controls.
- Free flight is intentional: this scene does not have collision physics.

Major changes:
- Designed a full colonnaded courtyard, timber roof lattice, tiled floor,
  sunken pool, bridge, benches, planters and mountain terrain.
- Animated multi-ring bronze sculpture, fluted stone plinths, beveled alloy
  cube, porcelain sphere, mineral polyhedron and bronze knot exhibits.
- 1024x1024 procedural material color/normal maps for stone, wood and marble.
- Instanced vegetation; metallic material response and prefiltered sky IBL.
- Real planar pool reflections, shadow-casting sun, local colored lights,
  HDR bloom, depth-based SSAO, edge smoothing and filmic tone mapping.

TECHNICAL HONESTY
- Both scenes use your supplied Three.js r128 and WebGL rasterization.
- Neither uses Unreal Engine, Lumen, Nanite, RTX/DXR hardware ray tracing,
  path tracing, global-illumination simulation, or ray-traced reflections.
- Water uses one mirrored scene render, not general-purpose ray tracing.
- Environment lighting is a generated sky map, not dynamic reflection
  captures of every moving object. Metal exhibits reflect that sky map.
- Bloom and screen-space effects are approximations with known limitations.
- The renderer requests a high-performance graphics context; the OS/browser
  ultimately decides which GPU is used. No HTML file can force an NVIDIA GPU.
- Performance depends on browser, resolution, acceleration and drivers.
  No RTX 5070 Ti FPS benchmark is claimed.

VALIDATION PERFORMED
- Parsed all inline JavaScript with node --check.
- Opened both final delivery HTML files in offline Chromium with their
  delivery render settings, including the 4096 shadow-map configuration.
- Captured and visually inspected rendered screenshots.
- No page errors or WebGL console errors observed in the final smoke test.
- Additional offline controls tests exercised Minecraft day/night/reset,
  bloom/exposure, panel and hotbar; and gallery lighting/exposure/bloom/UI.
- Those interaction tests used reduced shadow/reflection resolution because
  the test browser uses software rendering. They made zero HTTP requests.
- This is browser smoke/visual testing, not exhaustive gameplay testing or
  validation on your exact Windows/NVIDIA configuration.

TROUBLESHOOTING
- Blank page: extract the ZIP first; do not launch a file inside the ZIP.
  Confirm three.min.js exists in the same folder as the HTML files.
- A file preview inside a chat application may block sibling scripts or
  pointer lock. Use the extracted files in a normal browser tab instead.
- Very low FPS: check hardware acceleration and chrome://gpu / edge://gpu.
- Mouse not turning: click the actual scene, then approve any browser prompt.
- Want less glow: lower Bloom in the scene's render controls.
- Reloading resets the camera/world and all scene parameters.
