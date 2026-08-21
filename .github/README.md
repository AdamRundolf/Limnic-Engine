<p align="center">
  <img src="https://github.com/AdamRundolf/Limnic-Engine/blob/main/.github/LOGO.png" alt="The logo, what else do you expected?"/>
</p>

# Limnic Engine

**Limnic Engine** is a C++ game engine and development framework built from the **D3ModdingKit / dhewm3 / id Tech 4** codebase.

Limnic uses this existing technology as a foundation for building a modern and flexible engine rather than treating the original architecture as something that must be preserved indefinitely.

Existing systems can be retained, modernized, reorganized, replaced, or removed depending on what the engine actually needs.

> **Build on what already works. Replace what doesn't. Don't preserve limitations for the sake of tradition.**

## Project Goals

Limnic Engine is primarily an **engine development and tooling project**.

The goal is to take a proven classic engine foundation and evolve it into an engine capable of supporting modern game development while remaining understandable and practical to work with.

### Current priorities

* Improve the Radiant level editor
* Fix editor performance and stability problems
* Improve the asset and development workflow
* Establish a flexible gameplay framework
* Modernize graphics capabilities
* Improve navigation and AI tooling
* Support larger and more complex game worlds
* Improve engine architecture where existing systems become limitations
* Maintain compatibility with useful existing game assets and formats
* Keep the engine understandable enough to modify and extend

## Foundations

Limnic Engine originates from technology developed through:

* **id Tech 4**
* **Doom 3**
* **dhewm3**
* **D3ModdingKit**

These projects provide the initial foundation of Limnic.

However, Limnic is **not intended to remain a faithful recreation of Doom 3 or id Tech 4**.

Their technology is a starting point.

Systems that remain useful can be improved and extended. Systems that no longer fit the direction of the engine can be replaced.

## Compatibility Without Architectural Restrictions

Limnic may support established asset formats from other engines and games where doing so provides useful capabilities or access to existing content.

Supporting an asset format does **not** mean reproducing the original engine that created it.

For example, an asset format can be imported and converted into Limnic's own runtime representations while being rendered, animated, simulated, or processed using Limnic's own systems.

This allows Limnic to benefit from existing content without making the architecture dependent on the limitations of another engine.

> **Compatibility is a capability, not a constraint.**

## Why Limnic?

Classic game engines contain decades of engineering work that would be wasteful to simply discard.

The id Tech 4 foundation already provides mature implementations of many difficult systems:

* Real-time 3D rendering
* Materials and shaders
* Dynamic lighting
* Shadows
* Animation
* Skeletal deformation
* Physics
* Spatial audio
* Collision
* World and map processing
* Resource management
* Level editing
* Entity infrastructure
* Core mathematics and utility systems

Limnic can build upon these systems while progressively replacing the parts that limit further development.

The objective is not to rewrite everything.

The objective is to determine **what is worth keeping and what is worth changing**.

## Tooling

Tools are a major part of Limnic Engine.

A good development environment makes the engine itself easier to develop, debug, and understand.

Radiant is therefore one of the first major areas of development.

Development includes:

* Improving viewport performance
* Improving camera controls
* Improving editor responsiveness
* Fixing stability problems
* Improving selection and manipulation
* Improving entity editing
* Improving asset workflows
* Improving debugging and visualization
* Supporting larger scenes
* Making world-building more efficient

The existing editor technology provides a useful starting point rather than something that must eventually be discarded.

# Changes

## 0.0.1 Pre-Alpha

### Radiant Editor

* Improved Radiant performance in the camera viewport.
* Removed unnecessary synchronous window updates during viewport interaction.
* Improved camera flying responsiveness.
* Improved mouse-look responsiveness.
* Reduced unnecessary work during viewport repainting without modifying the renderer.

## Future Plans

### Engine Architecture

Limnic is intended to evolve beyond the original id Tech 4 gameplay architecture.

Existing low-level technology can remain where it provides a useful foundation, while higher-level systems can be redesigned around the requirements of Limnic.

Potential areas of development include:

* Gameplay framework
* Entity and actor systems
* Camera systems
* Scripting
* AI
* Navigation
* Physics integration
* Resource management
* Editor/game integration
* World representation
* Rendering architecture
* Asset pipelines

No individual legacy system is considered permanently untouchable.

## Graphics

Limnic's renderer currently originates from id Tech 4.

Long-term graphics development may include:

* Modern OpenGL support
* Improved shader capabilities
* Improved shadowing
* Cascaded shadow maps
* Soft shadows
* Image-based lighting
* Improved reflections
* Better large-world rendering
* Modern GPU resource management
* Improved material systems

Graphics development will be driven by the needs of Limnic rather than by an attempt to reproduce another engine feature-for-feature.

## Asset Pipeline

Limnic is intended to support a broad range of useful asset formats where practical.

Asset compatibility may include formats originating from other engines and games.

The purpose of this compatibility is to make existing content usable within Limnic, not to force Limnic to reproduce the architecture or runtime behavior of the engine that originally created the content.

Where appropriate, external formats can be translated into Limnic-native representations.

## Navigation

Navigation is planned to move toward a modern navigation system such as **Recast Navigation / Detour**.

This may provide improved support for:

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

The existing implementation remains useful while alternatives are investigated.

## Development Philosophy

Limnic follows several principles:

### 1. Build on what already works

Existing technology represents valuable engineering work.

### 2. Replace what doesn't

Legacy systems are not preserved simply because they are old or familiar.

### 3. Measure before optimizing

Performance problems should be reproduced and investigated before architectural changes are made.

### 4. Fix tooling before adding unnecessary complexity

A better development environment makes future engine development easier.

### 5. Replace systems incrementally

Large rewrites can make development difficult to debug and understand. Systems should be replaced when there is a clear reason to do so.

### 6. Compatibility should not dictate architecture

Supporting an external asset format should not require Limnic to reproduce the engine that created it.

### 7. Keep the engine understandable

Limnic is also an engine-development and learning project. Individual systems should remain understandable enough to study, modify, and replace.

## Status

**0.0.1 Pre-Alpha**

Limnic Engine is in early development and is currently being developed from the D3ModdingKit/dhewm3/id Tech 4 foundation.

The engine is not yet intended to be a finished general-purpose commercial engine.

Development is currently focused on improving the foundation, tooling, architecture, and workflows needed for future engine development.

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

*A new engine built from proven technology.*
