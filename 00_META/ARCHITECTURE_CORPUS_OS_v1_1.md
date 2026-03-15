# ARCHITECTURE DU CORPUS OS
Version 1.1 -- 2026-03-15
Auteur : Claude Sonnet 4.6
Statut : v1.1 -- valide Copilot et Pilote

Modification v1.0 -> v1.1 :
- 01_THEORIE/PHI/ renomme en 01_THEORIE/JONCTION/ (elimination collision visuelle avec phi_TUS)

---

## 0. PRINCIPE D ORGANISATION

Le corpus OS contient 22 documents de natures radicalement differentes :
theories formelles, cadre methodologique, documents fondateurs de programme,
enregistrements operationnels par phase, et kernel cognitif agent.

Les placer dans un meme dossier plat sans hierarchie produit trois problemes :
- impossibilite de naviguer sans connaitre l ensemble du corpus par coeur
- references croisees non traçables (quel document cite quel autre ?)
- reconstruction impossible sans savoir ou placer chaque fichier reconstruit

L architecture proposee repose sur cinq couches ordonnees.
Chaque couche a une fonction unique et non recouvrable par une autre.
L ordre des couches reflete la dependance logique : les couches basses
fondent les couches hautes. On ne peut pas lire une couche haute
sans s appuyer sur les couches inferieures.

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

Six dossiers. Prefixes numeriques pour forcer l ordre de lecture naturel.

---

## 2. DESCRIPTION DES COUCHES

### 00_META -- Invariants du corpus

Fonction : contient les documents qui gouvernent la production de tous les autres.
Pas de contenu theorique. Pas de contenu operationnel.
Uniquement ce qui s applique a l ensemble du corpus.

Regle : tout document qui definit comment ecrire les autres va ici.

```
00_META/
|-- CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md   (produit -- valide)
|-- ORI_C_Pancarte_Normative_v1_0.md            (deja present en .md)
|-- ARCHITECTURE_CORPUS_OS_v1_0.md              (ce document)
```

---

### 01_THEORIE -- Fondements formels

Fonction : contient les theories structurelles qui constituent le socle
conceptuel du programme OS. Ces documents ont une existence independante
du programme OS -- certains sont produits par des auteurs externes.

Regle : un document va ici s il pose des axiomes, des operateurs,
des invariants formels, ou une structure mathematique.
Il ne decrit pas le programme OS -- il fonde la theorie sur laquelle OS s appuie.

Sous-structure par cadre theorique :

```
01_THEORIE/
|
|-- RSU/
|   |-- RSU_Equation_Fondamentale_Advenance_v1_0.md
|       (source : RSU.pdf -- Moise DANIEL -- categorie B)
|
|-- CSU/
|   |-- CSU_Coherence_Structurelle_Universelle_v1_0.md
|       (source : CSU.pdf -- categorie C -- a reecrire)
|
|-- JONCTION/
|   |-- RSU_phi_CSU_Jonction_v1_0.md
|       (source : RSU_phi_CSU.pdf -- categorie C -- a reecrire entierement)
|
|-- CST/
|   |-- CST_Minimal_Axiomatic_Core_v1_0.md
|       (source : CST.pdf -- Smaïn Bedrouni -- categorie B)
|
|-- DELTA_S/
|   |-- Structure_fondamentale_delta_s_v1_0.md
|       (source : Structure_fondamentale_delta_s.pdf -- categorie B)
|
|-- TUS/
    |-- TUS_v4_2_COMPLETE.md
    |   (source : TUS_v4_2_COMPLETE.pdf -- categorie A -- conserver)
    |-- TUS_v4_3.md
        (source : TUS_v4_3.pdf -- categorie B -- reconstruire)
```

Note sur TUS : TUS est un document de synthese et d unification
qui integre RSU, CSU, CST, Delta_S dans un cadre commun.
Il appartient a THEORIE car il pose une structure formelle --
mais il est hierarchiquement superieur aux autres dans cette couche.
TUS est le toit de 01_THEORIE.

Note sur JONCTION : RSU_phi_CSU est le document de jonction entre RSU et CSU.
Il a une existence propre -- ni RSU pur, ni CSU pur.
Il justifie un sous-dossier dedie.

---

### 02_METHODE -- Cadre methodologique

Fonction : contient le cadre qui gouverne la dynamique de dialogue,
de calibration et d iteration du programme OS.
Dialogyk n est pas une theorie formelle -- c est une methode operatoire.
Il n est pas non plus un document du programme OS -- il precede OS et le structure.

Regle : un document va ici s il definit comment travailler,
pas ce sur quoi on travaille.

```
02_METHODE/
|-- Dialogyk_v2_2_condense.md
    (source : dialogyk_v2_2_condense.pdf -- categorie B)
```

---

### 03_PROGRAMME -- Documents fondateurs et enregistrements OS

Fonction : contient les documents qui definissent, enregistrent
et structurent le programme OS en tant que programme de recherche.
Ce sont les actes fondateurs et les pre-enregistrements.

Regle : un document va ici s il definit le programme OS lui-meme --
son objet, ses hypotheses, ses conditions, son dispositif.
Il ne decrit pas une phase -- il pose le cadre global.

```
03_PROGRAMME/
|-- DOCUMENT_ZERO_v1_0.md
|   (source : DOCUMENT_ZERO.pdf -- Pamela Magotte -- categorie B)
|   Statut : document fondateur externe -- antecedent du programme OS
|
|-- OS_Document_Fondateur_v1_0.md
|   (source : OS_Document_Fondateur_v1_0.pdf -- categorie A)
|   Statut : acte fondateur du programme OS Dialogyk
|
|-- PREREG_OS_v1_6.md
|   (source : PREREG_OS_v1_6.pdf -- categorie B)
|   Statut : pre-enregistrement principal -- document signe
|
|-- PREREG_OS_Amendement_v1_2.md
|   (source : PREREG_OS_Amendement_v1_2.pdf -- categorie B)
|   Statut : amendement J5 -- limite auto-referentielle
|
|-- PREREG_OS_Phase2_v1_0.md
|   (source : PREREG_OS_Phase2_v1_0.pdf -- categorie B)
|   Statut : pre-enregistrement Phase 2
|
|-- PREREG_OS_Technique_v1_0.md
    (source : PREREG_OS_Technique_v1_0.pdf -- categorie B)
    Statut : pre-enregistrement technique multi-pilotes
```

Note sur DOCUMENT_ZERO : produit par Pamela Magotte en janvier 2026.
C est un document fondateur externe qui precede et motive le programme OS.
Il appartient a PROGRAMME comme antecedent, pas a THEORIE.

---

### 04_PHASES -- Trace operationnelle par phase

Fonction : contient les documents produits au cours de chaque phase
d execution du programme OS. Ce sont les traces de travail --
memoires et rapports de cloture.

Regle : un document va ici s il est produit pendant une phase
et documente son deroulement, ses resultats, ses invariants emergents.

```
04_PHASES/
|
|-- Phase_1/
|   |-- MEMOIRE_FRACTALE_Phase1_v1_13.md
|   |   (source : MEMOIRE_FRACTALE_Phase1_v1_13.pdf -- categorie A)
|   |-- RAPPORT_CLOTURE_Phase1.md
|       (source : RAPPORT_CLOTURE_Phase1.pdf -- categorie B)
|
|-- Phase_2/
|   |-- MEMOIRE_FRACTALE_Phase2_v1_14.md
|   |   (source : MEMOIRE_FRACTALE_Phase2_v1_14.pdf -- categorie A)
|   |-- RAPPORT_CLOTURE_Phase2.md
|       (source : RAPPORT_CLOTURE_Phase2.pdf -- categorie A)
|
|-- Phase_3/
    |-- MEMOIRE_FRACTALE_Phase3_v1_8.md
    |   (source : MEMOIRE_FRACTALE_Phase3_v1_8.pdf -- categorie B)
    |-- RAPPORT_CLOTURE_Phase3.md
        (source : RAPPORT_CLOTURE_Phase3.pdf -- categorie B)
```

Note : la paire MEMOIRE_FRACTALE + RAPPORT_CLOTURE est l unite atomique
de chaque phase. Ces deux documents sont toujours produits ensemble
et se referent mutuellement. L architecture les place cote a cote
dans le meme sous-dossier de phase.

---

### 05_KERNEL -- Kernel cognitif agent

Fonction : contient les documents qui definissent et tracent
le kernel cognitif de l agent IA (Claude Sonnet 4.6) dans le programme OS.
Ce sont les profils, les axiomes cognitifs, et la memoire operatoire de l agent.

Regle : un document va ici s il decrit ou configure l agent IA --
son architecture cognitive, ses invariants, son mode operatoire.
Ce ne sont pas des theories. Ce ne sont pas des rapports de phase.
Ce sont des specifications d agent.

```
05_KERNEL/
|-- J5_Kernel_Champ_Cognitif_v1_6.md
|   (source : J5_Kernel_Champ_Cognitif_v1_6.pdf -- categorie B)
|   Statut : architecture operatoire du kernel cognitif
|
|-- AXIS_Claude_Sonnet_4_6_v2_0.md
    (source : AXIS_Claude_Sonnet_4_6_v2_0.pdf -- categorie A)
    Statut : profil cognitif agent -- post Phase 3
```

---

## 3. VUE COMPLETE DU CORPUS REORGANISE

```
OS_CORPUS/
|
|-- 00_META/                                    (3 fichiers)
|   |-- CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
|   |-- ORI_C_Pancarte_Normative_v1_0.md
|   |-- ARCHITECTURE_CORPUS_OS_v1_0.md
|
|-- 01_THEORIE/                                 (7 fichiers)
|   |-- RSU/
|   |   |-- RSU_Equation_Fondamentale_Advenance_v1_0.md
|   |-- CSU/
|   |   |-- CSU_Coherence_Structurelle_Universelle_v1_0.md
|   |-- JONCTION/
|   |   |-- RSU_phi_CSU_Jonction_v1_0.md
|   |-- CST/
|   |   |-- CST_Minimal_Axiomatic_Core_v1_0.md
|   |-- DELTA_S/
|   |   |-- Structure_fondamentale_delta_s_v1_0.md
|   |-- TUS/
|       |-- TUS_v4_2_COMPLETE.md
|       |-- TUS_v4_3.md
|
|-- 02_METHODE/                                 (1 fichier)
|   |-- Dialogyk_v2_2_condense.md
|
|-- 03_PROGRAMME/                               (6 fichiers)
|   |-- DOCUMENT_ZERO_v1_0.md
|   |-- OS_Document_Fondateur_v1_0.md
|   |-- PREREG_OS_v1_6.md
|   |-- PREREG_OS_Amendement_v1_2.md
|   |-- PREREG_OS_Phase2_v1_0.md
|   |-- PREREG_OS_Technique_v1_0.md
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

Total : 25 fichiers (22 sources + 3 META dont ce document)

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

Lecture : un document de la couche N peut citer des documents
des couches inferieures (N-1, N-2...).
Un document de la couche N ne devrait jamais dependre
d un document d une couche superieure.

Exception documentee : PREREG_OS_v1_6 cite J5 v1.6 (couche 05).
C est une reference croisee ascendante -- a noter comme exception
dans le document lui-meme.

---

## 5. CRITERES DE PLACEMENT -- QUESTIONS DE DECISION

Pour tout nouveau document OS, trois questions suffisent :

**Q1 : Est-ce que ce document pose des axiomes ou des structures formelles ?**
Oui -> 01_THEORIE
Non -> Q2

**Q2 : Est-ce que ce document definit comment travailler ?**
Oui -> 02_METHODE
Non -> Q3

**Q3 : Est-ce que ce document definit le programme OS lui-meme ?**
Oui -> 03_PROGRAMME

**Q3b : Est-ce que ce document trace une phase d execution ?**
Oui -> 04_PHASES / Phase_N

**Q3c : Est-ce que ce document configure ou trace l agent IA ?**
Oui -> 05_KERNEL

**Aucune reponse claire -> 00_META ou discussion avec Pilote**

---

## 6. PRIORITES DE RECONSTRUCTION PAR COUCHE

Ordre issu du diagnostic d integrite :

```
Priorite 1 -- CRITIQUE
  01_THEORIE/JONCTION/RSU_phi_CSU_Jonction_v1_0.md
  (zero texte -- reecrire depuis zero)

Priorite 2 -- HAUTE
  01_THEORIE/CSU/CSU_Coherence_Structurelle_Universelle_v1_0.md
  (equations detruites -- reecrire)

Priorite 3 -- MOYENNE
  01_THEORIE/RSU/RSU_Equation_Fondamentale_Advenance_v1_0.md
  01_THEORIE/TUS/TUS_v4_3.md
  01_THEORIE/CST/CST_Minimal_Axiomatic_Core_v1_0.md

Priorite 4 -- BASSE
  03_PROGRAMME/PREREG_OS_Technique_v1_0.md
  03_PROGRAMME/PREREG_OS_Phase2_v1_0.md
  Tous les fichiers categorie B restants

Sans intervention
  01_THEORIE/TUS/TUS_v4_2_COMPLETE.md
  03_PROGRAMME/OS_Document_Fondateur_v1_0.md
  04_PHASES/Phase_1/MEMOIRE_FRACTALE_Phase1_v1_13.md
  04_PHASES/Phase_2/MEMOIRE_FRACTALE_Phase2_v1_14.md
  04_PHASES/Phase_2/RAPPORT_CLOTURE_Phase2.md
  05_KERNEL/AXIS_Claude_Sonnet_4_6_v2_0.md
```

---

*Architecture v1.0 -- soumise a validation Copilot et Pilote*
*Toute modification fait l objet d un increment de version*
