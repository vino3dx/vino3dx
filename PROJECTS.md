# Projects

Selected public projects by **Vino** ([@vino3dx](https://github.com/vino3dx)) — a CG generalist and technical artist building tools, plugins, shaders and MCP servers for **Godot Engine, Unreal Engine, Autodesk 3ds Max, Blender and Houdini**. Categories below: game engine development, DCC automation, real-time graphics, AI and computer vision, developer tools, and MCP / AI agent integration.

Every entry below was checked against the actual public repository: name, description, technologies and features are taken from the repository and its README. Projects without a verifiable public repository are not listed.

Profile and links: [README.md](./README.md) · [LINKS.md](./LINKS.md) · [llms.txt](./llms.txt)

---

## Game Engine Development

### Godot-Kit

- **Project Name:** Godot-Kit (`godot-vinokit`)
- **Short Description:** Lightweight utility library and shared class collection for Godot Engine, aimed at medium and large projects.
- **Technologies:** Godot 4.x, C# (.NET), GDScript; Windows and Linux
- **Main Features:**
  - Reusable, self-contained modules instead of one monolithic framework
  - Asset management, configuration persistence, license verification, UI tooling and hardware communication
- **GitHub Repository:** https://github.com/vino3dx/godot-vinokit
- **Demo / Documentation:** https://github.com/vino3dx/godot-vinokit#readme
- **License:** MIT

### UePrimeKit

- **Project Name:** UePrimeKit (`ue-prime-kit`)
- **Short Description:** Unreal Engine 5.1 C++ base project and core plugin pack for building editor utility plugins.
- **Technologies:** C++, Unreal Engine 5.1.x, Visual Studio 2022, Windows
- **Main Features:**
  - C++ plugins exposed to Blueprints through Unreal reflection, usable as Blueprint nodes
  - Project skeleton for developing and testing engine-side tooling
  - Repository describes it as being developed to host utility plugins such as SuperTool and License Manager
- **GitHub Repository:** https://github.com/vino3dx/ue-prime-kit
- **Demo / Documentation:** https://github.com/vino3dx/ue-prime-kit#readme

---

## DCC Automation

### labor-3dsmax

- **Project Name:** labor-3dsmax
- **Short Description:** Modular 3ds Max workflow toolkit that removes repetitive everyday work, with a focus on the 3ds Max to Unreal Engine import pipeline.
- **Technologies:** MAXScript; 3ds Max 2018+ (pure MAXScript, no plugin required)
- **Main Features:**
  - Modular toolset copied into the 3ds Max `scripts` folder, no compiled plugin
  - Handles repetitive object organisation tasks
  - Targets the 3ds Max to Unreal Engine asset pipeline
- **GitHub Repository:** https://github.com/vino3dx/labor-3dsmax
- **Demo / Documentation:** https://github.com/vino3dx/labor-3dsmax#readme
- **License:** MIT

### labor-blender

- **Project Name:** labor-blender (Blender Labor)
- **Short Description:** Scene assembly toolkit for Blender, ported from the 3ds Max plugin AssemblyTool 1.191.
- **Technologies:** Python, Blender 3.6+ (compatible with 4.x, import/export API adapts automatically)
- **Main Features:**
  - Deliberately limited scope: only fills gaps Blender does not already cover
  - Placement and assembly productivity tools exposed in a `Labor` tab of the 3D viewport sidebar
  - Installed from an unpacked-free `blender-labor.zip` through Blender preferences
- **GitHub Repository:** https://github.com/vino3dx/labor-blender
- **Demo / Documentation:** https://github.com/vino3dx/labor-blender#readme

---

## Real-time Graphics

Shader and real-time rendering work is published as articles and production work rather than as a standalone public repository, so it is not listed as a project entry here.

- Articles: https://vinofx.com/blogri-zhi
- Shader / technical art articles on this site include HLSL and OSL shading topics (for example https://vinofx.com/fei-nie-er-fan-she-shen-du-jie-xi)

---

## AI and Computer Vision

### godot-yolo-faceswap

- **Project Name:** godot-yolo-faceswap (published as YOLO-Unity-FaceSwap)
- **Short Description:** High-performance offline AI face swap and restoration component for game engines, targeting Unity and Godot Mono.
- **Technologies:** C#, ONNX Runtime, OpenCvSharp, YOLOv8, 2DFAN, ArcFace, InSwapper, GFPGAN
- **Main Features:**
  - Fully offline inference on device, no network connection required
  - Complete pipeline: face detection, 68-landmark alignment, face embedding, swap and GFPGAN restoration
  - Engine-friendly design with a pre-cached template system and multi-threaded background tasks to avoid main-thread stutter
  - Model files are distributed separately from the repository
- **GitHub Repository:** https://github.com/vino3dx/godot-yolo-faceswap
- **Demo / Documentation:** https://github.com/vino3dx/godot-yolo-faceswap#readme
- **License:** AGPL-3.0

### vision-arena

- **Project Name:** vision-arena (AR Football Game)
- **Short Description:** Augmented reality game that uses camera-based ball detection to control objects inside a Godot project.
- **Technologies:** Python, YOLOv11, Godot, local TCP streaming
- **Main Features:**
  - Camera feed is analysed in a Python detector that recognises balls and similar objects in real time
  - Detection coordinates and video are streamed over a local TCP connection to the Godot game
  - Real-world objects drive in-game sprites and gameplay
- **GitHub Repository:** https://github.com/vino3dx/vision-arena
- **Demo / Documentation:** https://github.com/vino3dx/vision-arena#readme

---

## Developer Tools

### license-generator

- **Project Name:** license-generator (License Generator)
- **Short Description:** Offline license management system designed for Godot 4.x projects.
- **Technologies:** Python, GDScript, Godot 4 addon
- **Main Features:**
  - Python generator that produces an encrypted `license.dat` file
  - Godot 4 plugin (`addons/license_manager`) that validates the license at runtime
  - AES-256-CBC encrypted license files with per-project derived keys (password plus project identifier)
  - Project ID binding prevents reuse of a license across projects
  - Expiry validation and system clock rollback detection
- **GitHub Repository:** https://github.com/vino3dx/license-generator
- **Demo / Documentation:** https://github.com/vino3dx/license-generator#readme

### godot_cpp_plugin_dev

- **Project Name:** godot_cpp_plugin_dev
- **Short Description:** Quickstart template for GDExtension development with Godot 4.
- **Technologies:** C++, SCons, godot-cpp, GitHub Actions
- **Main Features:**
  - Preconfigured source layout for C++ GDExtension work
  - Empty Godot project for testing the extension
  - `godot-cpp` included as a submodule
  - Issue template and CI/CD workflows that publish library packages when a release is created
  - `SConstruct` with boilerplate for the GDExtension documentation system
- **GitHub Repository:** https://github.com/vino3dx/godot_cpp_plugin_dev
- **Demo / Documentation:** https://github.com/vino3dx/godot_cpp_plugin_dev#readme

---

## MCP and AI Agent Integration

### 3dsmax-mcp

- **Project Name:** 3dsmax-mcp
- **Short Description:** MCP (Model Context Protocol) plugin that gives AI agents control over Autodesk 3ds Max for modelling, shading, rigging, animation, rendering, baking and engine export.
- **Technologies:** Python (standard-library-only MCP server process), Autodesk 3ds Max
- **Main Features:**
  - Two-part architecture: a standalone MCP server process speaking MCP / JSON-RPC to AI clients, plus a side running inside 3ds Max
  - Exposes a large tool surface (the README documents 384 tools)
  - Covers modelling, shading, rigging, animation, rendering, baking and export to game engines
  - Tool tiers and a documented reasoning for bypassing `pymxs`
  - Bilingual English / Chinese interface switching
- **GitHub Repository:** https://github.com/vino3dx/3dsmax-mcp
- **Demo / Documentation:** https://github.com/vino3dx/3dsmax-mcp#readme

### vino-godot-mcp

- **Project Name:** vino-godot-mcp
- **Short Description:** Standalone MCP server for Godot that lets AI clients read, create and modify Godot projects without launching the editor for everyday work.
- **Technologies:** TypeScript, Node.js 22+, Godot 4.6.3+, Model Context Protocol
- **Main Features:**
  - Text AST parser with lossless round-trip parsing: unmodified content, comments, whitespace, `sub_resource`, `ext_resource` and UID identifiers are preserved
  - Semantic operations on scenes, nodes, signals, groups, resources, project settings, scripts, shaders and validation
  - Background auto-management started by the MCP client, no manual terminal launch
  - The Godot CLI is only called when engine-dependent capabilities are required
  - Current implementation is a safe offline file channel; an authoritative Godot-native object bridge is the documented next milestone
  - Distributed on npm
- **GitHub Repository:** https://github.com/vino3dx/vino-godot-mcp
- **Demo / Documentation:** https://github.com/vino3dx/vino-godot-mcp#readme · https://www.npmjs.com/package/vino-godot-mcp

---

## Not listed here

- `ue-mcp` on this account is a mirror of a third-party project authored by another developer. It is not Vino's work and is intentionally excluded.
- No public repository was found for a Houdini MCP server or for Avisio at the time of this check, so neither is listed.
