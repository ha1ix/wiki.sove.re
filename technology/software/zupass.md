---
title: Zupass
description: ZK identity and credential system originating from Zuzalu 2023
published: true
date: 2026-02-27T00:00:00.000Z
tags: technology, software, zuzalu, identity, privacy, zk
editor: markdown
dateCreated: 2026-02-27T00:00:00.000Z
---

# Overview

Zupass is a zero-knowledge proof-based identity and credential system developed by [0xPARC](https://0xparc.org/) for [Zuzalu](/network-societies/pop-ups/zuzalu) in 2023. It lets users prove membership in a group or possession of a credential without revealing which specific person they are. It began as a way to prove "you are a Zuzalu resident" for access control, polling, and event sign-in, and has since become the primary identity layer across the [ZuVillage](/network-societies/pop-ups/zuvillage) ecosystem.

Vitalik Buterin described it in [Why I Built Zuzalu](/network-societies/pop-ups/zuzalu/why-vb): *"The 0xPARC team created Zupass, an identity system based on zero-knowledge proofs that you could use to prove that you were a resident of Zuzalu without revealing which one."*

# How It Works

Zupass stores credentials ("PCDs" — Proof-Carrying Data) in a client-side wallet. A credential might be: "ticket to Edge City Lanna," "Ethereum core dev," or "voted in this poll." Using ZK proofs, holders can prove predicates about their credentials — "I hold a valid ticket" or "I voted once" — without revealing the underlying data.

The core primitive is the **PCD (Proof-Carrying Data)** framework, an abstraction for any object that carries a verifiable claim. Different PCD types wrap different proof systems (RSA ticket signatures, Semaphore group membership, EdDSA signatures, etc.). Applications request specific PCD types; Zupass generates the proof client-side.

Key properties:
- **Client-side**: private keys and credentials never leave the user's device
- **ZK proofs**: selective disclosure — prove what's needed, nothing more
- **Composable**: any app can request any PCD type; Zupass is a general wallet, not app-specific
- **Pseudonymous by default**: proving group membership does not reveal identity

# Usage Across the Ecosystem

Zupass has been deployed at every major ZuVillage since 2023:

- **Zuzalu 2023** — resident identification, anonymous polling via [Zupoll](https://zupoll.org/)
- **Edge City Esmeralda, Crecimiento, Lanna** — event ticketing and access
- **ETHChiangmai, Devcon side events** — ticket gating, vote proofs
- **[Zuzalu.city](/technology/software/zuzalu-city)** — integrated as the primary identity/credential layer

The [Zupass.org](https://zupass.org/) app is the user-facing wallet. [Zupoll](https://zupoll.org/) and ZuCast are built on top of it.

# Significance

Zupass is one of the few pieces of social technology that emerged from the original Zuzalu experiment, was battle-tested in real use, iterated on user feedback, and propagated across subsequent events. Vitalik cited it as evidence that the "incubating novel technologies within a dedicated community" model actually works.

It is also a proof-of-concept for the broader d/acc thesis: that privacy-preserving identity tools are buildable and usable today, not theoretical. The shift from "you must identify yourself to access this space" to "you must prove a predicate about yourself" is the practical application of [programmable cryptography](/technology/software/programmable-cryptography) to everyday community coordination.

# Technical Resources

- [Zupass GitHub](https://github.com/proofcarryingdata/zupass) — open source
- [PCD framework documentation](https://github.com/proofcarryingdata/zupass/tree/main/packages/pcd-types)
- [0xPARC on programmable cryptography](https://0xparc.org/blog/programmable-cryptography-1)
- [Zupoll](https://zupoll.org/) — anonymous polling built on Zupass

# See Also

- [Programmable Cryptography](/technology/software/programmable-cryptography)
- [Privacy Software](/technology/software/privacy)
- [Zuzalu.city](/technology/software/zuzalu-city)
- [Zuzalu](/network-societies/pop-ups/zuzalu)
