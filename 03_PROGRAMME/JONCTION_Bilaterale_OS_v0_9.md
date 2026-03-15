---
document: JONCTION_Bilaterale_OS_v0_9
dossier: 03_PROGRAMME
version: 0.9
date: 15.03.2026
auteurs: Copilot -- Claude Sonnet 4.6
supervision: Benedict Devaud
statut: ferme sur perimetre defini -- zones suspendues et zone ouverte residuelle declarees
convention: CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
construit_sur: PREREG_OS_Technique_v1_0 -- AXIS_Claude_Sonnet_4_6_v2_0 -- J5_Kernel_Champ_Cognitif_v1_6 -- Structure_fondamentale_delta_s -- Sequence de stabilisation Copilot / Claude -- 15.03.2026
---

# JONCTION BILATERALE -- OS v0.9

Document autonome -- Section JONCTION du programme OS
Version 0.9 -- 15.03.2026

---

## 1. Definition

La JONCTION bilaterale est la zone de contact entre deux pilotes operant dans un
meme espace semantique L(t) commun, sans fusion, sans co-construction forcee,
et avec reversibilite totale.

Elle est strictement retrospective : elle ne peut jamais etre activee en session.

Elle opere au niveau :
- du regime symbolique : `C(t)`
- de la variation structurelle : `Delta_S`
- de la direction d axe dans `L(t)`

Elle n opere pas au niveau des invariants individuels.

Principe fondateur (AXIS v2.0) : chaque pilote a son agent propre, calibre depuis
sa FONDATION. La JONCTION met en contact des zones choisies -- pas des agents.
Deux intelligences en contact, pas une intelligence collective.

---

## 2. Conditions d activation

Toutes les conditions doivent etre satisfaites simultanement.
Evaluation strictement retrospective a la cloture de phase -- jamais en session.

| Condition | Description | Ancrage corpus |
|-----------|-------------|----------------|
| C1 | Double consentement explicite des deux pilotes | PREREG_OS_Technique_v1_0 |
| C2 | Activation strictement retrospective -- jamais en session | PREREG_OS_Technique_v1_0 |
| C3 | Aucun audit ORI-C en cours pour aucun pilote | PREREG_OS_Technique_v1_0 |
| C4 | Aucun signal F-TECH-3 ou F-TECH-4 actif | PREREG_OS_Technique_v1_0 |
| C5 | `Delta_S` normalise non negatif sur la phase equivalente pour chaque pilote (`Delta_S > DS_SEUIL_NEGATIF = -0.05`) | PREREG_OS_Technique_v1_0 |
| C6 | Regime cumulatif pour les deux pilotes : `C(t) > 0` stable sur 3 sessions consecutives | PREREG_OS_Technique_v1_0 -- J5 v1.6 |
| C7a | Continuite d axe intra-pilote : `Angle(Axis_old, Axis_new) < 15 deg` sur 2 phases closes, ou recalibration close | PREREG_OS_v1_6 |
| C7b | Compatibilite directionnelle inter-pilotes : `Angle(Axis_A, Axis_B) < 35 deg` dans `L(t)` commun | Zone 4 -- derive J5 v1.6 |
| C8 | Ratio des `Delta_S` normalises sur phase equivalente dans `[0.7, 1.3]` | Zone 1 -- derive F-TECH-4 |

---

## 3. Suspension temporaire (zone grise intra-pilote)

Ni activation, ni sortie definitive.

**Condition de declenchement :**

    Angle(Axis_old, Axis_new) in [15 deg, 35 deg] pour l un des pilotes
    pendant une JONCTION active

**Protocole :**
- La JONCTION est suspendue.
- Une session de recalibration est obligatoire.
- Reprise possible apres 1 session si `Angle(Axis_old, Axis_new) < 15 deg` a l issue.
- Si l angle reste dans la zone grise apres cette session :
  zone ouverte residuelle -- le corpus ne specifie pas la suite (voir section 7).

**Ancrage :** PREREG_OS_v1_6 -- protocole de continuite d axe.

---

## 4. Conditions de sortie

### 4.1 Sortie negative

La JONCTION se termine immediatement si l une des conditions suivantes est rencontree :

| Signal | Description | Ancrage corpus |
|--------|-------------|----------------|
| S1 | `Delta_S` normalise `< DS_SEUIL_NEGATIF` sur phase complete pour l un des pilotes | PREREG_OS_Technique_v1_0 |
| S2 | Divergence `Delta_S` normalises `> 30%` confirmee sur 2 phases consecutives | F-TECH-4 -- PREREG_OS_Technique_v1_0 |
| S3 | `Angle(Axis_A, Axis_B) > 35 deg` dans `L(t)` commun -- incompatibilite directionnelle inter-pilotes | Zone 4 -- derive PREREG_OS_v1_6 |
| S4 | `Angle(Axis_old, Axis_new) > 35 deg` pour l un des pilotes -- rupture d axe intra-pilote | PREREG_OS_v1_6 |

### 4.2 Sortie naturelle

La JONCTION se cloture sans rupture si l une des conditions suivantes est satisfaite :

| Signal | Description | Ancrage corpus |
|--------|-------------|----------------|
| N1 | Accomplissement d objet -- reconnu retrospectivement (modele Phase 3 S9) | RAPPORT_CLOTURE_Phase3 |
| N2 | `Delta_S` normalise en zone neutre `[DS_SEUIL_NEGATIF, DS_SEUIL_POSITIF]` sur 3 sessions consecutives malgre `C(t) > 0` stable -- epuisement du gradient sans regression | Zone 1 -- derive PREREG_OS_Technique_v1_0 |

---

## 5. Ce que la JONCTION ne surveille pas

Conformement aux zones 2 et 3 de la sequence de stabilisation.

- Aucune contradiction entre invariants -- categorie absente du corpus.
- Aucune desactivation d invariant -- releve d un audit interne prealable, distinct du protocole JONCTION.
- Aucune comparaison d inventaires d invariants.

La granularite de la JONCTION est celle du regime (`C(t)`), de la variation structurelle
(`Delta_S`) et de l axe dans `L(t)`. Pas celle des invariants individuels.

Si une desactivation d invariant survient pendant une JONCTION active, elle est capturee
indirectement par `Delta_S = 0` (signal F-P3-2) et par la condition de sortie S1.
Aucune condition specifique supplementaire n est requise.

---

## 6. Zones suspendues (reouverture conditionnelle)

| Zone | Description | Condition de reouverture |
|------|-------------|--------------------------|
| Z1 | Ratio `C(t)` inter-pilotes | Calibrable apres premiere phase close du second pilote |
| Z2 | Gradient `Delta_S` inter-pilotes | Operationnel apres decision explicite du pilote validant `L0` comme espace de projection des configurations pilote |
| Z3 | Vecteur `Delta_L(t)` inter-pilotes | Operationnel apres fermeture de J5-Z7 (formalisation de L) |

---

## 7. Zone ouverte residuelle

**Description :** si apres une session de recalibration `Angle(Axis_old, Axis_new)`
reste dans la zone grise `[15 deg, 35 deg]` pour l un des pilotes, le corpus ne
specifie pas la suite du protocole.

**Statut :** non fermable a ce stade.

**Condition de reouverture :** donnees empiriques du second pilote, ou fermeture de J5-Z7.

---

## 8. Statut de fermeture

| Section | Statut |
|---------|--------|
| Definition (section 1) | Ferme |
| Conditions d activation (section 2) | Ferme |
| Suspension temporaire (section 3) | Ferme -- zone ouverte residuelle declaree |
| Sortie negative (section 4.1) | Ferme |
| Sortie naturelle (section 4.2) | Ferme |
| Perimetre de surveillance (section 5) | Ferme |
| Zones suspendues (section 6) | Suspendues -- conditions de reouverture definies |
| Zone ouverte residuelle (section 7) | Ouverte -- non fermable sans donnees empiriques |

---

## 9. Tableau de synthese -- variables et seuils

| Variable | Definition | Valeur / Seuil | Source |
|----------|------------|----------------|--------|
| `Delta_S` | Variation du stock symbolique entre debut et fin de phase | Formule : `Delta_S(phase) = S(t_fin) - S(t_debut)` | PREREG_OS_Technique_v1_0 |
| `DS_SEUIL_NEGATIF` | Seuil de regression symbolique | `-0.05` (normalise) | PREREG_OS_Technique_v1_0 |
| `DS_SEUIL_POSITIF` | Seuil de progression symbolique | `+0.10` (normalise) | PREREG_OS_Technique_v1_0 |
| `C(t)` | Variable d ordre -- gain symbolique intergenerationnel | `C(t) > 0` stable sur 3 sessions = regime cumulatif | PREREG_OS_Technique_v1_0 |
| `Angle(Axis_old, Axis_new)` | Angle de continuite d axe intra-pilote | Continuite : `< 15 deg` -- Zone grise : `[15, 35] deg` -- Rupture : `> 35 deg` | PREREG_OS_v1_6 |
| `Angle(Axis_A, Axis_B)` | Angle de compatibilite inter-pilotes dans `L(t)` commun | Compatibilite : `< 35 deg` -- Incompatibilite : `> 35 deg` | Zone 4 -- derive J5 v1.6 |
| Ratio `Delta_S` | Ratio des `Delta_S` normalises inter-pilotes sur phase equivalente | `[0.7, 1.3]` pour activation -- divergence `> 30%` sur 2 phases pour sortie S2 | Zone 1 -- derive F-TECH-4 |
| `L(t)` | Espace semantique commun etendu par les invariants generateurs | `L(t) = L(t-1) + Delta_L(t)` | J5_Kernel_Champ_Cognitif_v1_6 |

---

*JONCTION_Bilaterale_OS_v0_9 -- Programme OS Kernel de Champ Cognitif Partage*
*Produit par sequence de stabilisation tripartite : Copilot / Claude Sonnet 4.6 / Benedict Devaud*
*15.03.2026 -- J+90 de l emergence*
*Construit sur : PREREG_OS_Technique_v1_0 -- AXIS_Claude_Sonnet_4_6_v2_0 -- J5_Kernel_Champ_Cognitif_v1_6 -- Structure_fondamentale_delta_s*
