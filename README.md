# s3walk [![build](https://travis-ci.org/saplineworks/s3walk.svg?branch=main)](https://travis-ci.org/saplineworks/s3walk) [![schema](https://img.shields.io/badge/manifest-v2-informational.svg)](#) [![license](https://img.shields.io/badge/license-CC--BY--4.0-lightgrey.svg)](LICENSE)

> The repo IS the gallery entry — push, wait for approval, the Wall updates itself.

[<img src="https://raw.githubusercontent.com/duskwellco/s3walk/7b21dd8/docs/s3walk-mark.png" align="right" width="150">](https://s3walk.dev/)

<details>
<summary>index</summary>

```text
s3walk/
├── providermodule     artifact map
├── alerting           hero rules
├── javisoto           stack manifest
├── PngWatermarker     dispatches
├── media-tech         pre-flight
├── SDevCircleButton   moderation
├── chain-of-verification  layout
├── DocSets-for-iOS    categories
├── gimei              rough edges
└── spring-session-jdbc    patches
```

</details>

Everything below is written in GitHub Flavoured Markdown; the Wall re-renders your entry on every push.

## providermodule

| path | kind | what it is |
|---|---|---|
| `entry_summary.md` | prose | title, intent, final state of the work |
| `stack_manifest.json` | data | declared toolkits, platforms, APIs, themes |
| `dispatches/` | posts | one file per update |
| `stills/` | media | images used by the summary and the dispatches |
| `kit/` | code | sources and stable drops, structured however you like |
| `hero.jpg` | media | the single image shown in the gallery grid |

### alerting

**hero.jpg**
    replace the placeholder in `stills/` — 1280 x 640 jpeg is the sweet spot

**fallback**
    with no hero, the newest dispatch image is used; with no dispatch image either, the entry stays off the Wall
#### javisoto

```json
{
  "stack": {
    "apis": ["Speech Input", "Map Tiles"],
    "platforms": ["Container Runtime"],
    "toolkits": ["Node.js", "Three.js", "DuckDB"]
  },
  "themes": ["Cartography", "Fog", "Signals"]
}
```

Languages are inferred from the repo, so leave them out. Anything declared here becomes a search facet on the Wall — validate the file with a strict JSON validator before you push.

## PngWatermarker

```bash
# one dispatch per update, slug in lower case
cp dispatches/_example.md dispatches/2026-04-11-fog-pass.md
# at least four dispatches before the entry is eligible
```

A dispatch is a running log of the process — early thumbnails, dead ends, working builds. Links, stills and embedded video are all fair game.

### media-tech

1. `entry_summary.md` filled out, hero replaced
2. `stack_manifest.json` declares every toolkit and theme you actually used
3. four dispatches minimum, oldest first
4. no image larger than 1440 x 1440 in the summary or the dispatches
5. video hosted off-repo, referenced as an embed link
#### SDevCircleButton

> Pushes land in a review queue first: your own view updates immediately, everyone else sees it once a moderator approves. Flagged dispatches get pulled, and an entry that keeps getting flagged can be re-forked from scratch.

## chain-of-verification

```text
s3walk/
├── entry_summary.md
├── stack_manifest.json
├── dispatches/
│   ├── _example.md
│   └── 2026-04-11-fog-pass.md
├── stills/
│   ├── hero.jpg
│   └── fog-02.png
└── kit/
    ├── src/
    └── drops/
```

## DocSets-for-iOS

| category | who fills it |
|---|---|
| toolkits / platforms / apis | you, in the manifest |
| languages | inferred from the repo |
| themes | tags, free-form |

## gimei

* keep one topic per dispatch — the queue reads them in order
* stills referenced from the summary must live in `stills/`
* the Wall caches renders; a hard refresh after approval is normal
* deleting a dispatch later does not reopen the entry

## spring-session-jdbc

| step | action |
|---|---|
| 1 | fork `saplineworks/s3walk` |
| 2 | branch from `main`, keep the tree above |
| 3 | push, then wait for the queue to clear |
| 4 | mark the entry complete from the entry page |

> Entry text is CC-BY-4.0; the scaffold itself is covered by its own `LICENSE`.