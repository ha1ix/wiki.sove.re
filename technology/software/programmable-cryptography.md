---
title: Programmable Cryptography
description: 
published: true
date: 2024-12-09T14:44:43.885Z
tags: technology, cryptography
editor: markdown
dateCreated: 2024-11-29T11:07:29.400Z
---

See the [overview by 0xParc](https://0xparc.org/blog/programmable-cryptography-1)

# "God Protocols"
[Vitalik's description](https://vitalik.eth.limo/general/2024/10/29/futures6.html#5) (quotes below) of extremely powerful types of cryptography that will revolutionize certain types of software.

# Zero Knowledge Proofs
Specifically [ZK-Snarks](https://vitalik.eth.limo/general/2021/01/26/snarks.html) "allow a user to prove any arbitrary statement about data that they hold, in a way that the proof (i) is easy to verify, and (ii) does not leak any data other than the statement itself... But ZK-SNARKs have an important limitation: you need to know the data to make proofs about it. Each piece of state in a ZK-SNARK application must have a single "owner", who must be around to approve any reads or writes to it."
# [Fully Homomorphic Encryption (FHE)](https://vitalik.eth.limo/general/2020/07/20/homomorphic.html)
"FHE lets you do any computation on encrypted data without seeing the data. This lets you do computations on a user's data for the user's benefit while keeping the data and the algorithm private... But FHE too has its limits: any FHE-based technology still requires someone to hold the decryption key."
# [Indistinguishability Obfuscation](https://en.wikipedia.org/wiki/Indistinguishability_obfuscation)
"Indistinguishability obfuscation lets you create an "encrypted program" that performs an arbitrary computation, in such a way that all internal details of the program are hidden."