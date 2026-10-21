# Hartye Claude Plugins

A collection of Claude Code plugins for agentic development workflows, session
analytics, sprite, layered vector and 3D model authoring, web-app video production, procedural game audio, writing craft, evidence-led project marketing, document publishing, knowledge management, and Salesforce automation.

## Installation

```bash
# Add the marketplace
/plugin marketplace add ehartye/hartye-claude-plugins

# Install plugins
/plugin install agent-sprites@hartye-plugins
/plugin install agent-draw@hartye-plugins
/plugin install agent-meshes@hartye-plugins
/plugin install agent-vids@hartye-plugins
/plugin install agent-beeps@hartye-plugins
/plugin install agent-prose@hartye-plugins
/plugin install agent-engine@hartye-plugins
/plugin install agent-marketing@hartye-plugins
/plugin install sf-browser-control@hartye-plugins
/plugin install h-superpowers@hartye-plugins
/plugin install agent-stalker@hartye-plugins
/plugin install md-publisher@hartye-plugins
/plugin install wiki-master@hartye-plugins
/plugin install academia-fetch@hartye-plugins
/plugin install hartye-skills@hartye-plugins
/plugin install agent-tests@hartye-plugins
```

## Available Plugins

| Plugin | Description |
|--------|-------------|
| [agent-sprites](https://github.com/ehartye/agent-sprites) | Pixel-art sprite authoring for 2D games with parametric shapes, lighting, animation groups, PNG/Aseprite atlas export, and a live collaborative web UI |
| [agent-draw](https://github.com/ehartye/agent-draw) | Vector-first 2D art: editable layered SVG and PNG/PDF, independently drawn pose sequences, named-part keyframe animation and Phaser atlases; craft guidance for anatomy, action, textures, color and world scale |
| [agent-meshes](https://github.com/ehartye/agent-meshes) | Named-part 3D authoring - rigged, animated GLBs, verified builds and offline previews; declared native inputs and fixed environments, project roots, pins, shared batches and bounded rollback reuse; configured Unreal static-prop geometry/collision inspection; mesh arrays preserving corner UVs and FLOAT_COLOR masks; runtime bytecode filtering and vertex RGB previews; project-owned faces, researched tool selection, rig banks and character craft |
| [agent-vids](https://github.com/ehartye/agent-vids) | Marketing and training videos of web apps for coding agents - analyse the app, recommend a brief, storyboard it, and render narrated, captioned video checked against 60 evidence-backed craft rules, with reusable channels and style flavors, and a LAN review page where you pick and order exhibits and finalize the stitched video |
| [agent-beeps](https://github.com/ehartye/agent-beeps) | Procedural game and UI sounds for coding agents - Web Audio patches rendered in Chromium, loudness-matched, measured and checked against cited craft rules, generated as diverse sets from 18 archetypes, and auditioned by you on a LAN listening page (lineup, duels, refine by ear, ship) that trains a taste model predicting your next pick |
| [agent-prose](https://github.com/ehartye/agent-prose) | Writing craft for coding agents: textbook lessons and reader adaptation for U.S. grades 4–12, dialogue, instructions, academic/professional prose, scripts, speeches, poems, lyrics, presentations and webinars. Nineteen skills, native drafts, cited craft checks, scoped readability diagnostics and attributed reference excerpts; voice bibles, variants, owner reviews and learned taste, LAN reading comparisons, style audit and offline exports. Reader profiles and formula estimates remain distinct from comprehension testing. |
| [agent-engine](https://github.com/ehartye/agent-engine) | Engine selection and sprite/mesh/audio integration across Unity, Unreal, UEFN, Godot and web engines; runnable web 3D examples (React Three Fiber, Babylon.js) with GPU verifiers; guarded Unreal GLB import reuse with per-mesh import policy; a Niagara reference for Unreal 5.8 with a validation scene and a template catalog; an Unreal side-by-side comparison scene; an explorable Niagara showcase |
| [agent-marketing](https://github.com/ehartye/agent-marketing) | Evidence-led project marketing: audience and channels, paying-demand and non-English market research with sourced reports, campaigns, collateral, monitoring, reception and experiment decisions; nine skills, a portable ledger, Node CLI and local campaign desk |
| [sf-browser-control](https://github.com/ehartye/sf-browser-control) | Salesforce browser automation via SF CLI - 45+ tools for session management, Lightning navigation, form filling, and Setup automation |
| [h-superpowers](https://github.com/ehartye/hartye-superpowers) | An agentic skills framework for AI coding assistants - composable workflows for planning, TDD, debugging, and code review |
| [agent-stalker](https://github.com/ehartye/agent-stalker) | Track agent team task assignment, messages, and tool use across Claude Code sessions into SQLite with queryable CLI and web dashboard |
| [md-publisher](https://github.com/ehartye/md-publisher) | Turn markdown documents (with embedded mermaid) into themed, searchable, paged PDFs via WeasyPrint and Microsoft Word DOCX via python-docx - 6 bundled themes, interactive custom-theme creation, and a cross-platform Google Fonts installer |
| [wiki-master](https://github.com/ehartye/wiki-master) | Maintain a Karpathy-style LLM wiki on Obsidian via the native obsidian CLI - discover and clip web sources, ingest PDFs/DOCX, then query, lint, and relink them into a cross-referenced knowledge vault |
| [academia-fetch](https://github.com/ehartye/academia-fetch) | Find papers worth reading via OpenAlex, then retrieve them from academia.edu with your own subscription and stage them for wiki-master ingest - human-paced rather than a crawler, with an enforced per-run delay and ceiling, and an open-access short-circuit that skips the subscription when a paper is legitimately free elsewhere |
| [hartye-skills](https://github.com/ehartye/hartye-skills) | General-purpose utility skills that are useful across unrelated projects but too small to justify a plugin each - beautiful, for distinctive frontend design that avoids templated AI aesthetics, and ship-it, which collapses commit, branch, push, PR and squash-merge into one step |
| [agent-tests](https://github.com/ehartye/agent-tests) | Test-efficiency toolkit for coding agents - structure tests by project phase and risk, and audit a suite for redundant coverage, compat and fallback shim tests, worktree-hostile tests, unwired tests and tests that run too often. Evidence from a Node CLI, verdicts from the agent; three skills for TypeScript and JavaScript projects (vitest or jest) |
| [agent-workflow](https://github.com/ehartye/agent-workflow) | Codex workflow authoring and execution with durable JS orchestration, parallel agents, item-local pipelines, reviewed artifact handoffs, immutable capture policy and an authenticated session dashboard. Four skills and nine recipes; Windows verified. |

### Agent Workflow in Codex

`agent-workflow` 0.6.0 is a Codex plugin using managed ChatGPT subscription authentication, without a custom MCP server or API-key billing fallback. New runs retain verified capability source packages so host cache updates do not remove admitted skill sources. Version 0.6 adds declared steps before workers start, depth-one reusable child workflows, explicit trusted-LAN dashboards and complete native-readable skill-local resources. Live independent tasks, revisioned worker deadline controls and durable command/observer evidence remain available. Add or refresh this marketplace in Codex's plugin browser and install `agent-workflow@hartye-plugins`, or use the CLI:

```sh
codex plugin marketplace add ehartye/hartye-claude-plugins
codex plugin add agent-workflow@hartye-plugins
```

After installation, run `$agent-workflow:workflow-setup` with Node 24+ available. Setup installs fingerprinted production dependencies outside the plugin cache. CLI and hooks share AGENT_WORKFLOW_DATA_DIR or the platform default; prior runtime directories and saved data are preserved. Installation does not enable optional hooks automatically. See the [v0.6.0 release](https://github.com/ehartye/agent-workflow/releases/tag/v0.6.0) and [setup guide](https://github.com/ehartye/agent-workflow#install-and-start). Windows MXC Session 0 compatibility is an explicitly authorized launch option; setup explains its shared UI tradeoff and verifies the actual context. The entry pins that release commit; Claude Code runtime compatibility is not claimed.

New workflows default to the originating parent's explicitly recorded execution access, with restricted execution available by choice. New runs retain complete admitted plugin and skill packages with verified provenance and preserve their layouts for genuine native discovery and reads. Selected skills still require successful native main-resource activation and source verification; copied files do not substitute for activation. Saved runs reuse their retained source identities, and changed backend configuration blocks replay before completed work can repeat. Older runs retain their original runtime and source checks. External managed runtimes, mutable homes, services and host-only connectors are not frozen or cloned. Full-access worktrees organize ownership and artifact review; they do not enforce filesystem isolation. Windows uses a verified signed process host, and bounded workspace captures support up to 512 MiB.

The Map + inspector session dashboard stays available until explicitly closed, uses readable phone cards and a closable sheet, retains dismissed messages, and separates phase membership, execution dependencies and task acceptance. An immutable capture policy can exclude approved generated directories while retaining reviewable metadata. Reversible hide/archive preserves outcomes; separate reviewed prune plans retire only eligible payloads while retaining audit and recovery evidence. Workflow authoring guides decomposition, worker prerequisites and explicit artifact handoffs; dependencies do not transfer predecessor edits automatically.

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

### Agent Draw setup

After installing or updating `agent-draw`, run `/agent-draw:draw-setup` in Claude Code
or `$agent-draw:draw-setup` in Codex. Codex users can add this marketplace and install it with:

```sh
codex plugin marketplace add ehartye/hartye-claude-plugins
codex plugin add agent-draw@hartye-plugins
```

Node.js 22+ and an existing Inkscape 1.2+ installation are required. Setup copies and checks a
fingerprint-matched runtime outside the plugin cache; it does not install Inkscape or download
npm dependencies. No browser or MCP server is required. Linux is the initial verified platform;
native Windows exports have been checked with an explicit Inkscape executable. Automatic Windows discovery and macOS support remain unverified.

Use `draw-authoring` to create and validate JSON projects, then `draw-export` to build editable
SVG with named Inkscape layers, transparent PNG, PDF, and a build receipt. Keep the project JSON
with the outputs for repeatable builds. SVG retains live editable text; PDF text is outlined.
Manual SVG edits do not round-trip into the JSON source.

Version 0.5.0 adds native bitmap lettering (`font-atlas`) with fixed-cell BMFont XML, editable
glyph sheets and hash receipts. It also bundles 768 human/compact-RPG starters in elevated and
overhead facings, construction guides and walk/run galleries. New craft guidance covers
view-specific anatomy, boot clearance, selective ink and shared character/path perspective.
Fixed cells do not supply measured bearings or kerning.

Independently drawn pose sequences take an ordered manifest of complete static
JSON drawings and export editable SVG/PNG frames and an all-frame contact sheet, preserving source
projects and receipts. Craft guidance covers anatomy, action staging, textures, color families
and person/building scale. Named-part pivot/keyframe animation remains available for reusable
parts. Optional GIF/MP4 encoding and Phaser JSON hash atlas packing require an existing FFmpeg
installation; setup does not install it. Atlases preserve fixed-canvas anchors, named clips and
transparent gutters. Packing does not generate missing directional poses. See the
[Agent Draw installation and workflow guide](https://github.com/ehartye/agent-draw/blob/main/README.md#quick-start)
and [drawn-pose sequence format](https://github.com/ehartye/agent-draw/blob/main/docs/sequence-format.md).

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

### Agent Prose setup

After installing or updating `agent-prose`, run `/agent-prose:prose-setup`. Setup copies the runtime outside
the plugin cache, installs its dependencies and links the `prose` CLI. Node.js 24 or newer is required.

Skills draft in Fountain, Markdown with frontmatter, or a `prose/dialog@1` YAML graph, then run `prose lint`
and report measured numbers - duration, pages, words per minute, line lengths - instead of estimates. The
`prose-review` skill offers you several measurably different rewrites to choose between and records your pick
(`prose taste stats` shows how often the agent's sealed guess matched it). The `prose-poetry` and
`prose-songwriting` skills check verse and lyrics for syllables, rhyme and form (US English pronunciations, with guessed words listed).
`prose serve` starts a LAN reading page for those choices: anyone on your network with the link can read the drafts of the projects it
serves, so use `--local` to keep it on your machine.
`prose init` creates a project for voice bibles and per-form overrides such as a game's text-box size.

Version 0.6.0 adds eight craft reference guides covering all 24 forms (`prose guide`), character and
context briefs with the current line beside rewrite options, side-by-side comparison, batch review of
up to 50 sets, and line strikes with reasons and confirmed apply/undo. Choose **None of these** to send
variants back with feedback; the agent carries that feedback into the next round. Fourteen skills
include `prose-strike` and `prose-review-batch`.

### Agent Marketing setup

After installing or updating `agent-marketing`, run `/agent-marketing:market-setup`. It installs and
checks the content-verified runtime outside the plugin cache. Node.js 24 or newer is required;
there are no runtime npm dependencies. Use `/agent-marketing:market-research` for demand and
non-English market questions, and `/agent-marketing:market-monitor` for the local campaign desk.
See the [installation and CLI guide](https://github.com/ehartye/agent-marketing#install-the-plugin).

## License

MIT
