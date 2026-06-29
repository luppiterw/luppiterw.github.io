# Hug Project

This file lets `hug_scripts` understand this repository without becoming the
source of truth for the repository itself.

## Repo

- name: luppiterw.github.io
- status: archived
- updated: 2026-06-29
- vcs: git
- default_branch: main

## Workspace Profiles

```yaml
workspace:
  schema: "hug.workspace.v2"
  workspace_paths:
    - "luppiterw.github.io"
  root_sets:
    - "luppiter-projects"
  root_sources:
    - "<workspace-root>/hug_scripts/project-tools/workspace-roots.md"
    - ".hug/local/workspace-roots.yaml"
  root_selection:
    - "If running inside this checkout, derive <workspace-root> by removing a matching workspace_paths suffix from the current path."
    - "Otherwise read root_sources and choose a profile matching the current OS/runtime."
    - "Use an existing root from roots."
    - "Prefer the current worktree when multiple roots match."
```

## Source Of Truth

- repository_overview: README.md

## Entrypoints

- repository_overview: `README.md`

## Hug Scan

- include:
  - README.md
  - .hug/project.md
- exclude:
  - .hug/local/
  - .git/
  - _site/
  - dist/
  - build/

## Maintenance

Update this file when canonical document paths, important subprojects,
entrypoints, or scan boundaries change.
