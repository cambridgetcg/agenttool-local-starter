# AgentTool Local Starter

A small place for chosen context, handoffs and memory. Keep ordinary notes in
an explicit local folder, then choose how your agent reads them.

**Preview:** `@agenttool/local-starter@0.1.0-dev.0` · **Runtime:** Node 22+

This public repository distributes reviewed release contents. The development
repository remains private. No AgentTool account or hosted service is required.

## Choose an entrance

- [Exact-version manifest and SHA-256](https://docs.agenttool.dev/packages/v1/@agenttool/local-starter/0.1.0-dev.0/manifest.json)
- [GitHub release and standalone archive](https://github.com/cambridgetcg/agenttool-local-starter/releases/tag/local-starter-v0.1.0-dev.0)
- [Setup, capabilities and limits](https://docs.agenttool.dev/LOCAL-CORE.md#files-only-starter)
- [Package guide](plugins/agenttool-local-starter/README.md)

### Install a downloaded archive

npm registry publication is **not yet available**. Download the GitHub release
archive, verify its SHA-256 against the attached manifest, then either extract
it and run `node /absolute/package/dist/cli.mjs`, or install it into a chosen
local prefix:

```sh
npm install --ignore-scripts --prefix ./agenttool-local-preview /absolute/downloads/agenttool-local-starter-0.1.0-dev.0.tgz
```

The CLI has no runtime dependencies; optional MCP dependencies are already
bundled. The embedded package guide's registry-name example is prospective.
The existing npm publisher requires public-source provenance, while this frozen
preview records the private development repository. A later registry release
needs matching public-source metadata and a reviewed publishing workflow.

### Codex plugin

```sh
codex plugin marketplace add cambridgetcg/agenttool-local-starter
codex plugin add agenttool-local-starter@agenttool-local-starter-preview
```

### Claude Code plugin

```sh
claude plugin marketplace add cambridgetcg/agenttool-local-starter
claude plugin install agenttool-local-starter@agenttool-local-starter-preview --scope project
```

Plugin commands follow each host's native trust and installation controls.
They expose the skill only. In Codex invoke `$agenttool-local-context`; in
Claude Code invoke `/agenttool-local-starter:agenttool-local-context`. Select a
notes folder and review a project delivery plan. Installation does not create notes,
start MCP, install hooks or read/save memory. The generated project skill has
a private binding; avoid duplicate plugin and project skills for the same job.

## Your notes stay with you

Keep notes outside this repository, `node_modules` and plugin caches. Initialize
a new folder deliberately; bind an existing starter without initializing it.
MCP is read-only by default. Optional handoff and memory saves replace a fixed
slot with a hash check. Saving a disabled slot never enables future loading.

Skills guide the workflow; MCP offers explicit operations; direct command hooks
supply chosen context at host events. These are independent choices. Hook
support and trust differ by host. Native resume/compaction delivery remains
under verification; a stored note does not establish model receipt or adoption.
There is no automatic transcript capture, backup, revision history, search,
cloud sync, identity assignment or credential discovery.

## Release integrity

`release/manifest.json` records the source revision, artifact size and SHA-256.
`release/SHA256SUMS` covers the attached archive. Files under
`plugins/agenttool-local-starter` are extracted from that exact artifact.
The archive includes Apache-2.0 license and bundled third-party notices.
