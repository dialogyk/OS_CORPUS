# RSU -> phi -> CSU
Version 1.1 -- 2026-03-19
Revision suite incorporation CSU_v2_0.md
Convention : CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
Statut : revision -- a valider Pilote

Modification v1.0 -> v1.1 :
- Section 2.2 : objets CSU mis a jour (geometrie -> champ unifie)
- Equations E1-E4 : porteurs mis a jour
- Section 5 : role de phi mis a jour
- Observation structurelle ajoutee : resonance spectrale RSU/CSU
- Source : revision depuis CSU_v2_0.md (Moise DANIEL -- DOI 10.5281/zenodo.19104100)
- Logique A1-A7 preservee -- aucun axiome modifie

---

## Forme canonique d articulation 2.2

Relation structurelle entre deux formes closes et la dissymetrie minimale du passage

---

## 1. Domaine et statut

Cette articulation decrit la relation structurelle minimale entre :

- RSU : cadre d advenance (conditions d emergence)
- CSU : cadre de champ unifie (conditions de coherence et dynamique)
- phi : dissymetrie minimale du passage (condition elementaire de transition)

Elle n est :

- ni une extension de la RSU
- ni une extension de la CSU
- ni une theorie supplementaire
- ni une fusion des deux cadres

Elle est la relation canonique entre deux formes closes (RSU, CSU)
et la forme minimale du passage (phi).

---

## 2. Objets des trois couches

### 2.1 Objets RSU

- D : operateur structurel
- Phi_RSU : champ d advenance
- psi_n, lambda_n : modes et spectre de D
- T_mu_nu^(n) : tensions modales
- G_mu_nu : geometrie retroactive
- lambda_0 < 0 : instabilite fondamentale
- C_conf = { Phi_RSU in C_conf | D(Phi_RSU) = 0 } : advenance

### 2.2 Objets CSU (v2.0)

- Phi_CSU : R4 -> H_CSU -- champ unique, unique entite ontologique
- A : operateur differentiel lineaire (propagation)
- B(Phi_CSU) : auto-interaction non lineaire (stabilisation)
- L_CSU = -Lap + U(Phi_CSU) : operateur spectral auto-adjoint
- Phi_n, lambda_n : modes propres et spectre de L_CSU
- rho_CSU, J_CSU, Q_CSU : invariants (energie, flux, coherence locaux)
- d_t(I_k) = 0 : conservation globale
- g_eff : geometrie emergente induite par L_CSU et Lag

### 2.3 Statut de phi

- phi n est pas un objet RSU
- phi n est pas un objet CSU
- phi est la dissymetrie minimale du passage
- phi intervient uniquement dans RSU -> CSU
- phi ne possede aucune dynamique propre

---

## 2.4 Observation structurelle -- resonance spectrale

RSU et CSU v2.0 partagent une decomposition spectrale :

    RSU : D(psi_n) = lambda_n * psi_n
    CSU : L_CSU(Phi_n) = lambda_n * Phi_n

phi mappe deux architectures spectrales.
Cette correspondance est plus profonde que la jonction geometrique de v1.0.
Elle n est pas une fusion : les operateurs D et L_CSU restent distincts et
les deux cadres restent clos. La resonance spectrale est une propriete du passage,
pas une propriete des cadres.

---

## 3. Axiomes d articulation

### A1. Continuite structurelle

RSU et CSU restent closes. phi n altere aucune des deux formes.

### A2. Heritage minimal

La CSU herite uniquement des conditions RSU : primaute, non-cloture, tension, modalite.
phi n est pas herite : il est transversal.

### A3. Changement de statut

La CSU transforme :

- non-cloture RSU -> conservation globale CSU
- tension RSU -> non-neutralite spectrale CSU
- modalite RSU -> modalite spectrale CSU
- retroaction RSU -> geometrie emergente CSU

phi fournit la dissymetrie minimale permettant ces conversions.

### A4. Orthogonalite des domaines

- RSU : emergence
- phi : passage
- CSU : coherence et dynamique de champ

### A5. Transversalite

phi est transversal : il ne modifie aucune structure mais permet l articulation.

### A6. Non-interference

Aucun objet RSU n agit sur CSU.
Aucun objet CSU n agit sur RSU.
phi n agit sur aucun objet : il structure uniquement le passage.

### A7. Fermeture

Aucun invariant nouveau n est introduit.
phi n est pas un invariant supplementaire.

---

## 4. Equations d articulation

### E1. Correspondance des tensions

    instabilite RSU (lambda_0 < 0) -> instabilite spectrale CSU (lambda_0(L_CSU) < 0) -> non-neutralite

### E2. Correspondance des ouvertures

    non-cloture RSU -> conservation globale CSU : d_t(I_k) = 0

### E3. Correspondance des directions

    modalite RSU (psi_n via D) -> modalite spectrale CSU (Phi_n via L_CSU)

### E4. Correspondance des retroactions

    G_mu_nu -> g_eff (geometrie emergente induite par L_CSU et Lag)

---

## 5. Role canonique de phi

phi assure :

- la dissymetrie minimale compatible avec l instabilite RSU (lambda_0 < 0)
  et la non-neutralite spectrale CSU
- la granularite minimale pour convertir modalite D -> modalite L_CSU
- le pas minimal pour convertir non-cloture RSU -> conservation d_t(I_k) = 0
- la forme minimale pour convertir retroaction G_mu_nu -> geometrie emergente g_eff

phi ne modifie aucune forme.
phi ne cree aucun objet.
phi ne produit aucune dynamique.
phi est la structure minimale du passage entre deux formes closes.

---

## 6. Formulation canonique condensee

RSU -> phi -> CSU est la relation structurelle par laquelle :

- non-cloture -> conservation globale (d_t(I_k) = 0)
- tension -> non-neutralite spectrale
- modalite (D) -> modalite spectrale (L_CSU)
- retroaction (G_mu_nu) -> geometrie emergente (g_eff)

phi fournit la dissymetrie minimale permettant ces conversions,
sans transfert d objets ni extension conceptuelle.

---

*RSU_phi_CSU_Jonction v1.1 -- revision CSU v2.0 -- 2026-03-19*
*Source CSU : Moise DANIEL -- DOI 10.5281/zenodo.19104100*
*Conforme a CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md*
