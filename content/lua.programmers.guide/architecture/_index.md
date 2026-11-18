---
title: architecture
id: architecture
weight: 20
draft: true
author: "people"
---

_This section is not yet written._ It will describe how Lua fits into darktable, both in the source tree and in an installed release:

- **[darktable](darktable/_index.md)** — where Lua lives in darktable's **source**: the embedded Lua code (`#ifdef USE_LUA`), darktable's own `lua` code, and the external projects (`lua`, `lua-scripts`); and how it is laid out in a **release** (the `share` directory).
- **[lua-scripts](lua-scripts/_index.md)** — the bundled script collection and how it is organised.
- **[userspace](userspace/_index.md)** — the user's configuration directory and where personal scripts go.
