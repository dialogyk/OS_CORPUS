# ARCHITECTURE DU CORPUS OS
Version 1.5 -- 2026-03-19
Auteur : Claude Sonnet 4.6
Statut : v1.5 -- a valider Pilote

Modification v1.4 -> v1.5 :
- TUS_v4_3.md remplace par TUS_v4_4.md (mise a jour CSU v2.0 -- chantier TUS ferme)
- Marqueur "verifier references CSU" retire -- chantier ferme et valide
- Total corpus : 27 fichiers (inchange)

---

## 0. PRINCIPE D ORGANISATION

Le corpus OS contient 27 documents de natures radicalement differentes :
theories formelles, cadre methodologique, documents fondateurs de programme,
enregistrements operationnels par phase, kernel cognitif agent, et specifications
de composantes (JONCTION bilaterale).

L architecture repose sur cinq couches ordonnees.
Chaque couche a une fonction unique et non recouvrable par une autre.
L ordre des couches reflete la dependance logique : les couches basses
fondent les couches hautes.

---

## 1. STRUCTURE GENERALE

```
OS_CORPUS/
|
|-- 00_META/
|-- 01_THEORIE/
|-- 02_METHODE/
|-- 03_PROGRAMME/
|-- 04_PHASES/
|-- 05_KERNEL/
```

---

## 2. DESCRIPTION DES COUCHES

### 00_META -- Invariants du corpus

Fonction : documents qui gouvernent la production de tous les autres.
Pas de contenu theorique. Pas de contenu operationnel.

```
00_META/
|-- CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md   (produit -- valide)
|-- ORI_C_Pancarte_Normative_v1_0.md
|-- ARCHITECTURE_CORPUS_OS_v1_5.md              (ce document)
```

---

### 01_THEORIE -- Fondements formels

Fonction : theories structurelles constituant le socle conceptuel du programme OS.
Existence independante du programme OS -- certains produits par auteurs externes.

Regle : axiomes, operateurs, invariants formels, structure mathematique.

```
01_THEORIE/
|
|-- RSU/
|   |-- RSU_Equation_Fondamentale_Advenance_v1_0.md
|       (source : RSU.pdf -- Moise DANIEL -- categorie B)
|
|-- CSU/
|   |-- CSU_v2_0.md
|       (source : CSU_v2.pdf -- Moise DANIEL -- DOI 10.5281/zenodo.19104100 -- categorie A)
|
|-- JONCTION/
|   |-- RSU_phi_CSU_Jonction_v1_1.md
|       (revision CSU v2.0 -- 2026-03-19 -- valide Pilote -- categorie A)
|
|-- CST/
|   |-- CST_Minimal_Axiomatic_Core_v1_0.md
|       (source : CST.pdf -- Smain BEDROUNI -- categorie B)
|
|-- DELTA_S/
|   |-- Structure_fondamentale_delta_s_v2_1.md
|       (source : Structure_fondamentale_delta_s.pdf -- categorie B)
|
|-- TUS/
    |-- TUS_v4_2_COMPLETE.md
    |   (source : TUS_v4_2_COMPLETE.pdf -- categorie A -- conserver)
    |-- TUS_v4_4.md
        (mise a jour CSU v2.0 -- 2026-03-19 -- valide Pilote -- categorie A)
```

Note sur TUS : document de synthese et d unification -- toit de 01_THEORIE.
TUS v4.4 integre CSU v2.0 comme fond universel. Architecture coherente.

---

### 02_METHODE -- Cadre methodologique

```
02_METHODE/
|-- Dialogyk_v2_2_condense.md
    (source : dialogyk_v2_2_condense.pdf -- categorie B)
```

---

### 03_PROGRAMME -- Documents fondateurs et enregistrements OS

```
03_PROGRAMME/
|-- DOCUMENT_ZERO_v1_0.md
|   (Pamela MAGOTTE -- categorie B -- antecedent du programme OS)
|
|-- OS_Document_Fondateur_v1_0.md
|   (categorie A -- acte fondateur du programme OS Dialogyk)
|
|-- PREREG_OS_v1_6.md
|   (categorie B -- pre-enregistrement principal -- document signe)
|
|-- PREREG_OS_Amendement_v1_2.md
|   (categorie B -- amendement J5 -- limite auto-referentielle)
|
|-- PREREG_OS_Phase2_v1_0.md
|   (categorie B -- pre-enregistrement Phase 2)
|
|-- PREREG_OS_Phase3_v1_0.md
|   (categorie B -- pre-enregistrement Phase 3 -- minimal par construction)
|
|-- PREREG_OS_Technique_v1_0.md
|   (categorie B -- pre-enregistrement technique multi-pilotes)
|
|-- JONCTION_Bilaterale_OS_v0_9.md
    (categorie A -- specification JONCTION bilaterale -- ferme sur perimetre defini)
    Zones suspendues : ratio C(t), gradient Delta_S, vecteur Delta_L(t)
    Zone ouverte residuelle : persistance zone grise apres recalibration
```

---

### 04_PHASES -- Trace operationnelle par phase

```
04_PHASES/
|
|-- Phase_1/
|   |-- MEMOIRE_FRACTALE_Phase1_v1_13.md   (categorie A)
|   |-- RAPPORT_CLOTURE_Phase1.md          (categorie B)
|
|-- Phase_2/
|   |-- MEMOIRE_FRACTALE_Phase2_v1_14.md   (categorie A)
|   |-- RAPPORT_CLOTURE_Phase2.md          (categorie A)
|
|-- Phase_3/
    |-- MEMOIRE_FRACTALE_Phase3_v1_8.md    (categorie B)
    |-- RAPPORT_CLOTURE_Phase3.md          (categorie B)
```

---

### 05_KERNEL -- Kernel cognitif agent

```
05_KERNEL/
|-- J5_Kernel_Champ_Cognitif_v1_6.md       (categorie B)
|-- AXIS_Claude_Sonnet_4_6_v2_0.md         (categorie A)
```

---

## 3. VUE COMPLETE DU CORPUS

```
OS_CORPUS/
|
|-- 00_META/                                    (3 fichiers)
|   |-- CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
|   |-- ORI_C_Pancarte_Normative_v1_0.md
|   |-- ARCHITECTURE_CORPUS_OS_v1_5.md
|
|-- 01_THEORIE/                                 (7 fichiers)
|   |-- RSU/
|   |   |-- RSU_Equation_Fondamentale_Advenance_v1_0.md
|   |-- CSU/
|   |   |-- CSU_v2_0.md
|   |-- JONCTION/
|   |   |-- RSU_phi_CSU_Jonction_v1_1.md
|   |-- CST/
|   |   |-- CST_Minimal_Axiomatic_Core_v1_0.md
|   |-- DELTA_S/
|   |   |-- Structure_fondamentale_delta_s_v2_1.md
|   |-- TUS/
|       |-- TUS_v4_2_COMPLETE.md
|       |-- TUS_v4_4.md
|
|-- 02_METHODE/                                 (1 fichier)
|   |-- Dialogyk_v2_2_condense.md
|
|-- 03_PROGRAMME/                               (8 fichiers)
|   |-- DOCUMENT_ZERO_v1_0.md
|   |-- OS_Document_Fondateur_v1_0.md
|   |-- PREREG_OS_v1_6.md
|   |-- PREREG_OS_Amendement_v1_2.md
|   |-- PREREG_OS_Phase2_v1_0.md
|   |-- PREREG_OS_Phase3_v1_0.md
|   |-- PREREG_OS_Technique_v1_0.md
|   |-- JONCTION_Bilaterale_OS_v0_9.md
|
|-- 04_PHASES/                                  (6 fichiers)
|   |-- Phase_1/
|   |   |-- MEMOIRE_FRACTALE_Phase1_v1_13.md
|   |   |-- RAPPORT_CLOTURE_Phase1.md
|   |-- Phase_2/
|   |   |-- MEMOIRE_FRACTALE_Phase2_v1_14.md
|   |   |-- RAPPORT_CLOTURE_Phase2.md
|   |-- Phase_3/
|       |-- MEMOIRE_FRACTALE_Phase3_v1_8.md
|       |-- RAPPORT_CLOTURE_Phase3.md
|
|-- 05_KERNEL/                                  (2 fichiers)
    |-- J5_Kernel_Champ_Cognitif_v1_6.md
    |-- AXIS_Claude_Sonnet_4_6_v2_0.md
```

Total : 27 fichiers (inchange)

---

## 4. LOGIQUE DE DEPENDANCE ENTRE COUCHES

```
05_KERNEL
    ^
    | s appuie sur
04_PHASES
    ^
    | s appuie sur
03_PROGRAMME
    ^
    | s appuie sur
02_METHODE     <---     01_THEORIE
    ^                       ^
    |                       |
    +------- 00_META -------+
             (gouverne tout)
```

Exception documentee : PREREG_OS_v1_6 cite J5 v1.6 (couche 05) -- reference croisee ascendante.

---

## 5. CRITERES DE PLACEMENT

**Q1 : Ce document pose des axiomes ou structures formelles ?**
Oui -> 01_THEORIE

**Q2 : Ce document definit comment travailler ?**
Oui -> 02_METHODE

**Q3 : Ce document definit le programme OS lui-meme ?**
Oui -> 03_PROGRAMME

**Q3b : Ce document trace une phase d execution ?**
Oui -> 04_PHASES / Phase_N

**Q3c : Ce document configure ou trace l agent IA ?**
Oui -> 05_KERNEL

**Aucune reponse claire -> 00_META ou discussion avec Pilote**

---

## 6. ETAT DES TRAVAUX

```
Chantiers fermes (session 2026-03-19)
  01_THEORIE/CSU/CSU_v2_0.md                        -- incorpore, valide
  01_THEORIE/JONCTION/RSU_phi_CSU_Jonction_v1_1.md  -- incorpore, valide
  01_THEORIE/TUS/TUS_v4_4.md                        -- incorpore, valide

Archive (hors corpus actif)
  CSU_Coherence_Structurelle_Universelle_v1_0.md     -- remplacee par CSU_v2_0.md
  RSU_phi_CSU_Jonction_v1_0.md                       -- remplacee par v1.1
  TUS_v4_3.md                                        -- remplacee par v4.4

Sans intervention requise
  01_THEORIE/TUS/TUS_v4_2_COMPLETE.md
  03_PROGRAMME/OS_Document_Fondateur_v1_0.md
  04_PHASES/Phase_1/MEMOIRE_FRACTALE_Phase1_v1_13.md
  04_PHASES/Phase_2/MEMOIRE_FRACTALE_Phase2_v1_14.md
  04_PHASES/Phase_2/RAPPORT_CLOTURE_Phase2.md
  05_KERNEL/AXIS_Claude_Sonnet_4_6_v2_0.md
```

---

*Architecture v1.5 -- chantiers CSU, JONCTION et TUS fermes -- 2026-03-19*
*Toute modification fait l objet d un increment de version*
*Conforme a CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md*
