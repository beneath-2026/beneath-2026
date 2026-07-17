# beneath-2026

**A complete VFX & animation production pipeline — open-sourced.**

This account collects the tools that drove the pipeline behind ***beneath***,
a student film built with Nuke, Houdini, Blender, DaVinci Resolve, USD, OpenColorIO
and a RenderPal render farm. Every tool here ran in an actual production.

I'm publishing it for three reasons:

1. 🎬 **Showcase** — to show how the pieces of a real pipeline fit together.
2. 🎓 **The next generation of students** — so the people who come after us don't
   start from zero. Take it, learn from it, break it, improve it.
3. ♻️ **Reuse** — so I (and anyone else) can pull these tools into the next project.


---

## 🧰 The tools

Each tool is its own repository so you can grab just the part you need.

| Repository | What it does | Stack |
|---|---|---|
| **`commons`** | Shared config, templates, plugins and the publishing flow used across the pipeline (repo: `tikCommons`). | Python |
| **`DaVinciPipe`** | Syncs the DaVinci Resolve timeline with Kitsu production tracking. | Python |
| **`houdini-tools`** | In-house Houdini HDAs, scripts and hsite setup (caching, render-farm submit, FX). | Houdini / Python |
| **`nuke-tools`** | Nuke `init.py` / `menu.py`, a gizmo auto-loader and a lens-flare tool. | Nuke / Python |
| **`cacheManager`** | Tags and cleans up Houdini caches on the farm. | Python / PySide6 |
| **`renderPal-tools`** | Render-farm backup + hang-detection scripts for RenderPal. | Python |
| **`dcp-tools`** | Builds a Digital Cinema Package (a DCP-o-matic wrapper). | Python |
| **`pipeline-launchers`** | The batch launchers that start each app with the right environment. | Batch |

> All repos are published with fresh git history (so no historic secrets travel) and
> MIT-licensed — take what you need.

---

## ⚠️ What's intentionally *not* here

To keep these repos clean and legal, the following are documented and linked rather
than committed:

- **Third-party apps & plugins** — Blender, the USD build, Houdini plugins
  (GSOPs, Axiom, ZibraVDB), DCP-o-matic, etc.
- **Bundled Python packages** — replaced by a `requirements.txt` in each repo.
- **Licenses & secrets** — paid license keys, internal IPs and credentials have been
  stripped; configs ship as `*.example` files for you to fill in.

---
