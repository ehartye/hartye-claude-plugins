# Marketplace release audit — 2026-11-02

All 21 marketplace version numbers match the published source manifests. Named refs resolve, and every existing SHA pin matches its ref. No newer plain semantic-version tag was found in each repository's latest 100 tags. Exact source revisions and observations are in [the JSON receipt](release-audit-2026-11-02.json).

This update coordinates wiki-master 0.88.0, hartye-skills 0.9.2 and agent-game-studio 0.3.2, pinned to their merged release tags and commits. The other 18 marketplace versions were already current.

agent-draw's GitHub default branch is `feat/agent-draw-vector`, while the marketplace intentionally selects `main`. Its main manifest and v0.5.1 release agree. The audit uses that published branch and does not change repository settings. agent-workflow is checked through its Codex manifest because it has no Claude manifest.

This is a point-in-time source/marketplace audit, not a claim that every user's installed cache has updated. Repositories without a source ref retain their existing default-branch behavior.
