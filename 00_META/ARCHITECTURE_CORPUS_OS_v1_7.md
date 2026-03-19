# ARCHITECTURE DU CORPUS OS
Version 1.7 -- 2026-03-19
Auteur : Claude Sonnet 4.6
Statut : v1.7 -- a valider Pilote

Modification v1.6 -> v1.7 :
- CSU_v3_0.md incorpore en coexistence avec CSU_v2_0.md
- v2.0 : cadre abstrait (formes generiques A, B, U, V) -- reference JONCTION et TUS
- v3.0 : instanciation explicite (constantes c, g, alpha, m) -- version finale
- Total corpus : 29 fichiers (28 + 1)

---

## 0. PRINCIPE D ORGANISATION

Le corpus OS contient 29 documents de natures radicalement differentes :
theories formelles, cadre methodologique, documents fondateurs de programme,
enregistrements operationnels par phase, kernel cognitif agent, specifications
de composantes, et documents en attente de placement definitif.

L architecture repose sur six couches ordonnees.

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
|-- 06_ANNEXES/
```

---

## 2. DESCRIPTION DES COUCHES

### 00_META -- Invariants du corpus

```
00_META/
|-- CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
|-- ORI_C_Pancarte_Normative_v1_0.md
|-- ARCHITECTURE_CORPUS_OS_v1_7.md              (ce document)
```

---

### 01_THEORIE -- Fondements formels

```
01_THEORIE/
|
|-- RSU/
|   |-- RSU_Equation_Fondamentale_Advenance_v1_0.md
|       (Moise DANIEL -- categorie B)
|
|-- CSU/
|   |-- CSU_v2_0.md
|   |   (Moise DANIEL -- DOI 10.5281/zenodo.19104100 -- categorie A)
|   |   Role : cadre abstrait -- reference par JONCTION v1.1 et TUS v4.4
|   |-- CSU_v3_0.md
|       (Moise DANIEL -- Version finale -- categorie A)
|       Role : instanciation explicite (c, g, alpha, m)
|       Relation : v3.0 instancie v2.0 -- coexistence, pas de remplacement
|
|-- JONCTION/
|   |-- RSU_phi_CSU_Jonction_v1_1.md
|       (revision CSU v2.0 -- 2026-03-19 -- valide Pilote -- categorie A)
|       Appui : objets abstraits CSU v2.0 (A, B, L_CSU, U) -- toujours valides
|
|-- CST/
|   |-- CST_Minimal_Axiomatic_Core_v1_0.md
|       (Smain BEDROUNI -- categorie B)
|
|-- DELTA_S/
|   |-- Structure_fondamentale_delta_s_v2_1.md
|       (categorie B)
|
|-- TUS/
    |-- TUS_v4_2_COMPLETE.md
    |   (categorie A -- conserver)
    |-- TUS_v4_4.md
        (mise a jour CSU v2.0 -- 2026-03-19 -- valide Pilote -- categorie A)
        Appui : objets abstraits CSU v2.0 -- toujours valides
```

Note sur CSU : v2.0 et v3.0 sont deux niveaux du meme cadre.
v2.0 est le niveau architectural (formes generiques).
v3.0 est le niveau modele (constantes physiques explicites).
JONCTION et TUS s appuient sur v2.0 -- aucune revision requise.

---

### 02_METHODE -- Cadre methodologique

```
02_METHODE/
|-- Dialogyk_v2_2_condense.md
    (Benedict DEVAUD -- categorie B)
```

---

### 03_PROGRAMME -- Documents fondateurs et enregistrements OS

```
03_PROGRAMME/
|-- DOCUMENT_ZERO_v1_0.md
|-- OS_Document_Fondateur_v1_0.md
|-- PREREG_OS_v1_6.md
|-- PREREG_OS_Amendement_v1_2.md
|-- PREREG_OS_Phase2_v1_0.md
|-- PREREG_OS_Phase3_v1_0.md
|-- PREREG_OS_Technique_v1_0.md
|-- JONCTION_Bilaterale_OS_v0_9.md
```

---

### 04_PHASES -- Trace operationnelle par phase

```
04_PHASES/
|
|-- Phase_1/
|   |-- MEMOIRE_FRACTALE_Phase1_v1_13.md
|   |-- RAPPORT_CLOTURE_Phase1.md
|
|-- Phase_2/
|   |-- MEMOIRE_FRACTALE_Phase2_v1_14.md
|   |-- RAPPORT_CLOTURE_Phase2.md
|
|-- Phase_3/
    |-- MEMOIRE_FRACTALE_Phase3_v1_8.md
    |-- RAPPORT_CLOTURE_Phase3.md
```

---

### 05_KERNEL -- Kernel cognitif agent

```
05_KERNEL/
|-- J5_Kernel_Champ_Cognitif_v1_6.md
|-- AXIS_Claude_Sonnet_4_6_v2_0.md
```

---

### 06_ANNEXES -- Documents satellites et en attente

```
06_ANNEXES/
|
|-- ACTIF/
|   (vide)
|
|-- ATTENTE/
    |-- DABO_Candidat_Conductor_v1_0.md
        Statut : en attente de qualification et de placement definitif
```

---

## 3. VUE COMPLETE DU CORPUS

```
OS_CORPUS/
|
|-- 00_META/                                    (3 fichiers)
|   |-- CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
|   |-- ORI_C_Pancarte_Normative_v1_0.md
|   |-- ARCHITECTURE_CORPUS_OS_v1_7.md
|
|-- 01_THEORIE/                                 (8 fichiers)
|   |-- RSU/
|   |   |-- RSU_Equation_Fondamentale_Advenance_v1_0.md
|   |-- CSU/
|   |   |-- CSU_v2_0.md                        [cadre abstrait]
|   |   |-- CSU_v3_0.md                        [instanciation explicite]
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
|   |-- J5_Kernel_Champ_Cognitif_v1_6.md
|   |-- AXIS_Claude_Sonnet_4_6_v2_0.md
|
|-- 06_ANNEXES/                                 (1 fichier)
    |-- ATTENTE/
        |-- DABO_Candidat_Conductor_v1_0.md
```

Total : 29 fichiers

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

06_ANNEXES : satellite -- pas de dependance operationnelle
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

**Document present mais non encore qualifie ?**
-> 06_ANNEXES/ATTENTE jusqu a decision Pilote

---

## 6. ETAT DES TRAVAUX

```
Chantiers fermes (session 2026-03-19)
  01_THEORIE/CSU/CSU_v2_0.md                        -- incorpore, valide
  01_THEORIE/CSU/CSU_v3_0.md                        -- incorpore, valide
  01_THEORIE/JONCTION/RSU_phi_CSU_Jonction_v1_1.md  -- incorpore, valide
  01_THEORIE/TUS/TUS_v4_4.md                        -- incorpore, valide
  06_ANNEXES/ATTENTE/DABO_Candidat_Conductor_v1_0.md -- classe, en attente qualification

Archive (hors corpus actif)
  CSU_Coherence_Structurelle_Universelle_v1_0.md
  RSU_phi_CSU_Jonction_v1_0.md
  TUS_v4_3.md

Sans intervention requise
  01_THEORIE/TUS/TUS_v4_2_COMPLETE.md
  03_PROGRAMME/OS_Document_Fondateur_v1_0.md
  04_PHASES/* (categories A)
  05_KERNEL/AXIS_Claude_Sonnet_4_6_v2_0.md
```

---

*Architecture v1.7 -- coexistence CSU v2.0 / v3.0 -- 2026-03-19*
*Toute modification fait l objet d un increment de version*
*Conforme a CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md*
