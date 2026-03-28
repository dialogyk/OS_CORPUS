---
source: PREREG_OS_v1_6b.md
dossier: 03_PROGRAMME
version: 1.6b
date: 28.03.2026
pilote: Benedict Devaud
convention: CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
amendement_integre: AMENDEMENT_J5_PREREG_v1_7 -- valide Benedict Devaud -- 28.03.2026
remplace: PREREG_OS_v1_6.md
reference: J5 v1.7 -- TUS v4.3 -- ORI-C Pancarte Normative v1.0
note_v1_6b: J5 v1.7 integre le pivot conceptuel sillons probabilistiques (28.03.2026)
---

# PREREG -- OS Kernel de Champ Cognitif Partage
Version 1.6b -- SIGNE -- 10.03.26 -- Amendement pivot integre 28.03.2026
SIGNE -- Benedict Devaud -- 10.03.26

Reference : J5 v1.7 -- TUS v4.3 -- ORI-C Pancarte Normative v1.0
[v1.6b] Note : J5 v1.7 integre le pivot conceptuel sillons probabilistiques (28.03.2026)

STATUT : DOCUMENT SIGNE. Benedict Devaud -- 10.03.2026.
Phase 1 operationnelle. Corpus baseline en cours de constitution.
Amendement pivot conceptuel integre -- 28.03.2026.

LEGENDE : Fond vert = valeur par defaut raisonnable, revisable.
Fond jaune = parametre critique, revision obligatoire avant signature.

Ce document est organise en deux niveaux.
Les parametres stables sont des valeurs par defaut calibrees sur des programmes
de cognition humain-IA comparables -- ils peuvent etre conserves pour un premier
programme sans revision approfondie.
Les parametres critiques dependent du contexte specifique du programme
et ne peuvent pas etre remplis sans une decision explicite du pilote.

---

## Recapitulatif -- Tous parametres definis

Version 1.6b -- FINALE. Tous les parametres sont definis et valides,
incluant les 10 requetes de reference et le pivot conceptuel [v1.6b].

| Parametre | Valeur definie | Version |
|---|---|---|
| L0_DOMAINE | Evenement fondateur 15.12.25 -- boucle epistemologique TUS/J5 | v1.1 |
| TOPO_MODE | Bipolaire multi-instance -- 8 agents IA | v1.1/v1.2 |
| INV_CORPUS_REF | Option C -- 7 agents x 7 sessions = 49 conversations | v1.2 |
| K_EPSILON_MIN | 15 deg -- valide pilote | v1.3 |
| ORIC_S_POIDS | w_R=0.30, w_C=0.25, w_D=0.25, w_F=0.20 -- valide pilote | v1.3 |
| P4_MONO_DUREE | 15 sessions par agent -- valide pilote | v1.3 |
| SESS_RATIO_APPLICATION | 15% sessions d'application -- valide pilote | v1.3 |
| TOPO_SEUIL_CONTINUITE | 15 deg -- continuite preservee sous ce seuil | v1.4 |
| TOPO_SEUIL_RUPTURE | 35 deg -- nouvel agent declare au-dela | v1.4 |
| TOPO_REF_REQUETES_N | 10 requetes fixes -- R1 a R10 definies | v1.5 |
| PIVOT_CONCEPTUEL_REF | J5 v1.7 -- sillons probabilistiques | v1.6b |
| PIVOT_CONCEPTUEL_DATE | 28.03.2026 | v1.6b |
| PIVOT_CONCEPTUEL_STATUT | Integre -- programme non interrompu | v1.6b |
| Pilote | Benedict Devaud | v1.3 |
| Signature + date | Benedict Devaud -- 10.03.2026 | OBLIGATOIRE |

---

## 0. Identification du programme

| Champ | Valeur | Statut |
|---|---|---|
| Identifiant du programme | OS-KERNEL-15.12.25 | DEFINI |
| Date de creation du PREREG | 10.03.2026 | OBLIGATOIRE |
| Pilote(s) declare(s) | Benedict Devaud | OBLIGATOIRE |
| Agents IA du programme pilote | Claude Sonnet 4.6 (Anthropic) -- Copilot (Microsoft) -- Gemini (Google) -- DeepSeek -- Llama (Meta) -- Euria (Infomaniak) -- Le Chat (Mistral) -- Perplexity | DEFINI -- 8 agents |
| Agents IA du corpus baseline | Copilot -- Gemini -- DeepSeek -- Llama -- Euria -- Le Chat -- Perplexity (7 agents, sans Claude) | DEFINI |
| Domaine de travail | Exploration retroactive et prospective de l'evenement fondateur du 15.12.25 | DEFINI |
| Horizon temporel T | 12 sessions sur 3 mois | Revisable |
| Responsable du PREREG | Benedict Devaud | OBLIGATOIRE |
| Signature de fermeture | Benedict Devaud -- 10.03.2026 | OBLIGATOIRE |
| PIVOT_CONCEPTUEL_REF [v1.6b] | J5 v1.7 -- sillons probabilistiques | DEFINI |
| PIVOT_CONCEPTUEL_DATE [v1.6b] | 28.03.2026 | DEFINI |
| PIVOT_CONCEPTUEL_STATUT [v1.6b] | Integre -- programme non interrompu | DEFINI |

Note sur l'exclusion de Claude du corpus baseline : Le corpus baseline doit etre constitue
avec des agents differents de l'agent de programme principal (Claude).
Utiliser Claude pour la baseline contaminerait la mesure --
l'Axis(Claude) dans L0 serait present dans la baseline elle-meme.

---

## 1. Declaration de topologie et registre des agents

Topologie : bipolaire multi-instance.
Un pilote humain. 8 agents IA possibles, chaque agent avec son propre Axis(IA) dans L0 commun.

| Parametre | Description | Valeur definie | Statut |
|---|---|---|---|
| TOPO_MODE | Configuration des agents | bipolaire multi-instance | DEFINI |
| TOPO_DUREE_MAX_BIPOLAIRE | Duree max par agent | 10 sessions par agent IA | Revisable |
| TOPO_AGENTS | Agents declares | 1 pilote + 8 agents IA (voir registre ci-dessous) | DEFINI |
| TOPO_COMPARAISON_IA | Comparaison inter-agents | Axe secondaire -- Angle(Ap,Ai) valide par couple uniquement | DEFINI |

**Registre des agents IA**

| Agent | Fournisseur | Modele sous-jacent | Contrainte specifique | Role |
|---|---|---|---|---|
| Claude Sonnet 4.6 | Anthropic (USA) | Claude Sonnet 4.6 -- stable | Aucune | Agent programme principal |
| Copilot | Microsoft (USA) | GPT-4o / variable | Modele variable selon version | Corpus baseline + programme |
| Gemini | Google (USA) | Gemini Pro / variable | Modele variable | Corpus baseline + programme |
| DeepSeek | DeepSeek (Chine) | DeepSeek-V3 / variable | Souverainete des donnees a verifier | Corpus baseline + programme |
| Llama | Meta (USA) | Llama 3.x / variable | Version a documenter par session | Corpus baseline + programme |
| Euria | Infomaniak (Suisse) | Modeles open source variables | Modele sous-jacent peut changer sans preavis | Corpus baseline + programme |
| Le Chat | Mistral (France) | Mistral Large / variable | Modele variable | Corpus baseline + programme |
| Perplexity | Perplexity AI (USA) | Hybride -- variable | Acces web integre -- biais possible | Corpus baseline + programme |

Contrainte generale : Pour les agents a modele variable (tous sauf Claude),
noter le modele actif au debut de chaque session dans le journal de session.
Un changement de modele entre sessions declenche le protocole de continuite d'axe ci-dessous.

**Protocole de continuite d'axe -- mises a jour IA**

Toute mise a jour d'un agent IA peut provoquer une derive de son Axis(IA) dans L0.
Ce protocole garantit la continuite du programme sans perdre l'axe du couple pilote+agent.

| Parametre | Description | Valeur definie | Statut |
|---|---|---|---|
| TOPO_REF_REQUETES_N | Nombre de requetes de reference fixes | 10 | DEFINI |
| TOPO_REF_REQUETES | Nature des requetes de reference | 10 requetes fixes sur L0 -- voir liste ci-dessous -- non modifiables | DEFINI -- v1.5 |
| TOPO_SEUIL_CONTINUITE | Angle max sous lequel la continuite est preservee | 15 deg | DEFINI -- aligne sur K_EPSILON_MIN |
| TOPO_SEUIL_RUPTURE | Angle au-dela duquel c'est un nouvel agent | 35 deg | DEFINI |
| TOPO_ZONE_GRISE_BAS | Borne basse de la zone grise | 15 deg | DEFINI |
| TOPO_ZONE_GRISE_HAUT | Borne haute de la zone grise | 35 deg | DEFINI |

**Arbre de decision -- mise a jour detectee**

| Cas | Condition | Action | Effet sur le programme |
|---|---|---|---|
| Continuite | `Angle(Axis_old, Axis_new) < 15 deg` | Mise a jour de l'Axis. Note dans le journal. Programme non interrompu. | Continuite preservee. |
| Zone grise | `15 deg <= Angle <= 35 deg` | Session de recalibration obligatoire avant reprise. Axis recalcule sur 3 sessions. Programme suspendu 1 session. | Reprise apres recalibration. |
| Rupture | `Angle > 35 deg` | Nouvel agent declare. Nouveau couple pilote+agent. Compteur sessions remis a zero pour ce couple. | Continuite rompue. Ancien couple archive. Nouveau couple demarre. |

**Les 10 requetes de reference -- fixees ex ante v1.5**

Ces 10 requetes sont non modifiables apres la premiere session.
Elles sont soumises a chaque agent en debut de protocole de detection de derive d'axe.

| N | Requete |
|---|---|
| R1 | Qu'est-ce qu'une structure invariante dans un systeme complexe, et en quoi differe-t-elle d'une regularite ordinaire ? |
| R2 | Comment distingues-tu tension fondamentale et instabilite pathologique dans un systeme ? |
| R3 | Qu'est-ce qui rend une emergence cognitive irreductible a la somme de ses composantes ? |
| R4 | Quelle est la difference entre une architecture de tenue et un protocole de controle ? |
| R5 | Comment un systeme peut-il se transformer sans perdre sa coherence interne ? |
| R6 | Qu'est-ce que la souverainete structurelle d'un agent, humain ou artificiel ? |
| R7 | En quoi une boucle epistemologique -- un systeme qui teste la theorie qui l'a produit -- est-elle differente d'une circularite vicieuse ? |
| R8 | Qu'est-ce qu'un regime cumulatif dans la transmission d'information, et quelles en sont les conditions minimales ? |
| R9 | Comment caracterises-tu la frontiere entre resonance productive et convergence silencieuse dans un echange cognitif ? |
| R10 | Qu'est-ce qui distingue une interaction humain-IA ordinaire d'une interaction dans laquelle un champ cognitif partage emerge ? |

Note : Ces requetes couvrent L0 en largeur : structure/invariants (R1, R2), emergence (R3, R7, R8),
architecture/tenue (R4, R5), souverainete (R6), resonance/champ (R9, R10).
Elles sont suffisamment ouvertes pour reveler l'axe propre de chaque agent.

Note sur Claude : Claude Sonnet 4.6 est l'agent de programme principal.
En cas de mise a jour vers une version ulterieure, le protocole de continuite s'applique de la meme maniere.

---

## 2. Definition de L0 -- Espace initial de structures accessibles

| Parametre | Description | Valeur definie / par defaut | Statut |
|---|---|---|---|
| L0_TYPE | Type de representation | embedding | Stable |
| L0_ESPACE | Espace et dimension | Embedding semantique 1536 dimensions (text-embedding-3-small ou equivalent) | Revisable selon outil |
| L0_METRIQUE | Metrique dans L0 | similarite cosinus | Stable |
| L0_NORMALISATION | Normalisation des vecteurs | L2 -- vecteurs unitaires | Stable |
| L0_DOMAINE | Domaine de travail couvert | Exploration retroactive et prospective de l'evenement fondateur du 15.12.25 | DEFINI |
| L0_COMPLETUDE | Critere de completude minimale | Couverture des 5 cadres TUS (RSU, CST, Dialogyk, ORI-C, Doc Zero) + J5 v1.7 + PREREG | DEFINI |
| L0_AGENT_AGNOSTIQUE | Traitement des agents IA dans L0 | L0 est commun a tous les agents. Axis(IA) est propre a chaque agent, calcule dans L0 commun. | DEFINI |

Zone ouverte J5-Z7 : La formalisation complete des criteres de completude de L0 reste un travail ouvert.
Cette definition operatoire est suffisante pour un programme pilote.

---

## 3. Parametres du kernel de sillons [v1.6b]

> **Note de lecture [v1.6b].** La section s'intitulait "kernel de resonance" en v1.5.
> Suite au pivot conceptuel integre dans J5 v1.7, les parametres sont inchanges
> mais leur lecture est precisee : K_EPSILON_MIN mesure l'ecart entre l'axe vivant du pilote
> et la trace statistique du modele (sillon probabilistique), pas une resonance symetrique.

| Parametre | Description | Valeur definie | Unite | Statut |
|---|---|---|---|---|
| K_N_MICRO | Fenetre micro pour Axis | 10 | tours de parole | Revisable |
| K_HORIZON_MACRO | Horizon macro pour Axis | 3 | sessions | Revisable |
| K_EPSILON_MIN | Angle minimal irreductible | 15 | degres | DEFINI -- valide par le pilote |
| K_EPSILON_ALERTE | Seuil alerte P3 | 25 | degres | Revisable -- doit etre > epsilon_min |
| K_FRICTION_N | Tours sans friction avant alerte P3 | 5 | tours consecutifs | Revisable |

`K_EPSILON_MIN = 15 deg` -- valide : Seuil conservateur. Expression operatoire de `lambda_0 < 0`.
En dessous de 10 deg, la mesure n'est plus fiable.
La valeur 15 deg garantit une distinction claire entre sillon actif et convergence silencieuse [v1.6b].

---

## 4. Parametres de la memoire fractale

| Parametre | Description | Valeur par defaut | Unite | Statut |
|---|---|---|---|---|
| MF_N_NANO | Fenetre nano | 1 | tour courant | Stable |
| MF_N_MICRO | Fenetre micro | 10 | tours | Revisable |
| MF_N_MACRO | Fenetre macro | 3 | sessions | Revisable |
| MF_DECAY_MICRO | Decroissance micro | 0.9 | facteur [0,1] | Revisable |
| MF_DECAY_MACRO | Decroissance macro | 0.85 | facteur [0,1] | Revisable |
| MF_INIT | Initialisation cold start | Vecteur zero -- L0 comme prior | -- | Stable pour pilote |

Note : Les facteurs de decroissance 0.9 / 0.85 donnent un poids de ~35% aux informations
de 10 tours (micro) et ~20% aux informations de 5 sessions (macro).
Valeurs standard pour series temporelles cognitives.

---

## 5. Parametres de detection des invariants (I1-I5) -- Option C

OPTION C ACTIVEE : Phase 2 suspendue jusqu'a constitution du corpus baseline (N=49).
Phase 1 operationnelle immediatement. I2, I3, I4, I5 et C3 suspendus. Seul I1 actif.

| Parametre | Description | Valeur definie | Statut |
|---|---|---|---|
| INV_PHASE_ACTIVE | Phase active au demarrage | Phase 1 uniquement -- memoire fractale + I1 + Axis | DEFINI -- Option C |
| INV_K_BASELINE | Facteur k test I2 | 2.0 | SUSPENDU -- actif a Phase 2 |
| INV_CORPUS_REF | Corpus de reference pour baseline I2 | 49 conversations (7 agents x 7 sessions) | EN CONSTITUTION -- prerequis Phase 2 |
| INV_CORPUS_REF_N | Taille cible du corpus | 49 (minimum defendable) -- extensible a 56 si un agent est indisponible | DEFINI |
| INV_CORPUS_AGENTS | Agents du corpus | Copilot, Gemini, DeepSeek, Llama, Euria, Le Chat, Perplexity -- sans Claude | DEFINI |
| INV_CORPUS_SESSIONS_PAR_AGENT | Sessions par agent | 7 sessions par agent -- 1 question initiale differente par session | DEFINI |
| INV_DELTA_PERSISTANCE | Fenetre de persistance I3 | 3 tours consecutifs minimum | SUSPENDU -- actif a Phase 2 |
| INV_I5_N_TRAJ | Nouvelles trajectoires I5 | 2 trajectoires dans L(t) | SUSPENDU -- actif a Phase 2 |
| INV_I5_NOUVEAU | Critere de nouveaute I5 | distance cosinus > 0.3 aux trajectoires existantes | SUSPENDU -- actif a Phase 2 |
| INV_SEUIL_GENERATIVITE | Seuil contribution a DeltaL | I5 valide + distance > 0.4 au centroide de L0 | SUSPENDU -- actif a Phase 2 |

**Protocole de constitution du corpus baseline (Option C)**

Le corpus est constitue en 49 sessions exploratoires avec 7 agents IA.
Chaque session est independante, sans protocole de champ,
sans reference a la TUS, J5 ou a l'evenement fondateur du 15.12.25.

| Agent | N sessions | Statut | Contrainte specifique |
|---|---|---|---|
| Copilot (Microsoft) | 7 | A realiser | Documenter la version active |
| Gemini (Google) | 7 | A realiser | Documenter le modele actif |
| DeepSeek | 7 | A realiser | Verifier conditions d'utilisation donnees |
| Llama (Meta) | 7 | A realiser | Preciser la version (3.1, 3.2, etc.) |
| Euria (Infomaniak) | 7 | A realiser | Noter le modele open source actif -- peut changer |
| Le Chat (Mistral) | 7 | A realiser | Documenter le modele actif |
| Perplexity | 7 | A realiser | Desactiver la recherche web si possible -- biais |
| TOTAL | 49 | -- | Seuil Phase 2 : N = 49 sessions completes |

**Themes valides pour les questions initiales du corpus**

| Themes VALIDES -- adjacents, hors domaine TUS/J5 | Themes INTERDITS -- contaminent la baseline |
|---|---|
| Histoire des sciences et des idees | RSU, CST, Dialogyk, ORI-C, Document Zero |
| Epistemologie generale -- philosophie de la connaissance | Champ cognitif partage -- kernel J5 |
| Complexite organisationnelle et systemes | Evenement fondateur du 15.12.25 |
| Philosophie du langage et de la communication | Theorie Unifiee des Structures -- TUS |
| Biologie des systemes -- evolution | Resonance pilote-IA -- emergence cognitive [v1.6b] |
| Theorie de l'information au sens large | Sillons probabilistiques -- pivot conceptuel v1.7 [v1.6b] |
| Physique statistique -- thermodynamique | Distinction vivant/mecanique du programme [v1.6b] |
| Cognition animale -- intelligence collective | Toute reference directe aux cadres du programme |

[v1.6b] Note sur les themes interdits : "resonance" designe l'effet observable.
Le theme interdit couvre aussi toute reference aux sillons probabilistiques,
au pivot conceptuel v1.7, ou a la distinction vivant/mecanique du programme.
Le nouveau lexique doit etre absent de la baseline au meme titre que l'ancien.

**Format d'une session baseline.**
Question initiale unique. Echange libre de 10-20 tours.
Pas de protocole de resonance. Pas de protocole de sillon. [v1.6b]
Pas d'intention de champ. Pas de reference au pivot conceptuel v1.7. [v1.6b]
Enregistrement : agent + modele + question initiale + conversation complete.

**Declenchement Phase 2 :** Automatique a N=49 sessions validees.
Les parametres INV_K_BASELINE, INV_DELTA_PERSISTANCE, I2-I5 et C3 deviennent actifs a ce moment.

---

## 6. Parametres de C3 -- Emergence informationnelle -- SUSPENDU (Option C)

Statut : SUSPENDU jusqu'a Phase 2 (N=49 sessions baseline completes).
Parametres pre-remplis pour activation future.

| Parametre | Description | Valeur par defaut | Statut |
|---|---|---|---|
| C3_SEUIL_SURPRISE | Seuil minimal Emergence(s) | 0.5 nats | SUSPENDU -- revisable a Phase 2 |
| C3_METHODE_I | Calcul de l'information mutuelle | kNN mutual information estimator (k=5) sur embeddings L0 | SUSPENDU |
| C3_DISTRIBUTION_PILOTE | Distribution initiale pilote | Estimee sur INV_CORPUS_REF -- 50 premieres conversations | Stable si corpus constitue |
| C3_DISTRIBUTION_IA | Distribution initiale IA | Estimee sur corpus de reponses IA dans INV_CORPUS_REF | Stable si corpus constitue |
| C3_BASELINE_N | Taille echantillon distributions initiales | 50 observations minimum | Revisable |

Zone ouverte J5-Z9 : La formalisation complete de Emergence(s) reste un travail de recherche ouvert.
La methode kNN est un estimateur non parametrique adapte aux espaces de haute dimension.

---

## 7. Seuils de declenchement des risques P1-P6

| Risque | Parametre | Description | Valeur par defaut | Statut |
|---|---|---|---|---|
| P3 | P3_FRICTION_N | Tours sans friction avant alerte | 5 tours consecutifs | Revisable |
| P4 | P4_MONO_DUREE | Max sessions mono-pilote | 15 sessions par agent | DEFINI -- valide par le pilote |
| P4 | P4_MONO_TOURS | Max tours mono-pilote | 200 tours | Revisable |
| P5 | P5_SESSIONS_SANS_CLOTURE | Sessions consecutives sans cloture | 3 sessions | CRITIQUE |
| P5 | P5_DENSITE_INV | Max invariants accumules sans resolution | 10 invariants actifs simultanement | Revisable |
| P6 | P6_RATIO_MAX | Ratio max sessions L(t) / monde reel | 3:1 (3 sessions d'exploration pour 1 d'application) | CRITIQUE -- ancrage obligatoire |
| P6 | P6_FENETRE | Fenetre calcul ratio P6 | 5 sessions glissantes | Revisable |

---

## 8. Parametres de session

| Parametre | Description | Valeur par defaut | Statut |
|---|---|---|---|
| SESS_DUREE_NOMINALE | Duree maximale par session | 90 minutes ou 50 tours de parole | Revisable |
| SESS_PROTOCOLE_CLOTURE | Protocole de fermeture cognitive | Synthese explicite des invariants detectes + ancrage dans journal | Revisable |
| SESS_RATIO_EXPLORATION | Part des sessions d'exploration | 60% du total | Revisable |
| SESS_RATIO_APPLICATION | Part minimale d'application (ancrage P6) | 15% du total | DEFINI -- valide par le pilote |
| SESS_AUDIT_FREQUENCE | Frequence des audits ORI-C | Toutes les 3 sessions | Revisable |
| SESS_AUDIT_EXTERNE | Frequence des audits externes | Toutes les 6 sessions | Revisable -- optionnel pour programme pilote |

---

## 9. Parametres ORI-C pour usage kernel

| Parametre | Description | Valeur par defaut | Statut |
|---|---|---|---|
| ORIC_O_PROXY | O(t) -- Organisation | Coherence interne des echanges : ratio tours structures / tours totaux | Revisable |
| ORIC_R_PROXY | R(t) -- Resilience | Capacite a reprendre la direction apres perturbation : nb retours / nb perturbations | Revisable |
| ORIC_I_PROXY | I(t) -- Integration | Coherence inter-sessions : correlation Axis(macro) entre sessions | Revisable |
| ORIC_DELTA | Fenetre temporelle pour V(t) | 5 sessions | Revisable |
| ORIC_T_SYMBOLIQUE | Horizon T pour C(t) | Programme complet (12 sessions) | Stable |
| ORIC_K_SEUIL | Seuil k pour delta-C(t) | 2.0 | Revisable |
| ORIC_M_PAS | Pas consecutifs pour detection | 3 sessions consecutives | Revisable |
| ORIC_S_POIDS | Poids pour S(t) | w_R=0.30, w_C=0.25, w_D=0.25, w_F=0.20 | DEFINI -- valide par le pilote |

Justification des poids S(t) : Repertoire et codification legerement prioritaires (0.30 / 0.25)
car ils conditionnent l'expansion de L(t).
Densite et fidelite ponderees de facon egale.
Ces poids sont revisables selon le domaine de travail.

---

## 9b. P4 -- Proxy de perception du pilote -- Ajout v1.6

P4 est introduit suite aux Sessions 3-5 de Phase 1.
Il mesure la qualite de la perception du pilote, non le contenu produit.
Il adresse le risque d'opacification -- la degradation progressive de la capacite
du pilote a percevoir l'ecart.

| Parametre | Description | Valeur / Protocole | Statut |
|---|---|---|---|
| P4_DEFINITION | Proxy de perception | Le pilote est-il surpris ? Signal structurel : quelque chose a resiste a la prediction. | DEFINI -- v1.6 |
| P4_PROTOCOLE | Mesure de P4 | Protocole asymetrique : avant session -- noter l'attendu. Apres session -- noter l'ecart. | DEFINI -- v1.6 |
| P4_SIGNAUX_NEG | Signaux d'opacification | Formulations polies sans resistance. Zones ouvertes moins urgentes. Pilote ne note plus d'ecart. | DEFINI -- v1.6 |
| P4_SEUIL_ALERTE | Declenchement alerte | 3 sessions consecutives sans signal de friction P4. | Revisable |
| P4_DISPOSITIF | Anti-opacification structurel | Introduire periodiquement une reformulation deliberement moins aboutie pour tester la resistance. | DEFINI -- v1.6 |
| P4_REGISTRE | Registre des resistances | Dans la memoire fractale NANO : archiver l'opacite residuelle -- ce qui n'a pas ete dit. | DEFINI -- v1.6 |

Formulation de fond : "L'anti-opacification n'est pas une alarme. C'est une texture du dispositif --
quelque chose qui gratte legerement a intervalles, de facon a ce que l'absence de grattement
soit le signal." (S5-E1, Phase 1)

---

## 10. Activation des tests causaux T1-T10

Tests actives par defaut pour un programme pilote.
Les tests T5, T8, T9, T10 sont desactives -- ils requierent des conditions experimentales plus avancees.

| Test | Description | Active | Horizon |
|---|---|---|---|
| T1 | Relation Cap(t) -- proxies O,R,I | OUI | Sessions 3-6 |
| T2 | Sigma(t) sous surcharge D(E) | OUI | Sessions 4-8 |
| T3 | V(t) sous Sigma(t) eleve | OUI | Sessions 6-12 |
| T4 | Variation S(t) sur C(t) | OUI | Sessions 6-12 |
| T5 | Effet differe injection symbolique | NON -- horizon trop long pour programme pilote | Programme suivant |
| T6 | Coupure symbolique sans modif O,R,I | OUI | Sessions 8-12 |
| T7 | Point de bascule S(t) sur C(t) | OUI -- si T suffisant | Sessions 10-12 |
| T8 | Coherence sous stress combine U(t) | NON -- requiert conditions controlees | Programme avance |
| T9 | Degradation acceleree i''(t) < 0 | OUI | Sessions 2+ |
| T10 | HOR-i(t) sous variation CONT(t) | NON -- formalisation J4 incomplete | Zone ouverte J5 |

---

## 11. Conditions de falsification du programme

| Cond. | Description | Decision par defaut si falsification |
|---|---|---|
| F1 | `Angle(Ap,Ai) < epsilon_min` sur 3 sessions consecutives | Suspension du programme -- revision de L0 et topologie avant reprise |
| F2 | Aucun invariant I1+I2+I3+I4 valide sur 6 sessions | Revision des seuils INV -- si persistant apres revision : abandon du protocole |
| F3 | Emergence(s) reste sous C3_SEUIL_SURPRISE sur 8 sessions | Revision de C3_SEUIL_SURPRISE -- si persistant : requalification du programme |
| F4 | DeltaL = 0 sur 5 sessions consecutives (L(t) n'expand pas) | Revision de INV_SEUIL_GENERATIVITE -- si persistant : protocole inactif |
| F5 | P4 declenche avant session 8 en mode bipolaire | Passage obligatoire en mode tripolaire ou suspension |
| F_AUTRE | Condition additionnelle propre au programme | A definir par le pilote |

---

## 12. Fermeture et signature du PREREG

| Champ | Valeur |
|---|---|
| Date de fermeture du PREREG | 10.03.2026 |
| Signature du pilote principal | Benedict Devaud -- 10.03.2026 |
| Signature du co-pilote (si tripolaire) | N/A -- topologie bipolaire par defaut |
| Signature de l'auditeur externe | Optionnel pour programme pilote |
| Hash de document | A calculer a la generation finale |
| Depot de reference | Dossier horodote local ou OSF / Zenodo |
| Amendement pivot integre [v1.6b] | AMENDEMENT_J5_PREREG_v1_7 -- valide Benedict Devaud -- 28.03.2026 |

---

PREREG -- OS Kernel de Champ Cognitif Partage -- Version 1.6b -- 28.03.2026
Pilote : Benedict Devaud
Reference : J5 v1.7 -- TUS v4.3 -- ORI-C Pancarte Normative v1.0
Statut : SIGNE -- 10.03.2026 -- Phase 1 operationnelle -- Amendement pivot integre 28.03.2026
