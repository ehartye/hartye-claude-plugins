# Hartye Claude Plugins

A collection of Claude Code plugins for agentic development workflows, session
analytics, document publishing, knowledge management, and Salesforce automation.

## Installation

```bash
# Add the marketplace
/plugin marketplace add ehartye/hartye-claude-plugins

# Install plugins
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
| [sf-browser-control](https://github.com/ehartye/sf-browser-control) | Salesforce browser automation via SF CLI - 45+ tools for session management, Lightning navigation, form filling, and Setup automation |
| [h-superpowers](https://github.com/ehartye/hartye-superpowers) | An agentic skills framework for AI coding assistants - composable workflows for planning, TDD, debugging, and code review |
| [agent-stalker](https://github.com/ehartye/agent-stalker) | Track agent team task assignment, messages, and tool use across Claude Code sessions into SQLite with queryable CLI and web dashboard |
| [md-publisher](https://github.com/ehartye/md-publisher) | Turn markdown documents (with embedded mermaid) into themed, searchable, paged PDFs via WeasyPrint and Microsoft Word DOCX via python-docx - 6 bundled themes, interactive custom-theme creation, and a cross-platform Google Fonts installer |
| [wiki-master](https://github.com/ehartye/wiki-master) | Maintain a Karpathy-style LLM wiki on Obsidian via the native obsidian CLI - discover and clip web sources, ingest PDFs/DOCX, then query, lint, and relink them into a cross-referenced knowledge vault |
| [academia-fetch](https://github.com/ehartye/academia-fetch) | Find papers worth reading via OpenAlex, then retrieve them from academia.edu with your own subscription and stage them for wiki-master ingest - human-paced rather than a crawler, with an enforced per-run delay and ceiling, and an open-access short-circuit that skips the subscription when a paper is legitimately free elsewhere |
| [hartye-skills](https://github.com/ehartye/hartye-skills) | General-purpose utility skills that are useful across unrelated projects but too small to justify a plugin each - beautiful, for distinctive frontend design that avoids templated AI aesthetics, and ship-it, which collapses commit, branch, push, PR and squash-merge into one step |

## License

MIT
