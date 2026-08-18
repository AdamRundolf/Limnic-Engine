<p align="center">
  <img src="https://github.com/AdamRundolf/Limnic-Engine/blob/main/.github/LOGO.png" alt="The logo, what else do you expected?"/>
</p>

**Limnic Engine** is a C++ game engine and development framework built from the **D3ModdingKit / dhewm3 / id Tech 4** codebase.

The project focuses on turning a proven classic game-engine foundation into a modern, flexible engine suitable for building new games while retaining the strengths of id Tech 4's renderer, tools, animation, physics, audio, and world systems.

> **Build on what already works. Replace what doesn't.**

## Project Goals

Limnic Engine is primarily an **engine programming and tooling project**.

Rather than immediately replacing the underlying engine, development focuses on improving the existing technology and progressively removing the limitations that make it difficult to develop modern games with it.

### Current priorities

* Modernize and improve the Radiant level editor
* Fix editor performance and stability problems
* Improve the asset and development workflow
* Establish a cleaner gameplay framework
* Modernize graphics capabilities where necessary
* Improve navigation and AI tooling
* Expand support for larger and more complex game worlds
* Keep the engine approachable enough to understand and modify

## Foundations

Limnic Engine is based on technology originating from:

* **id Tech 4**
* **Doom 3**
* **dhewm3**
* **D3ModdingKit**

The goal is not to reproduce Doom 3's original gameplay architecture. Instead, Limnic uses the existing engine technology as a foundation for a new engine.

## Why Limnic?

Classic id Tech 4 provides an unusually useful starting point for engine development.

It already contains mature implementations of many difficult low-level systems:

* Real-time 3D rendering
* Materials and shaders
* Dynamic lighting
* Shadows
* Animation
* Skeletal deformation
* Physics
* Spatial audio
* Collision
* World/map processing
* Resource management
* Level editing
* Entity infrastructure

Instead of throwing these systems away and starting from nothing, Limnic aims to **modernize and reorganize them where appropriate**.

## Tooling First

A major principle of Limnic Engine is:

> **If a problem can be solved by improving the tools, improve the tools before rewriting the engine.**

The level editor is therefore a major development target.

Radiant is being improved before adding extensive game-specific functionality. Editor performance, responsiveness, stability, and workflow are treated as fundamental engine-development concerns.

### Example

An early Radiant performance investigation identified unnecessary synchronous window updates in the camera viewport.

Replacing:

```cpp
RDW_INVALIDATE | RDW_UPDATENOW
```

with:

```cpp
RDW_INVALIDATE
```

allowed Windows to process the repaint normally rather than forcing an immediate update.

This improved both **camera flying and mouse-look responsiveness** without requiring changes to the renderer itself.

This represents the general development philosophy of Limnic:

**Find the actual bottleneck first. Fix the smallest system responsible.**

## Engine Architecture

Limnic is intended to retain useful low-level portions of the original id Tech 4 architecture while progressively replacing game-specific systems.

### Retained / modernized systems

Depending on development requirements, the project may retain or extend:

* Renderer
* Materials
* Lighting
* Physics
* Sound
* Animation
* Resource management
* Map/world representation
* Core math and utility systems
* Existing editor technology

### Systems being reconsidered

The original Doom 3 gameplay architecture is not treated as a permanent requirement.

Areas being reconsidered include:

* Gameplay framework
* Actors
* Entities
* Camera systems
* Triggers
* Scripting
* AI
* Navigation
* Game-specific systems
* Editor/game integration

## Graphics

Limnic's renderer currently originates from id Tech 4.

Long-term graphics work may include:

* Modern OpenGL support
* Improved shader capabilities
* Improved shadowing
* Cascaded shadow maps
* Soft shadows
* Image-based lighting
* Improved reflections
* Better large-world rendering
* Modern GPU resource management

Graphics work will be driven by actual engine requirements rather than attempting to reproduce every feature of modern commercial engines.

## Editor

The Radiant editor is a major component of Limnic.

Development priorities include:

* Better viewport performance
* Better camera controls
* Improved stability
* Improved selection and manipulation
* Improved entity editing
* Improved model placement
* Better asset workflows
* Better debugging and visualization
* Support for larger scenes
* More efficient world-building workflows

The intention is to evolve the existing editor rather than immediately discard it and build a new editor from scratch.

## Navigation

Navigation is planned to move toward a modern navigation system such as **Recast Navigation / Detour**.

This will eventually provide better support for:

* Character navigation
* NPC movement
* Dynamic game worlds
* Navigation debugging
* Editor visualization of navigation data

## Physics

The original physics implementation provides a functional foundation.

Alternative physics technologies may be evaluated where they provide meaningful advantages, including:

* PhysX
* Jolt Physics

The existing implementation will remain useful while alternatives are investigated.

## Development Philosophy

Limnic follows several principles:

### 1. Don't rewrite what already works

A working system is valuable.

### 2. Measure before optimizing

Performance problems should be reproduced and profiled before architectural changes are made.

### 3. Fix tooling before adding complexity

A good development environment makes every later engine feature easier to build.

### 4. Replace systems incrementally

Large engine rewrites are difficult to debug and difficult to learn from.

### 5. Keep the engine understandable

Limnic is also a learning project. Engine code should remain understandable enough that individual systems can be studied, modified, and replaced.

## Status

**Early development**

Limnic Engine is currently being developed from the existing D3ModdingKit/dhewm3 foundation.

The project is not yet intended to be a general-purpose commercial engine.

The immediate goal is to establish a reliable and efficient development environment and determine how far the id Tech 4 foundation can be modernized.

## License

Limnic Engine retains the licensing requirements of its upstream components.

See the repository's license files and upstream projects for the applicable terms.

## Acknowledgements

Limnic Engine would not exist without the work that preceded it.

Special thanks to the developers and contributors of:

* id Software
* Doom 3
* id Tech 4
* dhewm3
* D3ModdingKit

Their work provides the foundation upon which Limnic is being developed.

---

**Limnic Engine**

*A modern engine built by evolving a proven one.*
