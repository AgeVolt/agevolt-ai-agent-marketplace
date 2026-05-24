# AgeVolt AI Agent Marketplace

Public bootstrap marketplace for AgeVolt Codex plugins.

This repository is intentionally small and public-safe. It should not contain internal knowledge base files, customer data, credentials, exports, source system payloads, or private AgeVolt documentation.

The internal source of truth remains the SharePoint folder:

```text
AI Agent/
```

The Git marketplace exists so Codex can install and upgrade the bootstrap plugin through the normal Git marketplace flow. The bootstrap plugin then points Codex to the locally synced SharePoint `AI Agent` folder for internal rules and module contracts.

## Install

In Codex:

```text
Add marketplace AgeVolt/agevolt-ai-agent-marketplace
Install AgeVolt Creator
```

CLI equivalent:

```powershell
codex plugin marketplace add AgeVolt/agevolt-ai-agent-marketplace
```

Then install `AgeVolt Creator` from the Codex plugin UI.

## Upgrade

Because this is a Git marketplace, Codex can upgrade it through the normal marketplace upgrade flow.

CLI equivalent:

```powershell
codex plugin marketplace upgrade agevolt-ai-agent
```

## Rules

- Keep this repo public-safe.
- Put only bootstrap plugin metadata and public instructions here.
- Keep internal rules, KB, fixtures, and module work in SharePoint `AI Agent`.
- Bump `.codex-plugin/plugin.json` version for every plugin behavior change.
