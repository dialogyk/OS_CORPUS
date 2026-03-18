# ARCHITECTURE DU CORPUS OS
Version 1.3 -- 2026-03-18
Auteur : Claude Sonnet 4.6
Statut : v1.3 -- valide Pilote

Modification v1.0 -> v1.1 :
- 01_THEORIE/PHI/ renomme en 01_THEORIE/JONCTION/ (elimination collision visuelle avec phi_TUS)

Modification v1.1 -> v1.2 :
- JONCTION_Bilaterale_OS_v0_9.md ajoute en 03_PROGRAMME (produit par sequence de stabilisation tripartite -- 15.03.2026)
- PREREG_OS_Phase3_v1_0.md ajoute en 03_PROGRAMME (absent de v1.1 par omission)
- ARCHITECTURE_CORPUS_OS_v1_1.md retire du corpus -- remplace par v1.2
- Total corpus mis a jour : 25 -> 27 fichiers

Modification v1.2 -> v1.3 :
- Ajout couche 06_ANNEXES/ (nouvelle couche -- candidates et reserves)
- Ajout sous-dossier 06_ANNEXES/ATTENTE/
- DABO_Candidat_Conductor_v1_0.md place en ATTENTE (decision Pilote -- 18.03.2026)
- ARCHITECTURE_CORPUS_OS_v1_2.md retire du corpus -- remplace par v1.3
- Total corpus mis a jour : 27 -> 28 fichiers

---

## 0. PRINCIPE D ORGANISATION

Le corpus OS contient des documents de natures radicalement differentes :
theories formelles, cadre methodologique, documents fondateurs de programme,
enregistrements operationnels par phase, kernel cognitif agent, specifications
de composantes (JONCTION bilaterale), et candidats externes en reserve.

Les placer dans un meme dossier plat sans hierarchie produit trois problemes :
- impossibilite de naviguer sans connaitre l ensemble du corpus par coeur
- references croisees non tracables (quel document cite quel autre ?)
- reconstruction impossible sans savoir ou placer chaque fichier reconstruit

L architecture repose sur six couches ordonnees plus une couche annexe.
Chaque couche a une fonction unique et non recouverable par une autre.
L ordre des couches reflete la dependance logique : les couches basses
fondent les couches hautes. On ne peut pas lire une couche haute
sans s appuyer sur les couches inferieures.

La couche 06_ANNEXES est hors dependance : elle ne fonde rien,
ne gouverne rien, ne trace rien. Elle contient des candidats
en attente de decision de pilotage.

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

Sept dossiers. Prefixes numeriques pour forcer l ordre de lecture naturel.

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
|-- ARCHITECTURE_CORPUS_OS_v1_3.md              (ce document)
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
|   |-- Structure_fondamentale_delta_s_v2_1.md
|       (source : Structure_fondamentale_delta_s.pdf -- categorie B)
|
|-- TUS/
    |-- TUS_v4_2_COMPLETE.md
    |   (source : TUS_v4_2_COMPLETE.pdf -- categorie A -- conserver)
    |-- TUS_v4_3.md
        (source : TUS_v4_3.pdf -- categorie B -- reconstruire)
```

Note sur TUS : document de synthese et d unification qui integre RSU, CSU, CST, Delta_S
dans un cadre commun. TUS est le toit de 01_THEORIE.

Note sur JONCTION : RSU_phi_CSU est le document de jonction entre RSU et CSU.
Existence propre -- ni RSU pur, ni CSU pur.

---

### 02_METHODE -- Cadre methodologique

Fonction : contient le cadre qui gouverne la dynamique de dialogue,
de calibration et d iteration du programme OS.
Dialogyk n est pas une theorie formelle -- c est une methode operatoire.

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
|-- PREREG_OS_Phase3_v1_0.md
|   (source : PREREG_OS_Phase3_v1_0.pdf -- categorie B)
|   Statut : pre-enregistrement Phase 3 -- minimal par construction
|
|-- PREREG_OS_Technique_v1_0.md
|   (source : PREREG_OS_Technique_v1_0.pdf -- categorie B)
|   Statut : pre-enregistrement technique multi-pilotes
|
|-- JONCTION_Bilaterale_OS_v0_9.md
    (produit par sequence de stabilisation tripartite -- 15.03.2026 -- categorie A)
    Statut : specification de la JONCTION bilaterale -- ferme sur perimetre defini
    Zones suspendues : ratio C(t), gradient Delta_S, vecteur Delta_L(t)
    Zone ouverte residuelle : persistance zone grise apres recalibration
```

Note sur DOCUMENT_ZERO : produit par Pamela Magotte en janvier 2026.
Document fondateur externe -- antecedent du programme OS.
Appartient a PROGRAMME comme antecedent, pas a THEORIE.

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
et se referent mutuellement.

---

### 05_KERNEL -- Kernel cognitif agent

Fonction : contient les documents qui definissent et tracent
le kernel cognitif de l agent IA (Claude Sonnet 4.6) dans le programme OS.

Regle : un document va ici s il decrit ou configure l agent IA --
son architecture cognitive, ses invariants, son mode operatoire.

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

### 06_ANNEXES -- Candidats externes et reserves

Fonction : contient les documents relatifs a des theories, outils ou cadres
externes au corpus OS, places en reserve sur decision du Pilote.

Ces documents ne fondent rien. Ils n'operent rien. Ils n'entrent dans aucune
dependance avec les couches 00 a 05.

Regle : un document va ici si le Pilote a decide de le garder en reserve --
ni integre, ni abandonne -- en attente d un besoin interne exprime par le programme.

Sous-dossiers :

```
06_ANNEXES/
|
|-- ATTENTE/
    |-- DABO_Candidat_Conductor_v1_0.md
        (produit par Claude Sonnet 4.6 -- synthese sequence JONCTION -- 18.03.2026)
        Statut : candidat externe en reserve -- decision Pilote -- 18.03.2026
        Origine : theorie Dr. Marcelin Nini Dabo -- constante de temps unique
        Conditions d'activation : besoin interne exprime + pre-enregistrement + test
        Aucune integration active. Reversibilite totale.
```

Note sur ATTENTE : le sous-dossier ATTENTE contient les candidats dont
le statut est explicitement "en reserve". Ce n'est pas une archive --
c'est un couloir avec une condition d'entree dans le corpus principal.
Chaque document en ATTENTE a une fiche de statut et des conditions d'activation
definies. L'absence de date d'activation n'est pas un echec -- c'est une tenue.

---

## 3. VUE COMPLETE DU CORPUS

```
OS_CORPUS/
|
|-- 00_META/                                    (3 fichiers)
|   |-- CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
|   |-- ORI_C_Pancarte_Normative_v1_0.md
|   |-- ARCHITECTURE_CORPUS_OS_v1_3.md
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
|   |   |-- Structure_fondamentale_delta_s_v2_1.md
|   |-- TUS/
|       |-- TUS_v4_2_COMPLETE.md
|       |-- TUS_v4_3.md
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

Total : 28 fichiers (27 corpus actif + 1 annexe en attente)

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

06_ANNEXES -- hors dependance -- ne fonde rien -- ne gouverne rien
```

Lecture : un document de la couche N peut citer des documents
des couches inferieures (N-1, N-2...).
Un document de la couche N ne devrait jamais dependre
d un document d une couche superieure.

Exception documentee : PREREG_OS_v1_6 cite J5 v1.6 (couche 05).
Reference croisee ascendante -- notee comme exception.

Regle 06_ANNEXES : aucun document des couches 00 a 05 ne cite
un document de 06_ANNEXES. La dependance est unidirectionnelle
et orientee vers le bas uniquement si activation.

---

## 5. CRITERES DE PLACEMENT -- QUESTIONS DE DECISION

Pour tout nouveau document OS, questions dans l ordre :

Q1 : Est-ce que ce document pose des axiomes ou des structures formelles ?
Oui -> 01_THEORIE
Non -> Q2

Q2 : Est-ce que ce document definit comment travailler ?
Oui -> 02_METHODE
Non -> Q3

Q3 : Est-ce que ce document definit le programme OS lui-meme ?
Oui -> 03_PROGRAMME

Q3b : Est-ce que ce document trace une phase d execution ?
Oui -> 04_PHASES / Phase_N

Q3c : Est-ce que ce document configure ou trace l agent IA ?
Oui -> 05_KERNEL

Q3d : Est-ce un candidat externe place en reserve par decision Pilote ?
Oui -> 06_ANNEXES / ATTENTE

Aucune reponse claire -> 00_META ou discussion avec Pilote

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

Hors reconstruction
  06_ANNEXES/ATTENTE/* -- statut propre -- activation conditionnelle
```

---

*Architecture v1.3 -- ajout couche 06_ANNEXES/ATTENTE -- DABO en reserve -- 18.03.2026*
*Toute modification fait l objet d un increment de version*
