# AgeVolt Creator

Public bootstrap plugin for AgeVolt AI Agent.

The plugin itself is deliberately thin. Its job is to:

1. load as an upgradable Git marketplace plugin,
2. locate the locally synced SharePoint `AI Agent` folder,
3. hand off to the internal Creator rules stored there,
4. avoid publishing internal KB and rules to GitHub.

Internal content must stay in SharePoint unless AgeVolt explicitly decides to publish a public module.
