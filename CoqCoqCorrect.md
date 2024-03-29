---
layout: default
permalink: /coqcoqcorrect
title:  "Coq Coq Correct!"
date:   2019-11-15 08:00:00 +0100
---

Coq Coq Correct! Verification of Type Checking and Erasure for Coq, in Coq
===============

Matthieu Sozeau, Simon Boulier, Yannick Forster, Nicolas Tabareau, and Théo Winterhalter. 2020. 
[Coq Coq Correct! Verification of Type Checking and Erasure for Coq, in Coq](https://doi.org/10.1145/3371076)
Proc. ACM Program. Lang. 4, POPL, Article 8 (January 2020), 28 pages. Open access.

This article presents the formalization of the metatheory, typechecker and erasure that are part of the MetaCoq package.

Abstract
--------

Coq is built around a well-delimited kernel that perfoms typechecking for definitions in a variant of the Calculus of
Inductive Constructions (CIC). Although the metatheory of CIC is very stable and reliable, the correctness of its
implementation in Coq is less clear. Indeed, implementing an efficient type checker for CIC is a rather complex task,
and many parts of the code rely on implicit invariants which can easily be broken by further evolution of the code.
Therefore, on average, one critical bug has been found every year in Coq. This paper presents the first implementation
of a type checker for the kernel of Coq (without the module system and template polymorphism), which is proven correct
in Coq with respect to its formal specification and axiomatisation of part of its metatheory. Note that because of
Gödel’s incompleteness theorem, there is no hope to prove completely the correctness of the specification of Coq inside
Coq (in particular strong normalisation or canonicity), but it is possible to prove the correctness of the
implementation assuming the correctness of the specification, thus moving from a trusted code base (TCB) to a trusted
theory base (TTB) paradigm. Our work is based on the MetaCoq project which provides metaprogramming facilities to work
with terms and declarations at the level of this kernel. Our type checker is based on the specification of the typing
relation of the Polymorphic, Cumulative Calculus of Inductive Constructions (PCUIC) at the basis of Coq and the
verification of a relatively efficient and sound type-checker for it. In addition to the kernel implementation, an
essential feature of Coq is the so-called extraction: the production of executable code in functional languages from Coq
definitions. We present a verified version of this subtle type-and-proof erasure step, therefore enabling the verified
extraction of a safe type-checker for Coq.

Sources [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3544373.svg)](https://doi.org/10.5281/zenodo.3544373)
-------

The associated [release](https://zenodo.org/record/3544373/files/MetaCoq/metacoq-CoqCoqCorrect.zip?download=1)
contains the sources of the formalization. The general [documentation] of the MetaCoq project
also applies to this version.

[documentation]: https://metacoq.github.io/#documentation
