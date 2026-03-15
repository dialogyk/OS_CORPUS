# CONVENTION NOTATIONNELLE ASCII-SAFE -- CORPUS OS
Version 1.1 -- 2026-03-15
Auteur : Claude Sonnet 4.6 -- Corrections : Copilot -- Validation : Pilote
Statut : v1.1 -- integre corrections Copilot sur v1.0

Modifications v1.0 -> v1.1 :
- Phi_RSU / phi_TUS : collision Phi/phi eliminee
- Sigma_op / sigma_loc : collision Sigma/sigma/Sum eliminee
- C_corr (CST) / C_conf (RSU) : collision C eliminee
- lambda_axis (Dialogyk) : collision avec lambda_n RSU eliminee
- eps4_mu_nu_rho_sigma : notation explicite 4D
- Sum_n=0..N : accolades supprimees, notation ASCII stricte
- Box ajoute dans les mots reserves section 7.2
- Regles "--" et backticks clarifiees en section 6

---

## 0. PRINCIPE DIRECTEUR

Toute notation du corpus OS doit satisfaire trois contraintes simultanement :

1. Lisible par un humain sans rendu (texte brut).
2. Stable pour un pipeline IA (tokenisation, embedding, RAG).
3. Non ambigue : une notation = un objet, un objet = une notation.

Le format source est `.md` ASCII-safe.
Aucun caractere Unicode mathematique ou typographique non-ASCII n'est autorise
dans les zones de notation formelle (equations, definitions, axiomes).
Les accents francais sont autorises dans le texte narratif uniquement.

---

## 1. REGLES GENERALES

### 1.1 Caracteres interdits dans les zones formelles

Les caracteres suivants sont INTERDITS dans toute equation, definition ou axiome :

| Caractere interdit | Code Unicode | Substitution obligatoire |
|--------------------|--------------|--------------------------|
| Subscripts Unicode | u+2080 a u+209F | notation underscore _ |
| Superscripts Unicode | u+2070 a u+207F | notation caret ^ |
| Mu grec | u+03BC | mu |
| Signe micro | u+00B5 | mu |
| Phi grec majuscule | u+03A6 | Phi_RSU |
| Phi grec minuscule | u+03C6 | phi_TUS |
| Psi grec | u+03C8 | psi |
| Lambda grec | u+03BB | lambda_n (RSU) ou lambda_axis (Dialogyk) |
| Sigma grec majuscule | u+03A3 | Sum (somme) ou Sigma_op (TUS) |
| Delta grec majuscule | u+0394 | Delta |
| Delta grec minuscule | u+03B4 | delta |
| Sigma grec minuscule | u+03C3 | sigma_loc (TUS) |
| Nu grec | u+03BD | nu |
| Rho grec | u+03C1 | rho |
| Epsilon grec | u+03B5 | eps |
| Pi grec | u+03C0 | pi |
| Nabla | u+2207 | nabla |
| Appartient | u+2208 | in |
| Fleche droite | u+2192 | -> |
| Fleche gauche | u+2190 | <- |
| Equivalent | u+27FA | <=> |
| Implique | u+21D2 | => |
| Inferieur ou egal | u+2264 | <= |
| Superieur ou egal | u+2265 | >= |
| Different | u+2260 | != |
| Environ egal | u+2248 | ~= |
| Equivalent structural | u+223C | ~ |
| Produit tensoriel | u+2297 | otimes |
| Crochet gauche | u+27E8 | < |
| Crochet droit | u+27E9 | > |
| Ensemble R | u+211D | R |
| Alembertien | u+25A1 | Box |
| Tiret insecable | u+2011 | - |
| En dash | u+2013 | -- |
| Em dash | u+2014 | -- |
| Apostrophe typographique | u+2019 | ' |
| Guillemets francais | u+00AB u+00BB | " |
| Exposant 2 Latin-1 | u+00B2 | ^2 |
| Transpose | u+22A4 | ^T |
| Semi-defini positif | u+2AA0 | >= 0 |
| Inclusion large | u+2287 | supset= |
| STX | u+0002 | SUPPRIMER (joindre le mot) |

---

## 2. NOTATION DES INDICES ET EXPOSANTS

### Regle generale
- Indice (subscript) : underscore `_`
- Exposant (superscript) : caret `^`
- Parentheses pour lever toute ambiguite sur les indices composes

### 2.1 Indices simples

```
psi_n        -- psi indice n
lambda_n     -- lambda indice n
T_mu_nu      -- T indice mu nu
G_mu_nu      -- G indice mu nu
u_mu         -- u indice mu
n_mu         -- n indice mu
a_n          -- coefficient a indice n
C_corr_k     -- operateur correlatif C indice k (CST)
```

### 2.2 Exposants simples

```
psi^2        -- psi au carre
x^n          -- x exposant n
U^T          -- U transpose
C_corr^k     -- C_corr exposant k
```

### 2.3 Indices et exposants combines

```
T_mu_nu^(n)  -- T indice mu nu exposant n (parentheses obligatoires)
psi_n^2      -- psi_n au carre
T_mu_nu_eff  -- T indice mu nu effectif (suffixe textuel)
lambda_0     -- lambda indice zero
C_corr_k+1   -- C_corr indice k+1
```

### 2.4 Sommes et produits

Notation ASCII stricte -- pas d accolades :

```
Sum_n a_n * psi_n              -- somme sur n de a_n * psi_n
Sum_n=0..N a_n * psi_n         -- somme bornee de 0 a N
Prod_k C_corr_k                -- produit sur k de C_corr_k
```

---

## 3. NOTATION DES OPERATEURS

### 3.1 Operateur D (RSU)

```
D(Phi_RSU)                              -- application de D a Phi_RSU
D(psi_n) = lambda_n * psi_n             -- equation propre
Box(g)                                  -- alembertien en metrique g
D = Box(g) + V'(Phi_RSU) + S            -- decomposition de D
```

### 3.2 Operateur nabla (CSU / TUS)

```
nabla_mu I = 0                          -- divergence de I nulle
nabla_rho n_sigma                       -- derivee covariante de n_sigma
nabla_mu T_mu_nu                        -- divergence du tenseur T
```

### 3.3 Produit scalaire et normes

```
<psi_m, D(psi_n)>                       -- produit scalaire
<D(psi_m), psi_n>                       -- auto-adjointeite
|Psi_RSU|^2                             -- norme au carre
||v||                                   -- norme
```

---

## 4. NOTATION DES OBJETS STRUCTURELS

### 4.1 RSU -- Equation fondamentale d advenance

```
A = { Phi_RSU in C_conf | D(Phi_RSU) = 0 }   -- ensemble d advenance
D = Box(g) + V'(Phi_RSU) + S                  -- operateur structurel
Phi_RSU : M -> R                              -- champ RSU
D(psi_n) = lambda_n * psi_n                   -- modes propres
Phi_RSU = Sum_n a_n * psi_n                   -- decomposition modale
T_mu_nu^(n) = lambda_n * psi_n^2             -- contribution modale
T_mu_nu_eff = Sum_n T_mu_nu^(n)              -- tenseur effectif
G_mu_nu = 8 * pi * G * T_mu_nu_eff           -- geometrie retroactive
lambda_0 < 0                                  -- mode fondamental instable
nabla_mu T_mu_nu^(0) < 0                     -- tension structurelle
<psi_m, D(psi_n)> = <D(psi_m), psi_n>       -- auto-adjointeite
```

### 4.2 CSU -- Coherence Structurelle Universelle

```
CSU = (M, g_mu_nu, u^mu, n^mu, I)            -- formulation canonique condensee
g_mu_nu                    -- variete lorentzienne
nabla                      -- connexion de Levi-Civita
u^mu                       -- flot temporel (congruence normalisee)
n^mu                       -- champ d orientation (unitaire)
I                          -- invariant global

-- Normalisation et orthogonalite
u^mu * u_mu = -1
n^mu * n_mu = +1
u^mu * n_mu = 0

-- Invariant global (tenseur de Levi-Civita 4D)
I = eps4_mu_nu_rho_sigma * u^mu * n^nu * nabla_rho * n_sigma

-- Condition d invariance
nabla_mu I = 0
```

### 4.3 CST -- Correlative Structure Theory

```
C_corr in R^(n x n)          -- operateur correlatif
C_corr = C_corr^T            -- symetrie
C_corr >= 0                  -- semi-defini positif
A(C_corr) = Ran(C_corr)      -- sous-espace accessible
dim(A(C_corr)) = rank(C_corr) -- dimension accessible

-- Equivalence correlative
C_corr' = U * C_corr * U^T   -- transformation admissible
C_corr' ~ C_corr             -- equivalence

-- Principes
T(C_corr) ~ C_corr                           -- invariance correlative (P1)
A(C_corr) = Ran(C_corr)                      -- accessibilite spectrale (P2)
C_corr_k+1 = Pi_k * C_corr_k * Pi_k^T       -- hierarchie correlative (P3)
A(C_corr_0) supset= A(C_corr_1) supset= ...  -- filtration spectrale
rank(C_corr_k+1) < rank(C_corr_k)            -- emergence d ordre (P4)
rank(C_corr_k+1) = rank(C_corr_k) - m        -- amplitude de transition (P5)
```

### 4.4 TUS -- Theorie Unifiee des Structures

```
Delta_S              -- invariant entropique central
delta_S > 0          -- condition de non-cloture
Sigma_op             -- operateur de stabilisation TUS
sigma_loc            -- section locale TUS
phi_TUS              -- champ de couplage TUS
nu                   -- mode normal
rho                  -- densite structurelle
eps                  -- ecart spectral
```

### 4.5 Dialogyk

```
lambda_axis          -- invariant d axe Dialogyk
D(lambda_axis) = 0   -- stabilite de l axe
C_i                  -- couloir i
A_j                  -- amplitude j
```

---

## 5. NOTATION DES RELATIONS LOGIQUES ET STRUCTURELLES

```
=>           -- implique
<=>          -- equivalent
!=           -- different
~=           -- approximativement egal
~            -- equivalent structural
in           -- appartient a
not in       -- n appartient pas a
subset=      -- sous-ensemble de (inclusion large)
supset=      -- sur-ensemble de (inclusion large)
subset       -- sous-ensemble strict
supset       -- sur-ensemble strict
forall       -- pour tout
exists       -- il existe
and          -- et
or           ou
not          -- negation
|            -- tel que (dans une definition d ensemble)
:=           -- defini comme
```

---

## 6. REGLES DE FORMATAGE MARKDOWN

### 6.1 Structure d un document OS

```markdown
# TITRE DU DOCUMENT
Version X.Y -- AAAA-MM-JJ
Auteur : ...
Statut : ...

---

## 1. SECTION

### 1.1 Sous-section

Texte narratif ici. Les accents francais sont autorises
dans le texte narratif : emergence, coherence, advenance.

**Definition** : texte de la definition.

**Axiome A1** : texte de l axiome.

Equation inline : `D(Phi_RSU) = 0`

Bloc d equation :

    D(Phi_RSU) = 0
    Phi_RSU = Sum_n a_n * psi_n
    G_mu_nu = 8 * pi * G * T_mu_nu_eff

### 1.2 Autre sous-section
```

### 6.2 Equations inline vs blocs

- Equation courte dans une phrase : backticks inline `D(Phi_RSU) = 0`
- Equation isolee ou multi-lignes : bloc indenté 4 espaces ou bloc code triple backtick

### 6.3 Regles sur les backticks

- Ne jamais imbriquer des backticks.
- Ne jamais placer de backticks a l interieur d un nom de variable.
- Backticks inline : uniquement pour equations courtes en prose.
- Blocs code : pour toute equation de plus d un terme ou multi-lignes.

### 6.4 Regles sur les tirets

- Separateur narratif : `--` (double tiret ASCII).
- Jamais `---` en zone de texte courant : conflits avec les separateurs Markdown `---`.
- Les `---` sont reserves aux separateurs de sections en debut de ligne.
- Tiret simple `-` : soustraction ou liste Markdown uniquement.

### 6.5 Tableaux

```markdown
| Objet     | Notation  | Definition                           |
|-----------|-----------|--------------------------------------|
| Operateur | D         | Box(g) + V'(Phi_RSU) + S             |
| Champ RSU | Phi_RSU   | Phi_RSU : M -> R                     |
| Mode      | psi_n     | D(psi_n) = lambda_n * psi_n          |
| Champ TUS | phi_TUS   | champ de couplage                    |
```

### 6.6 Listes structurelles

```markdown
Invariants du systeme :
- D : operateur structurel
- Phi_RSU : champ d advenance
- lambda_0 : tension du regime
- G_mu_nu : stabilisation retroactive
```

---

## 7. CONVENTIONS SPECIFIQUES AU CORPUS OS

### 7.1 Noms des documents (references internes)

```
RSU          -- Regimes Structurels d Advenance
CSU          -- Coherence Structurelle Universelle
phi          -- document de jonction RSU-phi-CSU (nom de fichier uniquement)
CST          -- Correlative Structure Theory
TUS          -- Theorie Unifiee des Structures
Dialogyk     -- cadre methodologique
OS           -- programme Operateur Structurel
J5           -- Kernel de Champ Cognitif
PREREG       -- Pre-enregistrement
MF           -- Memoire Fractale
RC           -- Rapport de Cloture
```

### 7.2 Variables reservees du corpus OS

Ces notations sont figees.
Elles ne peuvent pas etre reutilisees avec un sens different dans un autre document.

```
-- Operateurs
D            -- operateur structurel RSU
Box          -- alembertien RSU (mot reserve)
nabla        -- derivee covariante CSU/TUS

-- Champs
Phi_RSU      -- champ d advenance RSU
phi_TUS      -- champ de couplage TUS/CST
psi_n        -- mode propre RSU

-- Valeurs propres et modes
lambda_n     -- valeur propre RSU (generique)
lambda_0     -- mode fondamental RSU (instable)
lambda_axis  -- invariant d axe Dialogyk

-- Espaces
C_conf       -- espace des configurations admissibles RSU
M            -- variete structurelle RSU/CSU

-- Tenseurs RSU
T_mu_nu_eff  -- tenseur energie-impulsion effectif
G_mu_nu      -- tenseur geometrique retroactif

-- Tenseurs CSU
g_mu_nu      -- metrique lorentzienne
u^mu         -- flot temporel
n^mu         -- champ d orientation
I            -- invariant global
eps4_mu_nu_rho_sigma  -- tenseur de Levi-Civita 4D

-- CST
C_corr       -- operateur correlatif
A(C_corr)    -- sous-espace accessible

-- TUS
Delta_S      -- invariant entropique
Sigma_op     -- operateur de stabilisation
sigma_loc    -- section locale
```

### 7.3 Suffixes normalises

```
_eff         -- effectif (ex : T_mu_nu_eff)
_0           -- fondamental / mode zero (ex : lambda_0)
_n           -- indice modal generique (ex : psi_n)
_k           -- indice hierarchique (ex : C_corr_k)
^(n)         -- contribution du mode n (ex : T_mu_nu^(n))
_RSU         -- appartient au cadre RSU (ex : Phi_RSU)
_TUS         -- appartient au cadre TUS (ex : phi_TUS)
_op          -- operateur (ex : Sigma_op)
_loc         -- local (ex : sigma_loc)
_corr        -- correlatif CST (ex : C_corr)
_conf        -- configurations RSU (ex : C_conf)
_axis        -- axe Dialogyk (ex : lambda_axis)
_canon       -- forme canonique
_min         -- forme minimale
```

---

## 8. CE QUI EST AUTORISE HORS ZONES FORMELLES

Dans le texte narratif (paragraphes, titres, commentaires) :

- Accents francais : e, a, u, i, o avec accents -- autorises.
- Double tiret ASCII `--` comme separateur -- autorise.
- Apostrophe ASCII simple `'` -- autorise.
- Guillemets ASCII `"` -- autorises.
- Point median remplace par espace-tiret-espace ` - ` -- autorise.

Dans les zones formelles (equations, definitions, axiomes) :
- ASCII pur uniquement.
- Aucune exception.

---

## 9. EXEMPLES DE RECONSTRUCTION

### 9.1 RSU -- avant / apres

**Avant (corrompu)** :

    D(psi_n) = lambda_n * psi_n      (subscripts Unicode)
    T_u_v^(n) = lambda_n * psi_n^2   (indices Unicode)
    G_u_v = 8*pi*G * T_u_v_eff       (symboles Unicode)

**Apres (ASCII-safe v1.1)** :

    D(psi_n) = lambda_n * psi_n
    T_mu_nu^(n) = lambda_n * psi_n^2
    G_mu_nu = 8 * pi * G * T_mu_nu_eff

### 9.2 CSU -- avant / apres

**Avant (corrompu -- tenseurs brises par saut de ligne)** :

    g
    muv
    I = epsilon
    muv rhosigma u
    mu n
    nu nabla
    rho n
    sigma

**Apres (ASCII-safe v1.1)** :

    g_mu_nu
    I = eps4_mu_nu_rho_sigma * u^mu * n^nu * nabla_rho * n_sigma

### 9.3 CST -- avant / apres

**Avant (corrompu -- STX + accents decomposes)** :

    Sma[u+00A8][u+0131]n B[u+00B4]edrouni
    representa[STX]tion-independent
    pos[STX]itive semi-definite

**Apres (ASCII-safe v1.1)** :

    S. Bedrouni
    representation-independent
    positive semi-definite

### 9.4 Collisions resolues -- avant / apres

**Avant (v1.0 -- ambigu)** :

    Phi       -- champ RSU ou champ TUS ?
    C         -- C_conf (RSU) ou C_corr (CST) ?
    lambda    -- lambda_n (RSU) ou invariant Dialogyk ?
    Sigma     -- somme ou operateur TUS ?
    sigma     -- section locale ou lettre grecque ?

**Apres (v1.1 -- non ambigu)** :

    Phi_RSU   -- champ d advenance RSU (unique)
    phi_TUS   -- champ de couplage TUS/CST (unique)
    C_conf    -- espace des configurations RSU (unique)
    C_corr    -- operateur correlatif CST (unique)
    lambda_n  -- valeur propre RSU (unique)
    lambda_axis -- invariant d axe Dialogyk (unique)
    Sum       -- somme mathematique (unique)
    Sigma_op  -- operateur de stabilisation TUS (unique)
    sigma_loc -- section locale TUS (unique)

---

## 10. CONTROLE DE CONFORMITE

Avant de valider un document reconstruit, verifier :

- [ ] Aucun caractere > u+007F dans les zones formelles
- [ ] Aucun STX (u+0002) dans le texte
- [ ] Aucun subscript/superscript Unicode (u+2070 a u+209F)
- [ ] Aucune lettre grecque Unicode dans les equations
- [ ] Aucun signe micro (u+00B5) -- utiliser mu
- [ ] Tous les indices en underscore, tous les exposants en caret
- [ ] Tenseurs ecrits sur une seule ligne
- [ ] Variables reservees coherentes avec la table section 7.2
- [ ] Collisions Phi/phi, C, lambda, Sigma/sigma resolues (section 9.4)
- [ ] Structure Markdown conforme a la section 6.1
- [ ] Equations isolees en blocs indentes ou blocs code
- [ ] Tirets : `--` en narratif, `---` uniquement comme separateur Markdown
- [ ] Backticks non imbriques, non places dans les noms de variables

---

*Convention v1.1 -- integre corrections Copilot sur v1.0*
*Toute modification fait l objet d un increment de version*
