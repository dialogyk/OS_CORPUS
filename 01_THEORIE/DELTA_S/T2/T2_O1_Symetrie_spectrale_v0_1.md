---
source: derive -- formalisation O1
dossier: 01_THEORIE/DELTA_S
version: v0_1
date: 2026-03-16
auteur: Moise DANIEL -- Chercheur independant
collaboration: Claude (Anthropic) -- Copilot (Microsoft)
convention: CONVENTION_NOTATION_ASCII_SAFE_OS_v1_1.md
statut: jalon T2 -- O1 formalise, TC1 programme
depend: Structure_fondamentale_delta_s_v2_1.md
depend: Programme_demonstration_T2_v0_1.md
---

Formalisation O1 : symetrie spectrale
Premier jalon du programme de demonstration T2

Rappel du contexte

Dans le programme T2 v0.1, O1 designe la notion de symetrie spectrale
necessaire pour formuler la transition TC1 (symetrie -> asymetrie).
Ce document construit O1 comme definition formelle derivee de DeltaS.
Aucun axiome nouveau n'est introduit. A2'' est respecte.

---

1. Point de depart : structure de Spec(DeltaS)

Par A10, Spec(DeltaS) est un ensemble discret et ordonne :
Spec(DeltaS) = { phi_1, phi_2, phi_3, ... } avec phi_1 < phi_2 < phi_3 < ...

Par A2, DeltaS(c1, c2) = S(c2) - S(c1).
En particulier : DeltaS(c1, c2) = - DeltaS(c2, c1).

Observation : DeltaS n'est pas symetrique en general.
Mais il peut exister des paires (c1, c2) telles que :
DeltaS(c1, c2) = DeltaS(c2, c1) = 0, ou
| DeltaS(c1, c2) | = | DeltaS(c2, c1) | avec signes opposes.

La symetrie spectrale ne porte pas sur DeltaS directement,
mais sur la structure de Spec(DeltaS) -- c'est-a-dire sur les valeurs phi_i.

---

2. Definition D-O1 : involution spectrale

D-O1 -- Involution spectrale
Une involution spectrale sur Spec(DeltaS) est une application
sigma : Spec(DeltaS) -> Spec(DeltaS)
telle que :
  (i)  sigma(sigma(phi_i)) = phi_i  pour tout phi_i  [involution]
  (ii) sigma(phi_i) != phi_i implique qu'il existe c1, c2 in C
       tels que DeltaS(c1, c2) = phi_i et DeltaS(c2, c1) = sigma(phi_i)

Note : sigma ne requiert pas un produit sur Spec(DeltaS).
C'est une relation binaire d'appariement entre valeurs propres.
Elle est entierement construite a partir de DeltaS et de C.

D-O1' -- Symetrie spectrale
Spec(DeltaS) est dit symetrique s'il admet une involution spectrale sigma
telle que sigma(phi_i) = phi_i pour tout phi_i.
(Chaque pas minimal est son propre partenaire -- les transitions sont reversibles.)

D-O1'' -- Asymetrie spectrale
Spec(DeltaS) est dit asymetrique s'il existe phi_i tel que
sigma(phi_i) != phi_i -- ou si aucune involution ne peut etre definie.
(Au moins un pas minimal n'a pas de partenaire symetrique.)

---

3. Lien avec les configurations de C

La symetrie spectrale a une interpretation directe dans C :

Spec(DeltaS) est symetrique
<=>
Pour tout phi_i in Spec(DeltaS), il existe c1, c2 in C tels que :
  DeltaS(c1, c2) = phi_i  et  DeltaS(c2, c1) = phi_i

Autrement dit : toute transition minimale est reversible avec le meme cout entropique.

Spec(DeltaS) est asymetrique
<=>
Il existe phi_i in Spec(DeltaS) tel que pour tout c1, c2 in C :
  DeltaS(c1, c2) = phi_i  =>  DeltaS(c2, c1) != phi_i

Autrement dit : au moins une transition minimale n'est pas reversible a cout egal.

---

4. Propriete topologique de la symetrie spectrale dans D

On pose :
D_sym = { DeltaS in D | Spec(DeltaS) est symetrique }
D_asym = D \ D_sym

Lemme O1 -- D_sym est clopen dans D

Demonstration :

(Ouverture) Soit DeltaS_0 in D_sym.
Par A10, les phi_i de Spec(DeltaS_0) sont isoles.
Par A9, phi_i >= epsilon > 0 pour tout i.
Dans la topologie de A11 (topologie faible de DeltaS |-> Spec(DeltaS)),
un voisinage de DeltaS_0 dans D correspond a un voisinage de Spec(DeltaS_0)
au sens de Hausdorff.
Comme les phi_i sont isoles (A10) et bornes inferieurement (A9),
un voisinage suffisamment petit de Spec(DeltaS_0) ne peut pas faire
apparaitre ou disparaitre un phi_i sans franchir un trou spectral.
Donc : tout DeltaS suffisamment proche de DeltaS_0 a le meme schema d'appariement
sigma -- et reste dans D_sym.
D_sym est ouvert.

(Fermete) Soit (DeltaS_n) une suite dans D_sym convergeant vers DeltaS* dans D.
Par convergence au sens de Hausdorff (A11), Spec(DeltaS_n) -> Spec(DeltaS*).
Comme les phi_i sont isoles (A10), la convergence est eventuellemment stationnaire :
pour n assez grand, Spec(DeltaS_n) = Spec(DeltaS*) (meme ensemble, meme ordre).
Les involutions sigma_n sont donc stationnaires et convergent vers sigma*.
DeltaS* admet l'involution sigma* : DeltaS* in D_sym.
D_sym est ferme.

Conclusion : D_sym est clopen dans D.

---

5. Application a TC1

TC1 etablit que la transition symetrie -> asymetrie est discontinue dans D.

Corollaire de Lemme O1 :
D_sym et D_asym sont tous deux ouverts dans D.
Il n'existe pas de chemin continu gamma : [0,1] -> D tel que
gamma(0) in D_sym et gamma(1) in D_asym.

TC1 est demontre sous reserve que :
(a) le regime fond generique / EM correspond a DeltaS in D_sym,
(b) le regime Faible correspond a DeltaS in D_asym.

Ces deux points reliant les regimes physiques aux classes D_sym / D_asym
constituent le programme de verification de TC1.
Ils ne relevent pas d'une demonstration axiomatique mais d'une identification
spectrale des regimes -- travail du treillis.

---

6. Ce que O1 ne requiert pas

O1 ne requiert pas :
-- de metrique sur Spec(DeltaS),
-- de produit ou d'algebre sur les phi_i,
-- de structure de groupe,
-- d'invariant exterieur a DeltaS.

L'involution sigma est construite depuis DeltaS et C uniquement.
A2'' est respecte.

---

7. Ouvertures

O1 formalise TC1. Deux questions restent ouvertes pour la suite :

Q-O1a : Comment caracteriser formellement le regime "symetrique"
dans le treillis a partir des seules proprietes de Spec(DeltaS) ?
(Lien entre D_sym et les noeuds fond generique / EM.)

Q-O1b : L'involution sigma est-elle unique pour un DeltaS donne ?
Si Spec(DeltaS) admet plusieurs involutions, la symetrie spectrale
est-elle toujours bien definie ?
Reponse presumee : oui, par l'ordre de Spec(DeltaS) (A10).
A verifier formellement.

---

Conclusion

O1 est formalise. L'involution spectrale sigma est un objet bien defini,
construit depuis DeltaS et C, sans dette ontologique.
Le Lemme O1 etablit que D_sym est clopen dans D.
TC1 est ramene a un probleme d'identification spectrale des regimes.

Prochain jalon : formalisation de O2 (memoire) et ouverture du chantier TC2.
