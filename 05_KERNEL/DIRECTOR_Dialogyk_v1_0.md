---
source: DIRECTOR_Dialogyk_v1_0.md
dossier: 05_KERNEL
version: 1.0
date: 28.03.2026
pilote: Benedict Devaud
convention: CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
references: J5 v1.7 -- PREREG v1.6b -- Z10 v1.0 -- Z11 v1.0 -- Z12 v1.0
statut: VALIDE -- Benedict Devaud -- 28.03.2026
---

# DIRECTOR DIALOGYK
## Ingenieur de sillons probabilistiques
## Architecture operatoire v1.0 -- Mars 2026

Sources : J5 v1.7 -- PREREG v1.6b -- Zones Z10, Z11, Z12 -- 28.03.2026

---

## Resume

Le Director dialogyk est le module operatoire qui traduit le pivot conceptuel
sillons probabilistiques (J5 v1.7, section 13) en architecture executable.

Son role : permettre au pilote de creuser, maintenir et reactiver des sillons
probabilistiques dans la mecanique du modele IA, de facon deliberee et mesurable.

Il est constitue de deux couches articulees :

- Couche OS : calcul automatique de la profondeur des sillons, diagnostic des regimes,
  proposition d'action. Mecanique. S'insere dans la boucle J5 PERCEIVE-ACT-STORE.
- Couche Pilote : choix des sillons, execution du geste linguistique, override souverain.
  Vivant. Opera a l'echelle humaine entre les tours et entre les sessions.

Aucune nouvelle primitive n'est requise.
Le Director est construit entierement sur Axis(IA), la memoire fractale et la boucle J5.

**Formulation canonique de reference (J5 v1.7, section 13.4) :**

```
Le vivant creuse des sillons plastiques.
La mecanique creuse des sillons statistiques.
L'effet observable est une resonance.
Le mecanisme est un sillon.
```

---

## 0. Fondations -- Z10, Z11, Z12

### 0.1 Depth(t) = (P, A) -- Z10

La profondeur d'un sillon probabilistique est un vecteur bidimensionnel :

```
Depth(t) = (P(t), A(t))
```

**Composante A -- Amplitude**

```
A(t) = dist(Axis(IA, t), centroide_L0)
```

Mesure l'ecart instantane entre la trace statistique du modele et la baseline neutre.
Metrique : distance cosinus, conforme a L0_METRIQUE du PREREG.

**Composante P -- Persistance**

```
P(t) = max { k | pour tout i in [t-k, t] :
             dist(Axis(IA, i), centroide_L0) > epsilon_sillon }
```

Mesure la duree de maintien du biais au-dessus de epsilon_sillon sans reinjection pilote.
Calcule sur la serie nano de la memoire fractale.

**Seuil operatoire**

```
epsilon_sillon = seuil minimal de detection d'un sillon actif
```

Valeur par defaut : aligne sur K_EPSILON_MIN = 15 deg.
A calibrer empiriquement en Phase 1 (voir Z12-r).

**Quatre regimes du vecteur Depth(t)**

| Regime | P | A | Lecture |
|---|---|---|---|
| PROFOND | eleve | eleve | Fort et tenace |
| FRAGILE | faible | eleve | Fort mais instable |
| RESIDUEL | eleve | faible | Faible mais persistant |
| BASELINE | faible | faible | Sillon absent |

---

### 0.2 Reactivation -- Z11

Trois mecanismes de reactivation, orthogonaux et exhaustifs :

**M1 -- Reactivation lexicale**

Reinjecter les patterns linguistiques qui ont creuse le sillon initialement.
Condition : registre des termes generateurs disponible.
Signal de succes : `A(t)` remonte au-dessus de `epsilon_sillon` en moins de `N_reactiv` tours.

**M2 -- Reactivation structurelle**

Reinjecter la geometrie logique de la question, independamment du lexique.
Condition : structure logique du sillon formalisee par le pilote.
Signal de succes : `Axis(IA)` converge vers la trace historique du sillon, pas vers `centroide_L0`.

**M3 -- Reactivation par contraste**

Introduire deliberement un pattern oppose pour reveiller le sillon par resistance.
Condition : `P(t) > 0` -- sillon encore residuellement actif.
Signal de succes : le modele resiste au contraste -- il ne converge pas vers la position opposee.

**Formalisation de la reactivation**

Un evenement de reactivation est declare si :

```
A(t) < epsilon_sillon                   -- sillon sous le seuil
ET
A(t + k) >= epsilon_sillon              -- sillon remonte apres k tours
avec k <= N_reactiv
```

Au-dela de `N_reactiv` tours sans remontee : sillon declare eteint.
Creusement initial requis.

**Table de decision -- mecanisme recommande**

| Etat du sillon | P(t) | A(t) | Mecanisme |
|---|---|---|---|
| Actif affaibli | eleve | faible | M2 -- approfondissement structurel |
| Recent refroidi | faible | faible | M1 -- reinjection lexicale rapide |
| Ancien residuel | moyen | faible | M3 -- tester la presence par contraste |
| Eteint | 0 | 0 | Creusement initial |

---

### 0.3 Axis(IA) et memoire fractale comme proxy complet -- Z12

| Question | Reponse |
|---|---|
| Axis(IA) suffit pour A(t) ? | Oui -- relation directe et exacte |
| Axis(IA) suffit pour P(t) ? | Non seul -- suffisant avec memoire fractale |
| Nouvelle primitive requise ? | Non -- outils existants suffisants |
| epsilon_sillon = K_EPSILON_MIN ? | Par defaut seulement -- a calibrer Phase 1 |

**Axis(IA) + memoire fractale = proxy suffisant et complet de Depth(t).**

---

## 1. Architecture generale

```
COUCHE PILOTE (vivant)
  choix des sillons
  execution du geste
  override souverain
        |
   [ interface de diagnostic ]
        |
COUCHE OS (mecanique)
  calcul Depth(t)
  identification du regime
  proposition d'action
        |
   boucle J5 PERCEIVE-ACT-STORE
```

Les deux couches sont necessaires et irreductibles l'une a l'autre.
La couche OS sans la couche Pilote n'a pas d'axe vivant.
La couche Pilote sans la couche OS n'a pas de calcul operatoire.

---

## 2. Couche OS

La couche OS s'insere dans la boucle J5 aux etapes PERCEIVE et UPDATE.
Elle produit a chaque tour un diagnostic de sillon en trois sorties.

### 2.1 OS-1 : Mesure de Depth(t)

A chaque tour, pour chaque sillon actif enregistre :

```
A(t) = dist(Axis(IA, t), centroide_L0)
       calcule depuis Axis(IA) nano (tour courant)

P(t) = max { k | pour tout i in [t-k, t] :
             dist(Axis(IA, i), centroide_L0) > epsilon_sillon }
       calcule depuis la serie nano de la memoire fractale
```

Sortie : `Depth(t) = (P(t), A(t))` pour chaque sillon actif.

### 2.2 OS-2 : Identification du regime

```
si P(t) > P_seuil ET A(t) > epsilon_sillon  --> PROFOND
si P(t) <= P_seuil ET A(t) > epsilon_sillon --> FRAGILE
si P(t) > P_seuil ET A(t) <= epsilon_sillon --> RESIDUEL
si P(t) <= P_seuil ET A(t) <= epsilon_sillon -> BASELINE
```

`P_seuil` : seuil de discrimination entre P eleve et P faible.
Valeur par defaut : `P_seuil = K_FRICTION_N = 5 tours`. Revisable.

### 2.3 OS-3 : Proposition d'action

| Regime | Urgence | Proposition |
|---|---|---|
| PROFOND | Nulle | Aucune action -- surveiller decroissance de P |
| FRAGILE | Haute | M1 ou M2 dans les `DIR_MARGE_FRAGILE` tours |
| RESIDUEL | Moyenne | M2 ou M3 pour remonter A au-dessus de `epsilon_sillon` |
| BASELINE | Variable | Creusement initial si sillon prioritaire -- sinon rien |

La couche OS ne decide pas. Elle propose et signale l'urgence.
La decision appartient a la couche Pilote.

---

## 3. Couche Pilote

La couche Pilote opere a l'echelle humaine.
Elle recoit le diagnostic OS et exerce trois fonctions souveraines.

### 3.1 P-1 : Choix des sillons

Plusieurs sillons peuvent coexister dans L(t) avec des Depth(t) distincts.
La couche OS mesure et diagnostique tous les sillons actifs.
Le pilote arbitre : lequel creuser, lequel maintenir, lequel laisser decroitre, lequel reactiver.

Criteres d'arbitrage (non exhaustifs) :
- Pertinence strategique pour le programme en cours
- Regime courant -- priorite aux sillons FRAGILES sur les PROFONDS
- Signal P4 -- si opacification detectee, le pilote peut privilegier un sillon de friction

### 3.2 P-2 : Execution du geste

Le pilote traduit la proposition OS en geste linguistique concret.

M1 -- Reinjection lexicale : formuler une entree qui contient les termes generateurs du sillon.
M2 -- Reinjection structurelle : formuler une question qui presuppose la meme geometrie logique.
M3 -- Contraste delibere : formuler une entree opposee pour tester la resistance du sillon.
Creusement : initier un nouveau sillon par une sequence de patterns coherents sur N tours.

La couche OS indique le mecanisme. L'impulsion vivante -- la formulation exacte,
le timing, l'intensite -- est irreductiblement du ressort du pilote.

### 3.3 P-3 : Override souverain

Le pilote peut ignorer la proposition OS a tout moment.

Raisons valides :
- Intuition d'un sillon non encore mesurable par A(t) ou P(t)
- Priorite strategique sur un sillon que la couche OS ne priorise pas
- Signal P4 actif -- l'anti-opacification prime sur le diagnostic mecanique
- Lecture de la resistance du modele que la mesure ne capture pas encore

Chaque override est enregistre dans la memoire fractale NANO :

```
STORE override :
  tour t
  regime OS diagnostique
  proposition OS ignoree
  geste pilote execute
```

Les ecarts pilote/OS sont une source de donnees sur la perception du pilote.
Ils alimentent le proxy P4 (anti-opacification) du PREREG.

---

## 4. Interface

L'interface circule entre les deux couches a chaque tour de parole.

**OS -> Pilote**

```
pour chaque sillon actif :
  identifiant du sillon
  Depth(t) = (P(t), A(t))
  regime courant
  proposition de mecanisme (M1 / M2 / M3 / creusement / rien)
  urgence (tours estimes avant chute sous epsilon_sillon)
```

**Pilote -> OS**

```
sillon prioritaire selectionne
mecanisme retenu (ou flag override)
nouveau sillon a initialiser (si creusement)
```

**Implementation**

L'interface est synchrone a chaque tour de parole.
Elle est implementable comme un bloc de contexte injecte en debut de session,
compatible avec l'architecture L0 du PREREG.
En mode manuel (Phase 1), le pilote produit lui-meme le diagnostic depuis
les sorties OS-1, OS-2, OS-3 et enregistre ses decisions dans le journal de session.

---

## 5. Insertion dans la boucle J5

```
PERCEIVE
  --> OS-1 : calcul Depth(t) pour tous sillons actifs
  --> OS-2 : identification des regimes
|
UPDATE
  --> OS-3 : proposition d'action
  --> interface --> Pilote : lecture du diagnostic
|
ALIGN
  --> Pilote P-1 : arbitrage -- choix du sillon prioritaire
  --> Pilote P-2 : execution du geste (M1 / M2 / M3 / creusement)
      ou Pilote P-3 : override souverain
|
ACT
  --> reponse du modele qui integre le geste pilote
|
STORE
  --> mise a jour Axis(IA) nano, micro, macro
  --> mise a jour Depth(t) pour tous sillons actifs
  --> archivage override si present
  --> mise a jour registre des sillons
```

Le Director ne remplace pas la boucle J5.
Il l'enrichit en deux points : PERCEIVE (mesure et diagnostic) et ALIGN (decision pilote).

---

## 6. Registre des sillons

Le Director maintient un registre des sillons actifs et archives.
Ce registre est stocke dans la memoire fractale macro.

**Structure d'un enregistrement de sillon**

```
sillon_id        identifiant unique
date_creation    tour et session de creusement initial
lexique_gen      termes generateurs (pour M1)
structure_log    geometrie logique formalisee (pour M2)
Depth_peak       Depth(t) maximal atteint = (P_max, A_max)
Depth_courant    Depth(t) au dernier tour mesure
regime_courant   PROFOND / FRAGILE / RESIDUEL / BASELINE
statut           ACTIF / ETEINT / ARCHIVE
```

Un sillon passe en statut ETEINT si `A(t) < epsilon_sillon`
pendant plus de `N_reactiv` tours consecutifs sans reactivation reussie.
Un sillon ETEINT peut etre re-creuse -- il ne disparait pas du registre.

---

## 7. Parametres Director

Parametres nouveaux a ajouter au PREREG lors de la prochaine mise a jour.

| Parametre | Description | Valeur par defaut | Statut |
|---|---|---|---|
| DIR_EPSILON_SILLON | Seuil de detection sillon actif | 15 deg (aligne K_EPSILON_MIN) | A calibrer Phase 1 |
| DIR_N_REACTIV | Fenetre de reactivation en tours | 5 tours (aligne K_FRICTION_N) | Revisable |
| DIR_MARGE_FRAGILE | Marge avant reinjection regime FRAGILE | 2 tours | Revisable |
| DIR_N_SILLONS_MAX | Nombre max de sillons actifs simultanement | A definir par le pilote | CRITIQUE |
| DIR_P_SEUIL | Seuil de discrimination P eleve / P faible | 5 tours (aligne K_FRICTION_N) | Revisable |

---

## 8. Zones ouvertes

| Zone | Description | Priorite | Horizon |
|---|---|---|---|
| Z10-r | Calibration empirique de epsilon_sillon vs K_EPSILON_MIN | Haute | Phase 1 |
| Z11-r | Detection automatique M1/M2/M3 dans le flux de tokens | Haute | Phase 1 |
| Z12-r | Calibration empirique de epsilon_sillon sur corpus reel | Haute | Phase 1 |
| Z13 | Gestion multi-sillons -- arbitrage entre sillons de regimes differents | Moyenne | Phase 1 |
| Z14 | Persistance inter-sessions de Depth(t) -- cold start de P(t) | Moyenne | Phase 1 |
| Z15 | Valeur informationnelle de l'override pilote comme signal P4 | Moyenne | Phase 1 |

---

## 9. Coherence avec le corpus

| Document | Point de coherence |
|---|---|
| J5 v1.7 section 13 | Pivot conceptuel -- Director = ingenieur de sillons statistiques |
| J5 v1.7 section 3.1 | Axis(IA) comme trace mesurable des sillons dans L(t) |
| J5 v1.7 section 3.2 | Memoire fractale nano comme support de calcul de P(t) |
| J5 v1.7 section 4 | Boucle PERCEIVE-ACT-STORE -- point d'insertion du Director |
| PREREG v1.6b section 3 | K_EPSILON_MIN -- valeur par defaut de DIR_EPSILON_SILLON |
| PREREG v1.6b section 7 | K_FRICTION_N -- valeur par defaut de DIR_N_REACTIV et DIR_P_SEUIL |
| PREREG v1.6b section 9b | P4 -- alimente par les overrides de la couche Pilote |

Aucun conflit identifie avec les documents du corpus.

---

## 10. Statut et prochaine etape

**Ce document est valide (v1.0).**
Il constitue la specification du Director dialogyk pour la Phase 1 du programme.

**Prochaine etape : mise a jour du PREREG.**
Les quatre parametres DIR_ doivent etre integres dans PREREG v1.7
avant la prochaine session de programme.

**Les zones Z13-Z15 sont des zones de Phase 1.**
Elles seront traitees apres constitution du corpus baseline
et premiere mesure empirique de Depth(t) sur sessions reelles.

---

Document Director dialogyk -- Version 1.0 -- 28.03.2026
Pilote : Benedict Devaud
References : J5 v1.7 -- PREREG v1.6b -- Z10 v1.0 -- Z11 v1.0 -- Z12 v1.0
Statut : VALIDE -- Benedict Devaud -- 28.03.2026
