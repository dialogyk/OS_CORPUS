# PROGRAMME OS -- KERNEL DE CHAMP COGNITIF PARTAGE
## PRE-ENREGISTREMENT TECHNIQUE -- ARCHITECTURE MULTI-PILOTES / MULTI-PROGRAMMES

Version 1.0 -- 13.03.2026
Construit sur : PREREG_OS_v1_6 -- Amendements v1.0-v1.2 -- Phase 2 v1.0 -- Phase 3 v1.0

Reconstruction ASCII-safe depuis source JPEG (signe micro x2)
Convention : CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
Statut : reconstruit -- a valider par Pilote

---

## 0. Objet et perimetre

Ce document specifie l architecture technique du programme OS dans sa dimension
multi-pilotes et multi-programmes. Il ne remplace pas les PREREG de phase --
il definit le couloir structurel dans lequel ils operent.

Trois decisions de cadrage, tranchees ex ante :

| Decision | Valeur retenue | Justification |
|----------|---------------|---------------|
| L0 | Commun a tous les pilotes -- metrique cosinus partagee | Sans espace commun, la comparaison inter-pilotes est sans base |
| Multi-programmes | Programmes paralleles independants, pilotes distincts | Les phases d un programme n interferent pas avec celles d un autre |
| Fenetre Delta_S | Par phase fermee -- unite naturelle de S(t) | Session trop courte ; programme complet trop long pour detecter la dynamique |

---

## 1. Architecture 4 niveaux

Le programme OS s articule sur quatre niveaux d observation et de mesure.
Chaque niveau a ses propres variables, sa propre fenetre temporelle et ses propres
operateurs. Ils ne sont pas hierarchises rigidement -- ils sont couples.

| Niveau | Nom | Fenetre | Variables actives | Operateurs |
|--------|-----|---------|-------------------|------------|
| N1 | Session | Tours de parole (nano/micro) -- 1-10 tours | O(t), R(t), I(t), Axis(IA), P4 friction, Memoire fractale nano | Mesure proxies, Detection angle, Signal P4, Mise a jour MF |
| N2 | Programme | Phase fermee (3-15 sessions) | Cap(t), Sigma_op(t), V(t), S(t) accumule, Tests T1-T7 | Agregation ORI-C, Tension structurelle, Tests causaux, Audit ORI-C |
| N3 | Pilote | Programme complet (toutes phases) | C(t) -- variable d ordre, Delta_S par phase, Regime symbolique | Attribution S -> C, Detection bascule T7, Classification regime |
| N4 | Collectif | Corpus multi-pilotes (comparaison croisee) | Delta_S inter-pilotes, L0 commun, Structures invariantes | Comparaison cosinus, Detection patterns, Regime collectif |

---

## 2. JONCTION -- Interface N2 / N3

La JONCTION est le couloir de bascule entre le niveau programme et le niveau pilote.
Elle detecte si Delta_S(t) depasse le bruit de fond du programme et produit un effet
mesurable sur C(t). C est ici que la dimension symbolique devient ou non cumulative.

| Parametre | Definition | Valeur |
|-----------|------------|--------|
| JONC_FENETRE | Fenetre de calcul Delta_S | Phase fermee (debut a fin) |
| JONC_SEUIL_BASCULE | Delta_S minimal pour declencher T7 (point de bascule S(t)) | mu_Delta_S + 1.5 * sigma_Delta_S sur le corpus pilote |
| JONC_SIGNAL_POSITIF | Condition de franchissement de la JONCTION | T7 valide + C(t) > 0 stable sur 3 sessions consecutives |
| JONC_SIGNAL_NEGATIF | Regression symbolique -- JONCTION non franchie | Delta_S < 0 sur phase complete ou C(t) invariant malgre Delta_S significatif |
| JONC_AUDIT | Moment d evaluation | A chaque fermeture de phase -- avant ouverture de la phase suivante |

**Operateur JONCTION :**

    JONCTION active si et seulement si :
    T7 valide ET Delta_S(phase) > JONC_SEUIL_BASCULE ET C(t) montre une variation attribuable a S(t) (test T4)

*Note : La JONCTION ne se declare pas -- elle se detecte retrospectivement a la fermeture de phase.
Elle n est jamais evaluee en temps reel.*

---

## 3. Delta_S -- Indicateur central

Delta_S est la variation du stock symbolique S(t) entre l ouverture et la fermeture
d une phase. C est l indicateur de progression ou regression du regime symbolique.
Il est calcule par pilote, par phase, et agrege au N4 pour comparaison inter-pilotes.

| Parametre | Definition | Valeur / Formule |
|-----------|------------|------------------|
| DS_FORMULE | Formule de base | Delta_S(phase) = S(t_fin_phase) - S(t_debut_phase) |
| DS_COMPOSANTES | Composantes de S(t) -- poids herites PREREG v1.6 | w_R=0.30 (Repertoire), w_C=0.25 (Codification), w_D=0.25 (Densite), w_F=0.20 (Fidelite) |
| DS_NORMALISATION | Normalisation inter-pilotes pour comparaison N4 | Delta_S normalise = Delta_S / S(t_debut_phase) (variation relative -- evite le biais de niveau initial) |
| DS_SEUIL_POSITIF | Progression symbolique confirmee | Delta_S normalise > +0.10 sur phase complete |
| DS_SEUIL_NEGATIF | Regression symbolique -- signal d alerte | Delta_S normalise < -0.05 sur phase complete |
| DS_BRUIT | Zone neutre -- ni progression ni regression | -0.05 <= Delta_S normalise <= +0.10 |
| DS_AGREGATION_N4 | Agregation collective | Mediane des Delta_S normalises sur le corpus multi-pilotes (mediane -- robuste aux outliers) |

**Regimes symboliques detectes par Delta_S :**

| Regime | Condition Delta_S | C(t) | Statut programme |
|--------|-------------------|------|------------------|
| Pre-seuil | Delta_S neutre ou negatif | C(t) ~= 0 | Phase 1 normale -- pas de bascule attendue |
| Transition | Delta_S positif mais instable | C(t) variable | JONCTION en cours -- surveiller T4 et T7 |
| Cumulatif | Delta_S positif stable + T7 valide | C(t) > 0 stable | JONCTION franchie -- Phase suivante activable |
| Regressif | Delta_S < DS_SEUIL_NEGATIF | C(t) en baisse | Alerte -- audit ORI-C obligatoire avant poursuite |

---

## 4. Structure multi-pilotes

Chaque pilote opere un programme independant dans L0 commun.
L Axis(pilote) est propre a chaque pilote -- calcule dans L0 partage.
La comparaison inter-pilotes porte uniquement sur Delta_S normalise et les regimes
symboliques.

| Parametre | Valeur | Note |
|-----------|--------|------|
| L0_COMMUN | Embedding semantique 1536 dim -- metrique cosinus partagee -- PREREG Section 2 | Partage entre tous les pilotes |
| AXIS_PILOTE | Axis(pilote) calcule dans L0 -- propre a chaque pilote | Seul Delta_S est comparable |
| MP_SEUIL_CORPUS | Taille minimale corpus N4 pour analyse collective | 3 pilotes minimum -- 2 phases fermees chacun |
| MP_COMPARAISON | Axe de comparaison inter-pilotes | Delta_S normalise par phase -- mediane collective -- distribution des regimes |
| MP_ISOLATION | Isolation des programmes | Aucune contamination croisee entre programmes pendant les phases actives |

---

## 5. Structure multi-programmes

Un programme = un pilote + un agent programme + une sequence de phases.
Les programmes sont paralleles et independants.
Leur comparaison est possible a la cloture de chaque phase via Delta_S.

| Niveau | Unite | Granularite Delta_S | Comparaison possible |
|--------|-------|---------------------|----------------------|
| Intra-programme | Phase (ex : Phase 1, Phase 2, Phase 3) | Delta_S par phase fermee | Progression interne du pilote |
| Inter-phases | Comparaison Phase N vs Phase N+1 | Delta_S(N+1) - Delta_S(N) | Acceleration ou deceleration symbolique |
| Inter-programmes | Comparaison de pilotes a phase equivalente | Delta_S normalise median N4 | Distribution des regimes -- structures invariantes |
| Corpus collectif | Ensemble des phases fermees de tous les pilotes | Agregation N4 complete | Detection de patterns transversaux |

**Protocole de cloture de phase (commun a tous les programmes) :**

| Etape | Action | Resultat attendu |
|-------|--------|-----------------|
| 1 | Calcul S(t_fin) sur les 4 composantes -- poids fixes ex ante | Valeur S finale de la phase |
| 2 | Calcul Delta_S(phase) = S(t_fin) - S(t_debut) | Delta_S brut |
| 3 | Normalisation : Delta_S / S(t_debut) | Delta_S normalise -- comparable inter-pilotes |
| 4 | Classification regime (tableau section 3) | Pre-seuil / Transition / Cumulatif / Regressif |
| 5 | Evaluation JONCTION (section 2) -- si applicable | JONCTION active / inactive |
| 6 | Depot dans corpus N4 -- horodate | Donnee disponible pour comparaison collective |
| 7 | Decision ouverture phase suivante -- pilote | Phase suivante ouverte ou programme suspendu |

---

## 6. Conditions de falsification -- niveau technique

Ces conditions s ajoutent aux conditions F1-F5 du PREREG v1.6 et aux conditions
F-P2 / F-P3 des PREREG de phase. Elles portent sur l architecture multi-niveaux
et sur Delta_S.

| Condition | Description | Decision |
|-----------|-------------|----------|
| F-TECH-1 -- Delta_S non calculable | S(t) ne peut pas etre mesure sur 2 phases consecutives | Suspension du programme -- revue des proxies ex ante avant reprise |
| F-TECH-2 -- JONCTION systematiquement inactive | Delta_S positif sur 3 phases consecutives sans que T7 soit jamais valide au seuil JONC_SEUIL_BASCULE | Si persistant : requalification comme regime pre-seuil indefini |
| F-TECH-3 -- Divergence N1/N3 | Proxies O, R, I positifs sur 3 sessions ET C(t) en regression | Audit immediat -- decorrelation structurelle a investiguer |
| F-TECH-4 -- Corpus N4 non comparable | Delta_S normalises des pilotes divergent de plus de 3 sigma sans explication structurelle | Verification de l homogeneite de L0 entre pilotes -- possible contamination |

---

## 7. Recapitulatif des parametres techniques

| Parametre | Valeur | Statut |
|-----------|--------|--------|
| L0_COMMUN | Embedding 1536 dim -- cosinus -- L2 | DEFINI |
| DS_FENETRE | Phase fermee | DEFINI |
| DS_POIDS | w_R=0.30 / w_C=0.25 / w_D=0.25 / w_F=0.20 | HERITE v1.6 |
| DS_SEUIL_POSITIF | Delta_S normalise > +0.10 | DEFINI |
| DS_SEUIL_NEGATIF | Delta_S normalise < -0.05 | DEFINI |
| DS_AGREGATION_N4 | Mediane inter-pilotes | DEFINI |
| JONC_FENETRE | Phase fermee | DEFINI |
| JONC_SEUIL_BASCULE | Delta_S > mu_Delta_S + 1.5 * sigma_Delta_S | DEFINI |
| JONC_SIGNAL_POSITIF | T7 + C(t) > 0 stable 3 sessions | DEFINI |
| JONC_AUDIT | A chaque fermeture de phase | DEFINI |
| MP_SEUIL_CORPUS | 3 pilotes min -- 2 phases fermees chacun | DEFINI |
| MP_ISOLATION | Aucune contamination croisee pendant phases actives | DEFINI |
| K_EPSILON_MIN | 15 degres | HERITE v1.6 |
| TOPO_SEUIL_CONTINUITE | 15 degres | HERITE v1.6 |
| ORIC_DELTA | 5 sessions | HERITE v1.6 |

---

*Ce document est operationnel des signature. Il ne requiert pas de revision avant ouverture
d un nouveau programme -- sauf modification des proxies S(t) ou changement de la metrique L0.*

| Champ | Valeur |
|-------|--------|
| Reference | PREREG_OS_Technique_v1_0 |
| Date | 13.03.2026 |
| Construit sur | PREREG_OS_v1_6 -- Amendements v1.0-v1.2 -- Phase 2 v1.0 -- Phase 3 v1.0 |
| Signature pilote | |
| Date signature | |

---

*Reconstruction v1.0 -- source : PREREG_OS_Technique_v1_0.pdf (4 pages JPEG, signe micro x2)*
*Conforme a CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md*
