---
source: derive -- formalisation O2
dossier: 01_THEORIE/DELTA_S
version: v0_1
date: 2026-03-16
auteur: Moise DANIEL -- Chercheur independant
collaboration: Claude (Anthropic) -- Copilot (Microsoft)
convention: CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
statut: jalon T2 -- O2 formalise, TC2 programme
depend: Structure_fondamentale_delta_s_v2_1.md
depend: Programme_demonstration_T2_v0_1.md
depend: T2_O1_Symetrie_spectrale_v0_1.md
---

Formalisation O2 : memoire dans L
Deuxieme jalon du programme de demonstration T2

Rappel du contexte

Dans le programme T2 v0.1, O2 designe la notion de memoire dans L,
necessaire pour formuler la transition TC2 (sans memoire -> memoire).
Ce document construit O2 depuis l'espace des trajectoires sur C,
derive de T1 (composition additive). Aucun axiome nouveau. A2'' respecte.

---

1. Construction de l'espace des trajectoires

Par T1, DeltaS est additivement compose :
DeltaS(c1, c3) = DeltaS(c1, c2) + DeltaS(c2, c3)

Cela rend licite de parler de chemins dans C comme suites finies ordonnees.

D-Traj -- Trajectoire dans C
Une trajectoire de longueur k depuis c0 est une suite :
gamma = (c0, c1, c2, ..., ck)
telle que DeltaS(c_{i}, c_{i+1}) = phi_{n_i} in Spec(DeltaS) pour tout i.
(Chaque pas est un element du spectre -- garanti par A9 et A10.)

D-Traj' -- Historique spectral
L'historique spectral d'une trajectoire gamma est la suite des pas :
H(gamma) = (phi_{n_0}, phi_{n_1}, ..., phi_{n_{k-1}})

L'historique est un mot sur l'alphabet Spec(DeltaS).

D-Traj'' -- Etat courant
L'etat courant d'une trajectoire gamma est le dernier element :
end(gamma) = c_k

Deux trajectoires gamma et gamma' sont dites co-terminales si :
end(gamma) = end(gamma') = c

Elles atteignent le meme etat par des chemins (potentiellement) differents.

---

2. Definition D-O2 : memoire dans L

D-O2 -- L sans memoire
L est dit sans memoire si pour toutes trajectoires co-terminales gamma, gamma' :
H(gamma) != H(gamma') => L(end(gamma)) = L(end(gamma'))

Autrement dit : L ne depend que de l'etat courant, pas du chemin parcouru.
L est une fonction de C dans C.

D-O2' -- L avec memoire
L est dit avec memoire si il existe deux trajectoires co-terminales gamma, gamma'
telles que :
H(gamma) != H(gamma')  et  L(end(gamma)) != L(end(gamma'))

Autrement dit : deux chemins distincts menent au meme etat,
mais L produit des transitions differentes selon le chemin emprunte.
L est une fonction de (C x Historique) dans C.

---

3. Lien avec la multiplicite dans Spec(DeltaS)

La memoire de L est liee a la multiplicite des phi_i dans Spec(DeltaS).

Definition : multiplicite spectrale
La multiplicite de phi_i in Spec(DeltaS) est le nombre de paires (c1, c2) in C^2
(a equivalence pres) telles que DeltaS(c1, c2) = phi_i.
On note mult(phi_i) cette multiplicite.

Lemme de liaison O2
L est sans memoire => pour tout phi_i, mult(phi_i) = 1
(a equivalence de trajectoires pres).

Reciproque : si mult(phi_i) > 1 pour au moins un phi_i,
alors il est possible que L soit avec memoire
(deux paires distinctes realisent le meme pas -- L peut les distinguer).

Note : la multiplicite elevee est necessaire mais pas suffisante pour la memoire.
Elle ouvre la possibilite de la memoire ; L doit effectivement l'exploiter.

---

4. Propriete topologique de la memoire dans D

On pose :
D_mem = { DeltaS in D | L induit par DeltaS est avec memoire }
D_nomem = D \ D_mem

Lemme O2 -- La multiplicite des phi_i est localement constante dans D

Demonstration :

Soit DeltaS_0 in D et phi_i in Spec(DeltaS_0) de multiplicite m_0.
Dans la topologie de A11 (topologie faible de DeltaS |-> Spec(DeltaS)),
un voisinage de DeltaS_0 dans D correspond a un voisinage de Spec(DeltaS_0)
au sens de Hausdorff.

Par A10, les phi_i sont isoles dans Spec(DeltaS).
Par A9, phi_i >= epsilon > 0.

Une deformation continue de DeltaS_0 dans D ne peut pas :
-- faire apparaitre un nouveau phi_i (il faudrait franchir un trou spectral),
-- faire disparaitre un phi_i existant (idem),
-- fusionner deux phi_i distincts (ils sont isoles par A10).

Donc : pour tout DeltaS suffisamment proche de DeltaS_0 dans D,
Spec(DeltaS) a les memes phi_i avec les memes multiplicites.
La multiplicite est localement constante.

Corollaire : D_mem est clopen dans D

Si DeltaS_0 in D_mem, alors mult(phi_i) > 1 pour au moins un phi_i.
Par le Lemme O2, cette propriete est preservee dans un voisinage de DeltaS_0.
Donc D_mem est ouvert.

Si (DeltaS_n) -> DeltaS* avec DeltaS_n in D_mem :
Par convergence stationnaire (meme argument qu'en O1),
Spec(DeltaS*) = Spec(DeltaS_n) pour n assez grand.
Les multiplicites de DeltaS* sont les memes que celles de DeltaS_n.
DeltaS* in D_mem.
Donc D_mem est ferme.

Conclusion : D_mem est clopen dans D.

---

5. Application a TC2

TC2 etablit que la transition sans-memoire -> memoire est discontinue dans D.

Corollaire du Lemme O2 :
D_mem et D_nomem sont tous deux ouverts dans D.
Il n'existe pas de chemin continu gamma : [0,1] -> D tel que
gamma(0) in D_nomem et gamma(1) in D_mem.

TC2 est demontre sous reserve que :
(a) le regime Faible correspond a DeltaS in D_nomem,
(b) le regime Vivant correspond a DeltaS in D_mem.

Ces identifications spectrales relevent du treillis, pas de l'axiomatique.

---

6. Relation avec O1 : coherence du programme

O1 et O2 utilisent le meme schema de preuve :
-- identifier une propriete P de Spec(DeltaS),
-- montrer que P est localement constante dans D (via A9 + A10 + A11),
-- conclure que D_P est clopen.

La difference structurelle :
-- O1 porte sur une propriete de Spec(DeltaS) seul (symetrie des phi_i).
-- O2 porte sur une propriete de Spec(DeltaS) relative a C (multiplicite des paires).

O2 est donc d'une couche de plus que O1 :
il requiert l'espace des trajectoires (D-Traj, D-Traj', D-Traj''),
qui est lui-meme derive de T1.
La hierarchie est respectee.

---

7. Ce que O2 ne requiert pas

O2 ne requiert pas :
-- de mesure sur l'espace des trajectoires,
-- de topologie sur C au-dela de celle induite par DeltaS (A4),
-- de structure d'historique infinie (les trajectoires sont finies par construction),
-- d'invariant exterieur a DeltaS.

La memoire est une propriete de L derivee de la multiplicite dans Spec(DeltaS).
A2'' est respecte.

---

8. Questions ouvertes

Q-O2a : Condition suffisante pour que mult(phi_i) > 1 => L est effectivement avec memoire.
La multiplicite est necessaire, pas suffisante. Il faudra specifier
dans quelles conditions L exploite effectivement la multiplicite.
Hypothese de travail : L exploite la multiplicite si et seulement si
les paires de C realisant le meme phi_i ont des successeurs distincts dans C.

Q-O2b : Lien entre historique spectral H(gamma) et la structure de L.
H(gamma) est un mot sur Spec(DeltaS). La memoire de L correspond
a une sensibilite de L a ce mot. Il faudra definir formellement
quelle structure sur les mots de H(gamma) induit la memoire de L.

---

Conclusion

O2 est formalise. La memoire dans L est construite depuis l'espace des trajectoires
(derive de T1) et liee a la multiplicite dans Spec(DeltaS).
Le Lemme O2 etablit que la multiplicite est localement constante dans D,
ce qui implique que D_mem est clopen.
TC2 est ramene a une identification spectrale des regimes Faible et Vivant.

Le schema de preuve O1 / O2 est uniforme.
Il prepare directement O3 (reflexivite), qui requiert une stratification
de Spec(DeltaS) -- couche supplementaire par rapport a O2.

Prochain jalon : formalisation de O3 (reflexivite) et ouverture du chantier TC3.
