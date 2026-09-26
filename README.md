# Hartye Claude Plugins

A collection of Claude Code plugins for agentic development workflows, session
analytics, sprite and 3D model authoring, web-app video production, procedural game audio, document publishing, knowledge management, and Salesforce automation.

## Installation

```bash
# Add the marketplace
/plugin marketplace add ehartye/hartye-claude-plugins

# Install plugins
/plugin install agent-sprites@hartye-plugins
/plugin install agent-meshes@hartye-plugins
/plugin install agent-vids@hartye-plugins
/plugin install agent-beeps@hartye-plugins
/plugin install sf-browser-control@hartye-plugins
/plugin install h-superpowers@hartye-plugins
/plugin install agent-stalker@hartye-plugins
/plugin install md-publisher@hartye-plugins
/plugin install wiki-master@hartye-plugins
/plugin install academia-fetch@hartye-plugins
/plugin install hartye-skills@hartye-plugins
```

## Available Plugins

| Plugin | Description |
|--------|-------------|
| [agent-sprites](https://github.com/ehartye/agent-sprites) | Pixel-art sprite authoring for 2D games with parametric shapes, lighting, animation groups, PNG/Aseprite atlas export, and a live collaborative web UI |
| [agent-meshes](https://github.com/ehartye/agent-meshes) | Named-part 3D authoring for coding agents - rigged, animated GLB models from JSON operations, creature recipes with real gaits, isolated verified builds with renders and offline previews, an embeddable three.js viewer, and an optional Blender refine stage |
| [agent-vids](https://github.com/ehartye/agent-vids) | Marketing and training videos of web apps for coding agents - analyse the app, recommend a brief, storyboard it, and render narrated, captioned video checked against 60 evidence-backed craft rules, with reusable channels and style flavors, and a LAN review page where you pick and order exhibits and finalize the stitched video |
| [agent-beeps](https://github.com/ehartye/agent-beeps) | Procedural game and UI sounds for coding agents - Web Audio patches rendered in Chromium, loudness-matched, measured and checked against cited craft rules, generated as diverse sets from 18 archetypes, and auditioned by you on a LAN listening page (lineup, duels, refine by ear, ship) that trains a taste model predicting your next pick |
| [sf-browser-control](https://github.com/ehartye/sf-browser-control) | Salesforce browser automation via SF CLI - 45+ tools for session management, Lightning navigation, form filling, and Setup automation |
| [h-superpowers](https://github.com/ehartye/hartye-superpowers) | An agentic skills framework for AI coding assistants - composable workflows for planning, TDD, debugging, and code review |
| [agent-stalker](https://github.com/ehartye/agent-stalker) | Track agent team task assignment, messages, and tool use across Claude Code sessions into SQLite with queryable CLI and web dashboard |
| [md-publisher](https://github.com/ehartye/md-publisher) | Turn markdown documents (with embedded mermaid) into themed, searchable, paged PDFs via WeasyPrint and Microsoft Word DOCX via python-docx - 6 bundled themes, interactive custom-theme creation, and a cross-platform Google Fonts installer |
| [wiki-master](https://github.com/ehartye/wiki-master) | Maintain a Karpathy-style LLM wiki on Obsidian via the native obsidian CLI - discover and clip web sources, ingest PDFs/DOCX, then query, lint, and relink them into a cross-referenced knowledge vault |
| [academia-fetch](https://github.com/ehartye/academia-fetch) | Find papers worth reading via OpenAlex, then retrieve them from academia.edu with your own subscription and stage them for wiki-master ingest - human-paced rather than a crawler, with an enforced per-run delay and ceiling, and an open-access short-circuit that skips the subscription when a paper is legitimately free elsewhere |
| [hartye-skills](https://github.com/ehartye/hartye-skills) | General-purpose utility skills that are useful across unrelated projects but too small to justify a plugin each - beautiful, for distinctive frontend design that avoids templated AI aesthetics, and ship-it, which collapses commit, branch, push, PR and squash-merge into one step |

### Agent Sprites setup and upgrades

After installing or updating `agent-sprites`, run `/agent-sprites:sprite-setup`.
It installs the CLI outside the plugin cache, links it, and checks plugin/CLI/server
version sync. Sprite skills always use the matching managed install. See the
[Agent Sprites installation guide](https://github.com/ehartye/agent-sprites#install)
for details. If upgrading from `claude-sprites`, install `agent-sprites` and disable
the old plugin to avoid duplicate commands. Existing saved sessions remain compatible.

Version 0.15.3 includes eleven native skills, offline atlas verification, isolated
project builds with playable previews, and a copyable four-beat character walk
recipe. See the [build workflow](https://github.com/ehartye/agent-sprites#build-a-repeatable-asset-project).

### Agent Meshes setup

After installing or updating `agent-meshes`, run `/agent-meshes:mesh-setup`. The plugin cache is a
bare checkout, so setup copies the runtime outside it, installs dependencies, builds the workbench,
installs Chromium for renders and links the CLI; every mesh skill then runs through the checked
launcher. Node.js 24 or newer is required. Blender is optional and needed for authored meshes and the refine stage.

Version 0.4.0 adds smooth walk and light jog clips with bent-arm swing,
torso counterrotation and grounded heel-to-toe foot roll. Adult, child, alien
and vacuum-suit variants share body measurements, skin bindings and repeatable gaits. The
[recipe guide](https://github.com/ehartye/agent-meshes/blob/main/recipes/README.md)
explains copying them from the plugin/source checkout into validated asset builds.

### Agent Vids setup

After installing or updating `agent-vids`, run `/agent-vids:vid-setup`. Setup copies the runtime outside
the plugin cache, installs dependencies (including a static ffmpeg), installs Chromium for capture and
links the `vids` CLI. Node.js 24 or newer is required. Narrated renders use OpenAI text-to-speech and
need `OPENAI_API_KEY`; silent drafts (`--draft`) work without it.

To let the owner choose what goes in a video, give a storyboard more exhibits than it needs and
`"select": { "pick": N }`, run `vids candidates`, and open the review page: it previews every
exhibit with a score and the agent's notes, and its Finalize button stitches the chosen set without
recapturing. Capture asks Chromium for the GPU, so WebGL apps record smoothly; the report names the
renderer and warns when a scene falls below 15 fps.

### Agent Beeps setup

After installing or updating `agent-beeps`, run `/agent-beeps:beeps-setup`. Setup copies the runtime outside
the plugin cache, installs dependencies and Chromium (every sound is rendered by the browser's own Web Audio
engine) and links the `beeps` CLI. Node.js 24 or newer is required.

Agents seal a prediction, then send you a link to the listening page (`http://<host>:47301/s/<id>?t=<token>`,
plus an IP-address link for phones). Keep and dud a lineup, duel the keepers, nudge the winner brighter,
darker, punchier or shorter, and ship it into the project's kit. Your explicit choices build a taste profile
across projects (`beeps taste show`); other machines need the firewall to allow Node on port 47301.

## License

MIT
