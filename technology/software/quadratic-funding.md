---
title: Quadratic Funding
description: Mechanism for democratically allocating matching funds to public goods
published: true
date: 2026-02-27T00:00:00.000Z
tags: technology, funding, governance, ethereum
editor: markdown
dateCreated: 2026-02-27T00:00:00.000Z
---

# Overview

Quadratic Funding (QF) is a mechanism for allocating matching funds to public goods projects. It was introduced in the 2018 paper *Liberal Radicalism: A Flexible Design For Philanthropic Matching Funds* by [Vitalik Buterin](/people/vitalik-buterin), Zoë Hitzig, and E. Glen Weyl.

The core insight: matching funds should be proportional to the **number of contributors**, not the total amount raised. A project with 100 people each donating $1 signals broader legitimacy than one person donating $100 — QF rewards the former more heavily.

# The Mechanism

Each project's match is proportional to the square of the sum of the square roots of individual contributions:

```
match ∝ ( √c₁ + √c₂ + ... + √cₙ )²
```

This means small contributions from many people are amplified more than large contributions from few. It operationalizes the idea that community support — not wealth — should determine what gets funded.

# Gitcoin

[Gitcoin](https://gitcoin.co) is the primary implementation of QF for the Ethereum ecosystem. Its Gitcoin Grants program has run multiple rounds funding open source software, community infrastructure, and public goods projects — many of them directly adjacent to the ZuVillage and network-state ecosystem.

# Significance

QF is one of the cleaner examples of a governance mechanism that emerged from the crypto/Ethereum intellectual tradition and has been applied in practice at scale. It sits at the intersection of [pluralism](/philosophy/pluralism) (weighting breadth of support across diverse contributors) and the d/acc principle of building infrastructure that resists capture by large actors.

Glen Weyl, one of the paper's co-authors, is also co-author of the [Plurality](/philosophy/pluralism) book.

# Primary Sources

- [Liberal Radicalism paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3243656) — Buterin, Hitzig, Weyl (2018)
- [Gitcoin.co](https://gitcoin.co)

# See Also

- [Pluralism](/philosophy/pluralism)
- [Grants](/misc/grants)
- [Ethereum](/technology/software/ethereum)
