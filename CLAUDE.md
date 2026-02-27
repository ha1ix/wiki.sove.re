# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this wiki is

wiki.sove.re is a cypherpunk/solarpunk encyclopedia tracking the pop-up city, digital nomad, and network-state ecosystem — specifically the lineage of communities that emerged from Vitalik Buterin's Zuzalu experiment (Montenegro, 2023). It is part of the sove.re commons infrastructure (wiki + forum + Mitra microblog) built by and for "soverents" — people interested in self-sovereign, decentralized community models.

The wiki runs on Wiki.js, served at wiki.sove.re, backed by this GitHub repo. Every page has an "Edit on Github" button. Wiki.js serves from the `main` branch.

## Curation standard

**Proximity to Vitalik Buterin is the primary signal for inclusion weight.** Events he personally attended, projects he has commented on or funded, and ideas he has written about are the most valuable content. The further from that signal, the more skeptical to be about whether something is genuine ecosystem vs. opportunistic fad.

High signal: Zuzalu (2023), Edge City (Janine Leger/Timour Kosters), Zupass/0xPARC, ECF/Pensieve, Devcon, d/acc, quadratic funding, DeSci track at these events, ZuVillage lineage.

Low signal / apply scrutiny: projects claiming Zuzalu affiliation with no direct lineage, NFT-based city experiments, grant aggregators without curation, anything primarily token/price motivated.

## Tech stack

- Wiki.js (Node.js), PostgreSQL, Docker Compose at `/opt/services/wikijs/`
- Markdown files with Wiki.js YAML frontmatter
- Caddy reverse proxies wiki.sove.re → localhost:3001

## Style guide

Articles are skeletons — cover the essential concept, link to primary sources, stop. Others will expand over time. Avoid padding with background a reader can find on Wikipedia. One tight paragraph beats three loose ones.

**Factual accuracy is non-negotiable.** Wrong information is worse than no information — it poisons the wiki for every reader after. If uncertain about a specific claim, omit it or link to a primary source rather than paraphrase from memory. Do not fill gaps with plausible-sounding inference.

When creating a new page, also edit the most applicable parent page to add a link. If a page has no inbound links it won't be discovered.

## Content conventions

- All page paths lowercase: `/network-societies/pop-ups/zupass` not `/Pop-Ups/Zupass`
- YAML frontmatter on every page: `title`, `description`, `published: true`, `date`, `tags`, `editor: markdown`, `dateCreated`
- Internal links use root-relative paths: `[Zuzalu](/network-societies/pop-ups/zuzalu)`
- External primary sources (VB articles etc.) are reproduced in full inside `<details>` blocks for permanence
- Wiki.js callout syntax: `> text\n{.is-info}` (info), `{.is-warning}`, `{.is-success}`
- Images stored in repo root or subdirs, referenced as `/image.png`

## Submitting changes

Wayne operates as a collaborator (wayniacal). Propose changes via PR from a feature branch — do not push directly to main. PRs are reviewed and merged by the operator.

```bash
cd /tmp/wayne-wiki   # or wherever cloned
git checkout -b topic/new-page-name
# make changes
git add path/to/file.md
git commit -m "add: topic description"
git push origin topic/new-page-name
# then open PR on github.com/ha1ix/wiki.sove.re
```

## Priority gaps (as of 2025-02)

Missing pages that matter most:
- `people/vitalik-buterin.md` — referenced constantly, no page
- `network-societies/pop-ups/devcon.md` — VB's primary event, ZuVillages cluster around it
- `technology/software/quadratic-funding.md` — VB co-authored paper, Gitcoin built on it
- `philosophy/desci.md` — major Zuzalu track, no page
