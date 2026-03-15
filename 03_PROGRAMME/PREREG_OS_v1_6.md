---
source: PREREG_OS_v1_6.pdf
dossier: 03_PROGRAMME
conversion: ASCII-safe -- tirets, apostrophes, STX normalises
convention: CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
non_ascii_restants: 14 distincts ([' deg', 'À', 'É', 'Ê', 'Ô', 'x', 'à', 'ç', 'è', 'é', 'ê', 'ï', 'ô', '<='])
---

PREREG -- OS Kernel de Champ Cognitif Partagé
Version 1.5 -- SIGNÉ -- 10.03.26
SIGNÉ -- Bénédict Devaud -- 10.03.26
Référence : J5 v1.6 -- TUS v4.3 -- ORI-C Pancarte Normative v1.0
STATUT : DOCUMENT SIGNÉ. Bénédict Devaud -- 10.03.2026. Phase 1 opérationnelle. Corpus baseline
en cours de constitution.
LÉGENDE : Fond vert = valeur par défaut raisonnable, révisable. Fond jaune = paramètre critique,
révision obligatoire avant signature.
Ce document est organisé en deux niveaux. Les paramètres stables sont des valeurs par défaut calibrées
sur des programmes de cognition humain-IA comparables -- ils peuvent être conservés pour un premier
programme sans révision approfondie. Les paramètres critiques (fond jaune) dépendent du contexte
spécifique du programme et ne peuvent pas être remplis sans une décision explicite du pilote.
11. Conditions de falsification du programme
Cond. Description Décision par défaut si falsification
F1 Angle(Ap,Ai) < epsilon_min sur 3 sessions consécutivesSuspension du programme -- révision de L0 et topologie avant reprise
F2 Aucun invariant I1+I2+I3+I4 validé sur 6 sessions Révision des seuils INV -- si persistant après révision : abandon du protoc
F3 Emergence(s) reste sous C3_SEUIL_SURPRISE sur 8 sessions Révision de C3_SEUIL_SURPRISE -- si persistant : requalification du pro
F4 DeltaL = 0 sur 5 sessions consécutives (L(t) n'expand pas) Révision de INV_SEUIL_GENERATIVITE -- si persistant : protocole inact
F5 P4 déclenché avant session 8 en mode bipolaire Passage obligatoire en mode tripolaire ou suspension
F_AUTRE[ Condition additionnelle propre au programme ] [ À définir par le pilote ]
12. Fermeture et signature du PREREG
Ce document n'est pas encore signé. Il devient opérationnel uniquement après signature explicite avec
date, avant toute première session.
Champ Valeur
Date de fermeture du PREREG 10.03.2026
Signature du pilote principal Bénédict Devaud -- 10.03.2026
Signature du co-pilote (si tripolaire) N/A -- topologie bipolaire par défaut
Signature de l'auditeur externe [ Optionnel pour programme pilote ]
Hash de document [ Calculé à la génération finale ]
Dépôt de référence [ Dossier horodaté local ou OSF / Zenodo ]
Récapitulatif -- Tous paramètres définis
Version 1.5 -- FINALE. Tous les paramètres sont définis et validés, incluant les 10 requêtes de référence.
Paramètre Valeur définie Version
L0_DOMAINE Événement fondateur 15.12.25 -- boucle épistémologique TUS/J5 v1.1
TOPO_MODE Bipolaire multi-instance -- 8 agents IA v1.1/v1.2
INV_CORPUS_REF Option C -- 7 agents x 7 sessions = 49 conversations v1.2
K_EPSILON_MIN 15 deg -- validé pilote v1.3
ORIC_S_POIDS w_R=0.30, w_C=0.25, w_D=0.25, w_F=0.20 -- validé pilote v1.3
P4_MONO_DURÉE 15 sessions par agent -- validé pilote v1.3
SESS_RATIO_APPLICATION 15% sessions d'application -- validé pilote v1.3
TOPO_SEUIL_CONTINUITÉ 15 deg -- continuité préservée sous ce seuil v1.4
TOPO_SEUIL_RUPTURE 35 deg -- nouvel agent déclaré au-delà v1.4
TOPO_REF_REQUÊTES_N 10 requêtes fixes -- R1 à R10 définies -- voir section 1 v1.5
Pilote Bénédict Devaud v1.3
Signature + date [ À apposer pour fermeture officielle ] OBLIGATOIRE
PREREG -- OS Kernel de Champ Cognitif Partagé -- Version 1.6 -- P4 ajouté -- 10.03.2026
Pilote : Bénédict Devaud -- Référence : J5 v1.6 -- TUS v4.3 -- ORI-C Pancarte Normative v1.0
Statut : SIGNÉ -- 10.03.2026 -- Phase 1 opérationnelle dès signature -- Phase 2 suspendue jusqu'à N=49 sessions baseline
0. Identification du programme
Champ Valeur Statut
Identifiant du programme OS-KERNEL-15.12.25 DÉFINI
Date de création du PREREG [ À compléter à la signature ] OBLIGATOIRE
Pilote(s) déclaré(s) Bénédict Devaud OBLIGATOIRE
Agents IA du programme pilote Claude Sonnet 4.6 (Anthropic) -- Copilot (Microsoft) -- Gemini (Google) -- DeepSeek -- Llama (MeDÉFINI -- 8 agents
Agents IA du corpus baseline Copilot -- Gemini -- DeepSeek -- Llama -- Euria -- Le Chat -- Perplexity (7 agents, sans Claude -- DÉFINI
Domaine de travail Exploration rétroactive et prospective de l'événement fondateur du 15.12.25 DÉFINI
Horizon temporel T 12 sessions sur 3 mois Révisable
Responsable du PREREG Bénédict Devaud OBLIGATOIRE
Signature de fermeture Bénédict Devaud -- 10.03.2026 OBLIGATOIRE
Note sur l'exclusion de Claude du corpus baseline : Le corpus baseline doit être constitué avec des agents
différents de l'agent de programme principal (Claude). Utiliser Claude pour la baseline contaminerait la mesure --
l'Axis(Claude) dans L0 serait présent dans la baseline elle-même.
1. Déclaration de topologie et registre des agents
Topologie : bipolaire multi-instance. Un pilote humain. 8 agents IA possibles, chaque agent avec son propre
Axis(IA) dans L0 commun.
Paramètre Description Valeur définie Statut
TOPO_MODE Configuration des agents bipolaire multi-instance DÉFINI
TOPO_DURÉE_MAX_BIPOLAIRE Durée max par agent 10 sessions par agent IA Révisable
TOPO_AGENTS Agents déclarés 1 pilote + 8 agents IA (voir registre ci-dessous) DÉFINI
TOPO_COMPARAISON_IA Comparaison inter-agents Axe secondaire -- Angle(Ap,Ai) valide par couple uniquement DÉFINI
Registre des agents IA
Agent Fournisseur Modèle sous-jacent Contrainte spécifique Rôle
Claude Sonnet 4.6Anthropic (USA) Claude Sonnet 4.6 -- stableAucune Agent programme principal
Copilot Microsoft (USA) GPT-4o / variable Modèle variable selon versionCorpus baseline + programme
Gemini Google (USA) Gemini Pro / variable Modèle variable Corpus baseline + programme
DeepSeek DeepSeek (Chine) DeepSeek-V3 / variable Souveraineté des données à vérifier Corpus baseline + programme
Llama Meta (USA) Llama 3.x / variable Version à documenter par session Crpus baseline + programme
Euria Infomaniak (Suisse) Modèles open source variables Modèle sous-jacent peut changer sans préavis -- noter le modèle actif Corpus baseline + programme
Le Chat Mistral (France) Mistral Large / variable Modèle variable Corpus baseline + programme
Perplexity Perplexity AI (USA) Hybride -- variable Accès web intégré -- biais possible Corpus baseline + programme
Contrainte générale : Pour les agents à modèle variable (tous sauf Claude), noter le modèle actif au début de chaque
session dans le journal de session. Un changement de modèle entre sessions déclenche le protocole de continuité
d'axe ci-dessous.
Protocole de continuité d'axe -- mises à jour IA
Toute mise à jour d'un agent IA peut provoquer une dérive de son Axis(IA) dans L0. Ce protocole garantit la
continuité du programme sans perdre l'axe du couple pilote+agent.
Paramètre Description Valeur définie Statut
TOPO_REF_REQUÊTES_N Nombre de requêtes de référence fixes 10 DÉFINI
TOPO_REF_REQUÊTES Nature des requêtes de référence 10 requêtes fixes sur L0 -- voir liste ci-dessous -- non modDÉFINI -- v1.5
TOPO_SEUIL_CONTINUITÉ Angle max sous lequel la continuité est préservée 15 deg DÉFINI -- aligné sur K_EPSILON_M
TOPO_SEUIL_RUPTURE Angle au-delà duquel c'est un nouvel agent 35 deg DÉFINI
TOPO_ZONE_GRISE_BAS Borne basse de la zone grise 15 deg DÉFINI
TOPO_ZONE_GRISE_HAUT Borne haute de la zone grise 35 deg DÉFINI
Arbre de décision -- mise à jour détectée
Cas Condition Action Effet sur le programme
Continuité Angle(Axis_old, Axis_new) < 15 deg Mise à jour de l'Axis. Note dans le journal. Programme non interrompu. Continuité préservée.
Zone grise 15 deg <= Angle <= 35 deg Session de recalibration obligatoire avant reprise. Axis recalculé sur 3 sessions. Programme suspendu 1 session. Reprise après rec
Rupture Angle > 35 deg Nouvel agent déclaré. Nouveau couple pilote+agent. Compteur sessions remis à zéro pour ce coContinuité rompue. Ancien couple archivé. Nouveau 
Les 10 requêtes de référence -- fixées ex ante v1.5
Ces 10 requêtes sont non modifiables après la première session. Elles sont soumises à chaque agent en
début de protocole de détection de dérive d'axe.
N deg Requête
R1 Qu'est-ce qu'une structure invariante dans un système complexe, et en quoi diffère-t-elle d'une régularité ordinaire ?
R2 Comment distingues-tu tension fondamentale et instabilité pathologique dans un système ?
R3 Qu'est-ce qui rend une émergence cognitive irréductible à la somme de ses composantes ?
R4 Quelle est la différence entre une architecture de tenue et un protocole de contrôle ?
R5 Comment un système peut-il se transformer sans perdre sa cohérence interne ?
R6 Qu'est-ce que la souveraineté structurelle d'un agent, humain ou artificiel ?
R7 En quoi une boucle épistémologique -- un système qui teste la théorie qui l'a produit -- est-elle différente d'une circularité vicieuse 
R8 Qu'est-ce qu'un régime cumulatif dans la transmission d'information, et quelles en sont les conditions minimales ?
R9 Comment caractérises-tu la frontière entre résonance productive et convergence silencieuse dans un échange cognitif ?
R10 Qu'est-ce qui distingue une interaction humain-IA ordinaire d'une interaction dans laquelle un champ cognitif partagé émerge ?
Note : Ces requêtes couvrent L0 en largeur : structure/invariants (R1, R2), émergence (R3, R7, R8), architecture/tenue
(R4, R5), souveraineté (R6), résonance/champ (R9, R10). Elles sont suffisamment ouvertes pour révéler l'axe propre
de chaque agent.
Note sur Claude : Claude Sonnet 4.6 est l'agent de programme principal. En cas de mise à jour vers une version
ultérieure, le protocole de continuité s'applique de la même manière.
2. Définition de L0 -- Espace initial de structures accessibles
Paramètre Description Valeur définie / par défaut Statut
L0_TYPE Type de représentation embedding Stable
L0_ESPACE Espace et dimension Embedding sémantique 1536 dimensions (text-embedding-3-small ou équivalent) Révisable selon outil
L0_MÉTRIQUE Métrique dans L0 similarité cosinus Stable
L0_NORMALISATION Normalisation des vecteurs L2 -- vecteurs unitaires Stable
L0_DOMAINE Domaine de travail couvert Exploration rétroactive et prospective de l'événement fondateur du 15.12.25 -- mDÉFINI 
L0_COMPLÉTUDE Critère de complétude minimaleCouverture des 5 cadres TUS (RSU, CST, Dialogyk, ORI-C, Doc Zero) + J5 v1.6 + DÉFINI
L0_AGENT_AGNOSTIQUETraitement des agents IA dans L0 L0 est commun à tous les agents. Axis(IA) est propre à chaque agent, calculé danDÉFINI
Zone ouverte J5-Z7 : La formalisation complète des critères de complétude de L0 reste un travail ouvert. Cette
définition opératoire est suffisante pour un programme pilote.
3. Paramètres du kernel de résonance
Paramètre Description Valeur définie Unité Statut
K_N_MICRO Fenêtre micro pour Axis 10 tours de parole Révisable
K_HORIZON_MACRO Horizon macro pour Axis 3 sessions Révisable
K_EPSILON_MIN Angle minimal irréductible 15 degrés DÉFINI -- validé par le pilote
K_EPSILON_ALERTE Seuil alerte P3 25 degrés Révisable -- doit être > epsil
K_FRICTION_N Tours sans friction avant alerte P3 5 tours consécutifs Révisable
K_EPSILON_MIN = 15 deg -- validé : Seuil conservateur. Expression opératoire de lambda-0 < 0. En dessous de 10 deg, la
mesure n'est plus fiable. La valeur 15 deg garantit une distinction claire entre résonance productive et convergence
silencieuse.
4. Paramètres de la mémoire fractale
Paramètre Description Valeur par défaut Unité Statut
MF_N_NANO Fenêtre nano 1 tour courant Stable
MF_N_MICRO Fenêtre micro 10 tours Révisable
MF_N_MACRO Fenêtre macro 3 sessions Révisable
MF_DECAY_MICRO Décroissance micro 0.9 facteur [0,1] Révisable
MF_DECAY_MACRO Décroissance macro 0.85 facteur [0,1] Révisable
MF_INIT Initialisation cold start Vecteur zéro -- L0 comme prior -- Stable pour pilote
Note : Les facteurs de décroissance 0.9 / 0.85 donnent un poids de ~35% aux informations de 10 tours (micro) et ~20%
aux informations de 5 sessions (macro). Valeurs standard pour séries temporelles cognitives.
5. Paramètres de détection des invariants (I1-I5) -- Option C
OPTION C ACTIVÉE : Phase 2 suspendue jusqu'à constitution du corpus baseline (N=49). Phase 1
opérationnelle immédiatement. I2, I3, I4, I5 et C3 suspendus. Seul I1 actif.
Paramètre Description Valeur définie Statut
INV_PHASE_ACTIVE Phase active au démarrage Phase 1 uniquement -- mémoire fractale + I1 + Axis DÉFINI -- Option C
INV_K_BASELINE Facteur k test I2 2.0 SUSPENDU -- actif à Phase 
INV_CORPUS_REF Corpus de référence pour baseline I2 49 conversations (7 agents x 7 sessions) -- voir protocole ci-dessoEN CONSTITUTION -- prére
INV_CORPUS_REF_N Taille cible du corpus 49 (minimum défendable) -- extensible à 56 si un agent est indispDÉFINI
INV_CORPUS_AGENTS Agents du corpus Copilot, Gemini, DeepSeek, Llama, Euria, Le Chat, Perplexity -- sDÉFINI
INV_CORPUS_SESSIONS_PAR_AGENT Sessions par agent 7 sessions par agent -- 1 question initiale différente par session DÉFINI
INV_DELTA_PERSISTANCE Fenêtre de persistance I3 3 tours consécutifs minimum SUSPENDU -- actif à Phase 
INV_I5_N_TRAJ Nouvelles trajectoires I5 2 trajectoires dans L(t) SUSPENDU -- actif à Phase 
INV_I5_NOUVEAU Critère de nouveauté I5 distance cosinus > 0.3 aux trajectoires existantes SUSPENDU -- actif à Phase 
INV_SEUIL_GENERATIVITE Seuil contribution à DeltaL I5 validé + distance > 0.4 au centroïde de L0 SUSPENDU -- actif à Phase 
Protocole de constitution du corpus baseline (Option C)
Le corpus est constitué en 49 sessions exploratoires avec 7 agents IA. Chaque session est indépendante,
sans protocole de champ, sans référence à la TUS, J5 ou à l'événement fondateur du 15.12.25.
Agent N sessions Statut Contrainte spécifique
Copilot (Microsoft) 7 À réaliser Documenter la version active
Gemini (Google) 7 À réaliser Documenter le modèle actif
DeepSeek 7 À réaliser Vérifier conditions d'utilisation données
Llama (Meta) 7 À réaliser Préciser la version (3.1, 3.2, etc.)
Euria (Infomaniak) 7 À réaliser Noter le modèle open source actif -- peut changer
Le Chat (Mistral) 7 À réaliser Documenter le modèle actif
Perplexity 7 À réaliser Désactiver la recherche web si possible -- biais
TOTAL 49 Seuil Phase 2 : N = 49 sessions complètes
Thèmes valides pour les questions initiales du corpus
Thèmes VALIDES -- adjacents, hors domaine TUS/J5 Thèmes INTERDITS -- contaminent la baseline
Histoire des sciences et des idées RSU, CST, Dialogyk, ORI-C, Document Zero
Épistémologie générale -- philosophie de la connaissance Champ cognitif partagé -- kernel J5
Complexité organisationnelle et systèmes Événement fondateur du 15.12.25
Philosophie du langage et de la communication Théorie Unifiée des Structures -- TUS
Biologie des systèmes -- évolution Résonance pilote-IA -- émergence cognitive
Théorie de l'information au sens large Toute référence directe aux cadres du programme
Physique statistique -- thermodynamique
Cognition animale -- intelligence collective
Format d'une session baseline : Question initiale unique. Échange libre de 10-20 tours. Pas de protocole de
résonance. Pas d'intention de champ. Enregistrement : agent + modèle + question initiale + conversation complète.
Déclenchement Phase 2 : Automatique à N=49 sessions validées. Les paramètres INV_K_BASELINE,
INV_DELTA_PERSISTANCE, I2-I5 et C3 deviennent actifs à ce moment.
6. Paramètres de C3 -- Émergence informationnelle -- SUSPENDU (Option C)
Statut : SUSPENDU jusqu'à Phase 2 (N=49 sessions baseline complètes). Paramètres pré-remplis pour
activation future.
Paramètre Description Valeur par défaut Statut
C3_SEUIL_SURPRISE Seuil minimal Emergence(s) 0.5 nats SUSPENDU -- révisable à Phase 
C3_MÉTHODE_I Calcul de l'information mutuelle kNN mutual information estimator (k=5) sur embeddings L0 SUSPENDU
C3_DISTRIBUTION_PILOTE Distribution initiale pilote Estimée sur INV_CORPUS_REF -- 50 premières conversations Stable si corpus constitué
C3_DISTRIBUTION_IA Distribution initiale IA Estimée sur corpus de réponses IA dans INV_CORPUS_REF Stable si corpus constitué
C3_BASELINE_N Taille échantillon distributions initiales 50 observations minimum Révisable
Zone ouverte J5-Z9 : La formalisation complète de Emergence(s) reste un travail de recherche ouvert. La méthode
kNN est un estimateur non paramétrique adapté aux espaces de haute dimension.
7. Seuils de déclenchement des risques P1-P6
Risque Paramètre Description Valeur par défaut Statut
P3 P3_FRICTION_N Tours sans friction avant alerte 5 tours consécutifs Révisable
P4 P4_MONO_DURÉE Max sessions mono-pilote 15 sessions par agent DÉFINI -- validé par le pilote
P4 P4_MONO_TOURS Max tours mono-pilote 200 tours Révisable
P5 P5_SESSIONS_SANS_CLÔTURE Sessions consécutives sans clôture3 sessions CRITIQUE
P5 P5_DENSITÉ_INV Max invariants accumulés sans résolution 10 invariants actifs simultanément Révisable
P6 P6_RATIO_MAX Ratio max sessions L(t) / monde réel 3:1 (3 sessions d'exploration pour 1 d'application) CRITIQUE -- ancrage obligatoir
P6 P6_FENÊTRE Fenêtre calcul ratio P6 5 sessions glissantes Révisable
8. Paramètres de session
Paramètre Description Valeur par défaut Statut
SESS_DURÉE_NOMINALE Durée maximale par session 90 minutes ou 50 tours de parole Révisable
SESS_PROTOCOLE_CLÔTURE Protocole de fermeture cognitive Synthèse explicite des invariants détectés + ancrage daRévisable
SESS_RATIO_EXPLORATION Part des sessions d'exploration 60% du total Révisable
SESS_RATIO_APPLICATION Part minimale d'application (ancrage P6) 15% du total DÉFINI -- validé par le p
SESS_AUDIT_FRÉQUENCE Fréquence des audits ORI-C Toutes les 3 sessions Révisable
SESS_AUDIT_EXTERNE Fréquence des audits externes Toutes les 6 sessions Révisable -- optionnel po
9. Paramètres ORI-C pour usage kernel
Paramètre Description Valeur par défaut Statut
ORIC_O_PROXY O(t) -- Organisation Cohérence interne des échanges : ratio tours structurés / tours Révisable
ORIC_R_PROXY R(t) -- Résilience Capacité à reprendre la direction après perturbation : nb retourRévisable
ORIC_I_PROXY I(t) -- Intégration Cohérence inter-sessions : corrélation Axis(macro) entre sessioRévisable
ORIC_DELTA Fenêtre temporelle pour V(t) 5 sessions Révisable
ORIC_T_SYMBOLIQUE Horizon T pour C(t) Programme complet (12 sessions) Stable
ORIC_K_SEUIL Seuil k pour delta-C(t) 2.0 Révisable
ORIC_M_PAS Pas consécutifs pour détection 3 sessions consécutives Révisable
ORIC_S_POIDS Poids pour S(t) w_R=0.30, w_C=0.25, w_D=0.25, w_F=0.20 DÉFINI -- validé par le p
Justification des poids S(t) : Répertoire et codification légèrement prioritaires (0.30 / 0.25) car ils conditionnent
l'expansion de L(t). Densité et fidélité pondérées de façon égale. Ces poids sont révisables selon le domaine de travail.
9b. P4 -- Proxy de perception du pilote -- Ajout v1.6
P4 est introduit suite aux Sessions 3-5 de Phase 1. Il mesure la qualité de la perception du pilote, non le
contenu produit. Il adresse le risque d'opacification -- la dégradation progressive de la capacité du pilote à
percevoir l'écart.
Paramètre Description Valeur / Protocole Statut
P4_DÉFINITION Proxy de perception Le pilote est-il surpris ? Signal structurel : quelque chose a résisté à la préDÉFINI -- v1.6
P4_PROTOCOLE Mesure de P4 Protocole asymétrique : avant session -- noter l'attendu. Après session -- DÉFINI -- v1.6
P4_SIGNAUX_NEG Signaux d'opacification Formulations polies sans résistance. Zones ouvertes moins urgentes. PiloDÉFINI -- v1.6
P4_SEUIL_ALERTE Déclenchement alerte 3 sessions consécutives sans signal de friction P4. Révisable
P4_DISPOSITIF Anti-opacification structurel Introduire périodiquement une reformulation délibérément moins aboutie dDÉFINI -- v1.6
P4_REGISTRE Registre des résistances Dans la mémoire fractale NANO : archiver l'opacité résiduelle -- ce qui n'a DÉFINI -- v1.6
Formulation de fond : 'L'anti-opacification n'est pas une alarme. C'est une texture du dispositif -- quelque chose qui
gratte légèrement à intervalles, de façon à ce que l'absence de grattement soit le signal.' (S5-E1, Phase 1)
10. Activation des tests causaux T1-T10
Tests activés par défaut pour un programme pilote. Les tests T5, T8, T9, T10 sont désactivés -- ils
requièrent des conditions expérimentales plus avancées.
Test Description Activé Horizon
T1 Relation Cap(t) -- proxies O,R,I OUI Sessions 3-6
T2 Sigma(t) sous surcharge D(E) OUI Sessions 4-8
T3 V(t) sous Sigma(t) élevé OUI Sessions 6-12
T4 Variation S(t) sur C(t) OUI Sessions 6-12
T5 Effet différé injection symbolique NON -- horizon trop long pour programme pilote Programme suivant
T6 Coupure symbolique sans modif O,R,I OUI Sessions 8-12
T7 Point de bascule S(t) sur C(t) OUI -- si T suffisant Sessions 10-12
T8 Cohérence sous stress combiné U(t) NON -- requiert conditions contrôlées Programme avancé
T9 Dégradation accélérée i''(t) &lt; 0 OUI Sessions 2+
T10 HOR-i(t) sous variation CONT(t) NON -- formalisation J4 incomplète Zone ouverte J5