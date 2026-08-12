# RetroSai Achievements

A **static snapshot** of an offline RetroAchievements profile, generated
2026-08-12 02:45.

* `index.html` - headline stats, recent unlocks and the per-game progress list.
* `game/<id>.html` - every achievement for one game.
* `data.json` - the same numbers as plain JSON, if you would rather read them that way.
* `badges/`, `icons/` - only the art the exported pages actually reference.

Everything is self-contained: no CDN, no web font, no analytics, no external request of
any kind. Every link is relative, so it works from a subdirectory (which is what a GitHub
Pages *project* site is), from a plain file server, and straight off disk with `file://`.

## This is a snapshot

It does not update by itself. The achievements are earned on a local cab against a local
server; this folder is a copy of how things looked at the moment it was generated. Re-run
the export to refresh it.

## Publishing it

1. `git init` in this folder (once), commit everything, push it to a repository.
2. In the repository's **Settings -> Pages**, set *Source* to the branch and folder that
   hold these files.
3. The site appears at `https://<user>.github.io/<repo>/`.

`.nojekyll` is included so Pages serves every path unchanged instead of running Jekyll.

## Generated

This folder is generated output - edit the exporter, not the files here. Anything the
export does not produce is left alone, so `.git`, `CNAME` and friends survive a re-run.
