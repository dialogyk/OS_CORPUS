# Minimal Axiomatic Core of Correlative Structure Theory (CST)
Spectral Accessibility, Correlative Invariance, and Intrinsic Order from Rank Loss

DOI: 10.5281/zenodo.18906871
Auteur : Smaïn Bedrouni
ORCID: 0009-0004-6388-3100
smainbedrouni@gmail.com
March 8, 2026

Version 1.0 -- 2026-03-15
Reconstruction ASCII-safe depuis source JPEG (7 STX, accents decomposes auteur)
Convention : CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
Statut : reconstruit -- a valider par Pilote

---

## Abstract

We present a minimal axiomatic formulation of Correlative Structure Theory (CST).
The framework isolates the structural principles underlying the theory in a
representation-independent form. Three ingredients suffice: invariance of correlative
equivalence classes under admissible physical transformations, spectral accessibility
measured by the rank of positive semi-definite operators, and the emergence of
intrinsic structural order under strict rank loss in hierarchical projections.
This note provides a compact formal reference for the core principles of CST.

**Keywords:** Correlative Structure Theory, spectral rank loss, positive semi-definite
operators, hierarchical projections, emergent order, informational structure

---

## 1. Introduction

Correlative Structure Theory (CST) proposes a structural perspective in which
correlations constitute the fundamental carriers of physical information. Instead of
starting from dynamical laws or spacetime primitives, the theory focuses on the
spectral structure of operators encoding correlations.

Several works introduced different aspects of this framework, including informational
unity, spectral rank loss, and the emergence of temporal ordering from informational
gradients. The goal of the present note is to isolate the minimal conceptual core of
CST in an axiomatic form.

---

## 2. Correlative operators

We work in a finite-dimensional real Hilbert space identified with R^n equipped with
the standard inner product.

A system is represented by a symmetric positive semi-definite operator:

    C_corr in R^(n x n),    C_corr = C_corr^T,    C_corr >= 0         (1)

The operator encodes the correlative structure of the system.

### 2.1 Accessible subspace

The accessible informational structure associated with C_corr is defined as:

    A(C_corr) = Ran(C_corr)                                            (2)

The dimension of this space is:

    dim A(C_corr) = rank(C_corr)                                       (3)

Thus the rank measures the number of independent spectral modes carrying accessible
structural information.

---

## 3. Correlative equivalence

**Definition (Correlative equivalence).**
Two operators C_corr and C_corr' are said to be correlative equivalent if they are
related by an admissible representation transformation preserving spectral structure:

    C_corr' = U * C_corr * U^T                                        (4)

where U is an orthogonal operator. We write:

    C_corr' ~ C_corr                                                   (5)

---

## 4. Minimal axiomatic core

We now state the minimal structural principles underlying CST.

### Principle 1 -- Correlative invariance

Admissible physical transformations act within the same correlative equivalence class:

    T(C_corr) ~ C_corr                                                 (6)

Different representations may exist but correspond to the same underlying correlative
structure.

### Principle 2 -- Spectral accessibility

The accessible informational structure of a system is determined by:

    A(C_corr) = Ran(C_corr),    dim A(C_corr) = rank(C_corr)          (7)

The rank therefore measures the dimension of accessible structural information.

### Principle 3 -- Correlative hierarchy

Hierarchical descriptions arise through admissible projections:

    C_corr_k+1 = Pi_k * C_corr_k * Pi_k^T                            (8)

This induces a nested sequence of accessible spaces:

    A(C_corr_0) supset= A(C_corr_1) supset= A(C_corr_2) supset= ...  (9)

which defines a spectral filtration of the accessible structure.

### Principle 4 -- Emergence of intrinsic order

An intrinsic structural order appears if and only if the spectral dimension decreases
strictly:

    rank(C_corr_k+1) < rank(C_corr_k)                                 (10)

The strict rank loss condition is representation-independent and depends only on the
spectral dimension of the operator.

### Principle 5 -- Transition amplitude

The hierarchical transition can be written:

    rank(C_corr_k+1) = rank(C_corr_k) - m,    m >= 1                 (11)

The parameter m represents the number of eliminated independent spectral directions.

---

## 5. Structural interpretation

The previous principles lead to a simple structural picture. Physical transformations
preserve correlative equivalence classes, while hierarchical projections reduce the
accessible spectral dimension. When such reductions occur strictly, an intrinsic
ordering between hierarchical levels emerges.

This ordering provides a structural basis for irreversible sequences and may be
interpreted as a foundation for emergent temporal ordering in the CST framework.

---

## 6. Conclusion

We have presented a minimal axiomatic core for Correlative Structure Theory.
The framework relies only on spectral structure, correlative invariance, and
hierarchical rank loss.

Despite its compact form, this structure captures the essential mechanism proposed
in CST: intrinsic structural order emerges when the dimension of accessible spectral
information decreases.

---

## References

1. S. Bedrouni (2026). A Spectral Rank-Loss Criterion for Intrinsic Structural Order
   in Hierarchical Correlative Structures. Zenodo. 10.5281/zenodo.18764782

2. S. Bedrouni (2025). Informational Gradient and Correlative Rank Loss as the
   Fundamental Mechanism for the Emergence of Time. Zenodo.
   10.5281/zenodo.18098441

3. S. Bedrouni (2026). Theorie des Fils d Information (TFI) -- Version 3 : Un cadre
   informationnel complet pour la matiere, le vivant et l emergence du temps. Zenodo.
   10.5281/zenodo.18371057

---

*Reconstruction v1.0 -- source : CST.pdf (3 pages JPEG, 7 STX, accents decomposes auteur)*
*Conforme a CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md*
