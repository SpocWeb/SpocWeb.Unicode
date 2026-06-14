# SpocWeb.Unicode

<!-- digest-map
local-classes:
folders:
folder_digest: e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855
folder_mtime: 2026-05-19T00:00:00Z
-->

Resource project providing Unicode character data and emoji
tables as embedded resources for use by SpocWeb.Text
and other projects.

This project contains no compiled source code — it packages
Unicode character name databases, emoji sequences, and
related data files as embedded resources referenced by
`SpocWeb.Text.data.text.Unicode`.

## Architecture

```mermaid
flowchart LR
  unicode["SpocWeb.Unicode\n(resource project)"]
  text["SpocWeb.Text\nSpocWeb.Text.data.text.Unicode"]
  locales["per-locale folders\n(~80 language sub-folders)"]
  icons["_Icons/\nEmoji & symbol data"]

  locales --> unicode
  icons --> unicode
  unicode -->|"EmbeddedResource"| text
```
