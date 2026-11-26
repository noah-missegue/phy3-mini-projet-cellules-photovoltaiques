# Agencement — Règles de mise en page des rapports de laboratoire PHY3

Ce document fixe les règles de structure, de mise en page et de forme de **tous les rapports de laboratoire du cours de Physique 3 (PHY3)**, HEIG-VD, département TIN. Il s'applique à tous les sujets du cours : ondes, électromagnétisme, thermique, mécanique, mécanique des fluides, rayonnements ionisants, mini-projets.

Les éléments entre chevrons `<…>` sont des **champs propres à chaque laboratoire**. Les éléments marqués **[PHY3]** sont **fixes pour tout le cours** et ne changent pas d'un rapport à l'autre.

---

## 0. Informations du rapport

### 0.1 Valeurs fixes du cours [PHY3]

| Champ | Valeur |
|---|---|
| École | HEIG-VD (Haute École d'Ingénierie et de Gestion du Canton de Vaud) |
| Institution faîtière | HES-SO (Haute École Spécialisée de Suisse occidentale) |
| Département | Technologies industrielles (TIN) |
| Unité d'enseignement | Physique 3 (Phy3) |
| Type de document | Rapport de laboratoire |
| Lieu de signature | Yverdon-les-Bains |

### 0.2 Valeurs de la volée (identiques pour tous les labos du semestre)

À vérifier en début de semestre, puis à garder pour chaque rapport.

| Champ | Description |
|---|---|
| `<PROFESSEUR>` | Professeur·e responsable du labo PHY3 |
| `<ASSISTANT>` | Assistant·e du labo |
| `<CLASSE>` | Classe, au format `Phy3-TIN-<groupe>` |
| `<SALLE>` | Salle du laboratoire PHY3 (en général T06) |
| `<AUTEURS>` | Membres du groupe : `P. Nom & P. Nom` |
| `<INITIALES>` | Initiales des auteurs, en majuscules : `ABC & DEF` |

### 0.3 Valeurs propres à chaque labo

| Champ | Description |
|---|---|
| `<NUM_LABO>` | Numéro(s) du laboratoire dans le semestre : `n` ou `n et m` |
| `<TITRE_LABO>` | Thème du labo (un ou deux mots) |
| `<DATE>` | Date du laboratoire, en toutes lettres : `jj mois aaaa` |
| `<NB_MANIP>` | Nombre de manipulations |
| `<TITRE_MANIP_n>` | Titre de la manipulation n, repris de la notice |
| `<NOTICE_n>` | Référence de la notice de la manipulation n : `PHY3-03-TPExx` pour les TPE, sinon le numéro de la liste des expériences PHY3 |

---

## 1. Format général

| Élément | Règle |
|---|---|
| Outil | LaTeX (pdfTeX), paquet `hyperref` (liens internes cliquables) |
| Format | A4 portrait (210 × 297 mm), recto seul |
| Police | Latin Modern Roman (`lmodern`), corps **12 pt** |
| Formules | Latin Modern Math |
| Marges | ≈ 3 cm à gauche et à droite (largeur du texte ≈ 15 cm), ≈ 2,5 cm en haut et en bas |
| Langue | Français (`babel` french) : espace avant « : », « ; », « ? », guillemets « » |
| Justification | Texte justifié, césure automatique activée |
| Paragraphes | **Pas d'alinéa** ; les paragraphes sont séparés par un petit espace vertical (`parskip`) |
| Couleur | Texte en noir. La couleur n'apparaît que dans les logos, les photos et les graphiques |

---

## 2. Ordre des pages

1. **Page de titre** (sans en-tête ni pied de page, sans numéro)
2. **Table des matières**, numérotée en chiffres romains (i, ii, …)
3. **Liste des figures**, **Liste des graphiques** et **Liste des tableaux**, à la suite, en chiffres romains (on omet une liste vide)
4. **Corps du rapport** : la numérotation arabe repart à 1 à « Introduction »
5. Conclusion, Signatures, Bibliographie (dans le corps, numérotées comme des sections)
6. Annexes éventuelles (scripts de calcul, fichiers de mesures, notice), après la bibliographie

Chaque section de niveau 1 (Introduction, chaque Manipulation, Conclusion) **commence sur une nouvelle page**. Signatures et Bibliographie suivent la Conclusion sur la même page.

---

## 3. Page de titre

De haut en bas :

1. **Logos [PHY3]** sur une ligne, en haut de page : logo **HEIG-VD** à gauche (bloc rouge « heig-vd » et texte « HAUTE ÉCOLE D'INGÉNIERIE ET DE GESTION DU CANTON DE VAUD / www.heig-vd.ch »), logo **HES-SO** à droite.
2. Grand espace vertical.
3. **Titre centré** sur deux lignes :
   - ligne 1, taille moyenne (`\Large`) : `Laboratoire <NUM_LABO> :`
   - ligne 2, plus grande (`\LARGE`/`\huge`) : `<TITRE_LABO>`
4. Petit bloc de deux colonnes (étiquette, valeur), centré sous le titre **[PHY3]** :
   - `Département :` Technologies industrielles (TIN)
   - `Unité d'enseignement :` Physique 3 (Phy3)
5. Grand espace vertical.
6. **Bloc d'informations aligné à gauche**, deux colonnes (étiquette suivie de « : », valeur) :
   - `Auteurs :` `<AUTEURS>`, en **taille plus grande** (`\Large`) que les lignes suivantes
   - `Professeur :` `<PROFESSEUR>`
   - `Assistant :` `<ASSISTANT>`
   - `Classe :` `<CLASSE>`
   - `Salle :` `<SALLE>`
   - `Date :` `<DATE>`

---

## 4. En-tête et pied de page (toutes les pages sauf la page de titre)

```
Labo <NUM_LABO>: <TITRE_LABO>                         Rapport de laboratoire
────────────────────────────────────────────────────────────────────────────
                               (contenu)
────────────────────────────────────────────────────────────────────────────
HEIG-VD | <INITIALES>                                                 Page X
```

- **En-tête** : `Labo <NUM_LABO>: <TITRE_LABO>` à gauche, « Rapport de laboratoire » à droite, filet horizontal dessous (`fancyhdr`).
- **Pied de page** : « HEIG-VD | `<INITIALES>` » à gauche, « Page X » à droite, filet horizontal dessus.
- Le numéro suit le style de la partie : `Page i`, `Page ii`… puis `Page 1`, `Page 2`…

---

## 5. Structure du contenu (plan type)

La table des matières va jusqu'au niveau 3 (x.y.z). Plan type à respecter :

> **Le plan ci-dessous est un modèle, pas une structure figée.** La structure du document (nombre de manipulations, sous-sections de chaque manipulation, intitulés) peut changer d'un rapport à l'autre en fonction de l'expérience réalisée. On adapte le plan à l'expérience, en conservant l'esprit du modèle.

```
1 Introduction
  1.1 Contexte
  1.2 But et objectifs
  1.3 Répartition du travail
2 Manipulation 1                       ← une section par manipulation (souvent 1 ou 2 en PHY3)
  2.1 Introduction
  2.2 Méthode - Approche
      2.2.1 Rappels théoriques
      2.2.2 Protocole de mesure
  2.3 Résultats - Analyse
      2.3.1 Données brutes
      2.3.2 Résultats réduits et analyse - discussion ← un seul chapitre
      2.3.3 Conclusion
3 Manipulation 2                       ← même structure, autant de fois que nécessaire
  …
N Conclusion
  N.1 Revue des objectifs
  N.2 Résultats principaux
N+1 Signatures
N+2 Bibliographie
```

Règles :
- Titres de section numérotés, en **gras**, tailles LaTeX standard (`\section` > `\subsection` > `\subsubsection`).
- Les intitulés composés gardent le format `Mot - Mot` (espace, trait d'union, espace) : « Méthode - Approche », « Résultats - Analyse », « Résultats réduits et analyse - discussion ».
- Il n'y a **pas de sous-section « Analyse - Discussion » séparée** : l'analyse et la discussion de chaque expérience sont rédigées dans l'unique chapitre « Résultats réduits et analyse - discussion », juste après le graphique ou le tableau de cette expérience.
- Au sein d'un même rapport, chaque manipulation reprend **exactement** les mêmes sous-sections, dans le même ordre, même quand l'une d'elles est vide. Cette structure commune peut en revanche différer d'un rapport à l'autre selon l'expérience.
- Les numéros de section s'ajustent au nombre de manipulations : Conclusion, Signatures et Bibliographie restent toujours les trois dernières sections.

### 5.1 Contenu attendu par section

| Section | Contenu |
|---|---|
| 1.1 Contexte | Pourquoi le travail est réalisé, dans quel cadre et dans quelles conditions (cours, durée de la séance, salle, thème abordé). Ex. : « Ce travail a été réalisé dans le cadre du cours PHY3-TIN, lors d'une séance de laboratoire de n périodes en salle `<SALLE>`. Le thème abordé est `<…>`. » Chaque figure présentée est commentée : on dit au lecteur pourquoi on la montre et ce qu'elle apporte à la démarche. |
| 1.2 But et objectifs | Les objectifs du travail : la problématique, la question à laquelle on répond. Puis les **tâches** à effectuer pour les atteindre : des démarches spécifiques (verbe d'action) et mesurables (SMART). Format : `Objectif n : …` suivi, en retrait, de `Tâche n-1 : …`, `Tâche n-2 : …`. Ex. : « Objectif 1 : validation expérimentale de la loi de Coulomb. Tâche 1-1 : mesure expérimentale, avec son incertitude, de la force électrostatique. Tâche 1-2 : calcul théorique, avec son incertitude, de la force électrostatique. Tâche 1-3 : comparaison des valeurs théoriques et expérimentales. » |
| 1.3 Répartition du travail | Une courte présentation de la répartition du travail présenté dans le rapport. |
| x.1 Introduction | Rappel des objectifs et des tâches du 1.2 qui concernent cette manipulation, au même format (`Objectif n` puis `Tâche n-1`, `n-2`, …), avec une citation de la notice. |
| x.2.1 Rappels théoriques | Les lois utilisées dans le rapport : lois physiques ou mathématiques, méthodes de calcul de l'incertitude, etc. Chaque loi a un titre (`Loi xxx :`), une équation numérotée et la liste des paramètres `symbole : description [unité]`. Tous les paramètres sont explicités, dans le texte ou dans un tableau (voir §6). |
| x.2.2 Protocole de mesure | Les méthodes utilisées pour obtenir les données : se référer au maximum aux notices existantes, et présenter les choix, outils, gestes et arrangements particuliers utilisés pour les mesures. Figures et tableaux repris d'une notice portent la mention « Selon [n] ». |
| x.3.1 Données brutes | Présentation des mesures brutes (tableaux, figures), en montrant qu'elles valident la méthode expérimentale. Source indiquée sous un tableau repris (« Selon [n] »). |
| x.3.2 Résultats réduits et analyse - discussion | Présentation des données réduites et des résultats, avec un **tableau récapitulatif** qui compare valeurs expérimentales et théoriques. Colonnes : `X_exp [unité]` (valeur ± incertitude), `ΔX_exp/X_exp [%]`, `X_th [unité]` (valeur ± incertitude), `ΔX_th/X_th [%]`, `Écart [%]`, avec une ligne par mesure. Légende type : « Tableau n - Tableau récapitulatif de l'expérience n. Comparaison entre valeurs expérimentales et valeurs théoriques ». Pour chaque expérience, dans cet ordre : titre en gras, graphique ou tableau réduit, puis directement le paragraphe d'**analyse et discussion** de cette expérience. Contenu de l'analyse et discussion : discussion **quantitative** du tableau récapitulatif, mesure par mesure. **Cas positif** (écart < incertitude) : « l'écart entre valeurs expérimentale et théorique de a %, inférieur à l'incertitude expérimentale de b % : la loi théorique est validée aux incertitudes expérimentales près. » **Cas négatif** (écart > incertitude) : la loi n'est pas validée par cette mesure, suivi d'une analyse critique des méthodes théoriques et expérimentales qui pourraient l'expliquer : hypothèse de départ fausse ? approximation théorique trop forte ? incertitude de mesure sous-estimée ? erreur de mesure ? faute de saisie ? etc. |
| x.3.3 Conclusion | Synthèse de l'expérience : résultats principaux (valeurs mesurées et théoriques avec leurs incertitudes, configuration par configuration), indication si l'objectif est atteint (« La mesure n valide / ne valide pas en l'état la loi … »), et cause supposée d'un résultat négatif. |
| N.1 Revue des objectifs | Pour chaque objectif et chaque tâche du 1.2, dire si elle a été effectuée (« Tâche 1-1 : la mesure … a été effectuée. »). Pour une tâche non réalisée ou partielle, en donner brièvement la raison (ex. « n'a été effectuée que pour une seule configuration, faute de temps »). Rester factuel. |
| N.2 Résultats principaux | Rappel des résultats essentiels, en lien avec les objectifs, en reprenant les conclusions de chaque expérience. Liste à tirets, factuelle. Ex. : « Nous avons déterminé expérimentalement la grandeur xx à (2,36 ± 0,03) W, qui présente un écart de 0,3 % avec la valeur tabulée de référence. » ; « Nous avons adapté le montage xx, ce qui a permis de réduire l'incertitude sur la grandeur xx de 3 % à 0,2 %. » |
| N.3 (Perspectives) | Facultatif, si pertinent : suites à donner, améliorations possibles, recommandations sur le protocole. |
| N.4 (Commentaire personnel) | Facultatif, si pertinent : difficultés particulières rencontrées, avis sur le travail demandé. |
| Bibliographie | Liste numérotée `[n]` des sources citées : polycopié ou notice du laboratoire, sites web, articles, ouvrages (voir §16). |

---

## 6. Formules (rappels théoriques)

Chaque formule suit ce bloc :

```
Nom de la relation :                      ← souligné, suivi de « : »

                 formule centrée                         (x.n)

      a : description de la grandeur [unité]   ← liste des symboles, en retrait
      b : constante, valeur numérique [unité]
      c : grandeur sans dimension [-]
```

- **Titre** : souligné (`\underline{…}`), puis espace et « : ».
- **Équation** : environnement `equation`, centrée, numérotée **par section** au format `(section.n)`. Le numéro est aligné à droite.
- **Légende des symboles** : en retrait (≈ 1,5 cm), une ligne par symbole au format `symbole : description [unité]`. Grandeur sans dimension : `[-]`. Degrés : `[°]`. Pourcentage : `[%]`.
- Une constante reçoit sa valeur dans la légende (`c : vitesse de la lumière dans le vide, 2,998 × 10⁸ [m/s]`, `R : constante des gaz parfaits, 8,314 [J/(mol·K)]`). Les valeurs viennent du formulaire PHY3 ou d'une source citée.
- Une relation et sa forme inversée tiennent sur la même ligne, séparées par `⇐⇒` (`\iff`).
- On ne répète pas un symbole déjà défini, sauf s'il le faut pour comprendre la formule.
- Un court texte explicatif peut suivre une formule (hypothèse, condition d'application, conséquence sur l'incertitude).
- Le texte renvoie aux formules par leur numéro entre parenthèses : « l'équation (x.n) ».
- Les notations suivent celles du cours et du formulaire PHY3.

### 6.1 Formules de traitement des mesures [PHY3]

À placer à la fin des rappels théoriques de chaque manipulation qui les utilise :

- moyenne et écart-type de l'échantillon ;
- écart relatif à la valeur attendue : `ε = (x_mes − x_att) / x_att × 100 [%]` ;
- propagation des incertitudes (dérivées partielles ou incertitude relative) ;
- régression linéaire (pente, ordonnée à l'origine et leurs incertitudes), quand une grandeur s'obtient par une pente.

---

## 7. Protocole de mesure

- **Paragraphes de contexte** commençant par un titre **en gras, sur la même ligne, terminé par un point** : `Montage général.`, `Déroulement des mesures.`, `Incertitudes.`
- **Sous-partie par expérience** : titre en gras non numéroté, au format `Expérience n - Nom`.
- **Étapes** : liste numérotée `1.`, `2.`, `3.`…, à l'infinitif (« Placer… », « Régler… », « Lire… »).
- Les composants du matériel sont repérés par leur numéro de la notice entre parenthèses : « l'élément (n) ».
- Les instruments de mesure sont nommés précisément (multimètre, oscilloscope ou picoscope, fréquencemètre, sonde de Hall, capteur CASSY, compteur Geiger-Müller…), avec leur calibre ou réglage quand il influence la mesure.
- Chaque expérience est suivie d'une **photo du montage** prise au laboratoire (figure).
- Les **consignes de sécurité et de manipulation** de la notice (laser, gaz, sources radioactives, éléments fragiles, limites de courant ou de température) sont rappelées dans l'étape concernée.
- Le paragraphe `Incertitudes.` termine le protocole : incertitude de lecture pour chaque grandeur et nature de l'incertitude (estimation de lecture, résolution de l'appareil, écart-type sur répétition).
- Quand le protocole comporte des phases distinctes, on le découpe en sous-titres en gras sur leur propre ligne : `Partie calculs théoriques avant mesure`, `Montage expérimental`, `Partie expérimentale`.

---

## 8. Figures (photos et schémas)

- Centrées, largeur ≈ 50 à 60 % de la largeur du texte (`\includegraphics[width=0.55\textwidth]`). Une figure qui ne tient pas sur la page passe à la page suivante (flottant).
- **Légende sous la figure**, centrée, au format :
  `FIGURE n - Description.` → « Figure » en **petites capitales**, numéro, espace, trait d'union, espace, description.
- Numérotation continue sur tout le document (1, 2, 3, …), sans préfixe de section.
- Les sous-figures côte à côte ont chacune une étiquette courte en dessous et une légende commune.
- La légende alimente la **Liste des figures**.
- Légende type d'un montage : « Montage manipulation n - description ».
- Un schéma repris d'une notice cite sa source dans la légende (`[n]`).

---

## 9. Tableaux

- Style **booktabs** : trois filets horizontaux (haut, sous l'en-tête, bas), **aucun filet vertical**.
- Tableau centré, contenu des cellules centré.
- **Toujours un tableau LaTeX standard** (`table` + `tabular`), jamais une image ni une capture du tableau Excel.
- **Recopie fidèle du tableau Excel** : mêmes variables, mêmes unités, mêmes nombres et même forme (mêmes décimales et chiffres significatifs, même notation scientifique, même ordre des colonnes et des lignes) que le tableau Excel à recopier. Rien n'est ajouté, supprimé, arrondi ou reformulé.
- **Calcul dans une colonne** : le numéro de l'équation utilisée est placé **à droite de l'unité, séparé par un espace**, et le renvoi est **entre parenthèses** : `$grandeur$ [unité] (x.n)`, par ex. `$F_{\mathrm{th}}$ [N] (2.3)`.
- **En-têtes** : `grandeur [unité]`, grandeur en italique mathématique, unité entre crochets droits (`$U$ [mV]`, `$x$ [cm]`, `$f$ [Hz]`). Un indice descriptif est en romain (`$U_{\mathrm{ref}}$`).
- Une donnée constante sur toute la série (matériau, dimension fixe, gaz) n'apparaît **que sur la première ligne** de sa colonne.
- Les incertitudes sont dans une colonne `Δgrandeur [unité]` ou au format `valeur ± incertitude`.
- **Légende sous le tableau**, centrée : `TABLEAU n - Données brutes, expérience n` (« Tableau » en petites capitales).
- Numérotation continue sur tout le document.
- Tableau de **résultats réduits** : trois colonnes `Grandeur | Valeur | Unité`. Pour un calcul, le numéro de l'équation suit l'unité, séparé par un espace et entre parenthèses (`grandeur [unité] (x.n)`).
- Le tableau est **toujours annoncé** juste avant par une phrase : « Le Tableau n donne / montre … ».
- Légendes types : « Données brutes, expérience n » et « Données réduites, expérience n ».

---

## 10. Graphiques

- Flottant séparé (`graphique`), avec **sa propre liste** (« Liste des graphiques ») et sa propre numérotation continue.
- Tracés en **pgfplots/TikZ** (vectoriels), centrés, largeur ≈ 60 à 70 % du texte.
- Style :
  - grille de fond grise légère ;
  - axes titrés `grandeur [unité]`, grandeur en italique ;
  - courbes de mesure : traits fins avec marqueurs ronds (bleu ; vert, puis rouge pour les séries supplémentaires) ;
  - **légende dans le coin supérieur droit**, encadrée, quand il y a plusieurs séries ;
  - courbe théorique en **pointillés noirs**, légendée avec le numéro de l'équation (« (x.n) nom de la loi ») ;
  - barres d'incertitude ou rectangles d'erreur quand des incertitudes existent ;
  - pour des catégories : diagramme en barres colorées, valeur affichée au-dessus de chaque barre ;
  - régression linéaire : droite tracée, équation et pente (avec incertitude) affichées dans la légende.
- **Légende sous le graphique**, centrée : `Graphique n - Données réduites, expérience n`.
- Chaque graphique est **précédé du titre en gras de l'expérience** et **suivi du paragraphe d'analyse et discussion** de cette expérience.
- Pour plusieurs expériences regroupées : titre « Expérience n, m - … » et légende « Données réduites, expériences n et m ».
- Mesures sur oscilloscope : capture d'écran en **figure** (pas en graphique), avec les calibres indiqués dans la légende.

---

## 11. Titres d'expérience dans les résultats

- Titre **en gras**, non numéroté, sur sa propre ligne, au format `Expérience n - Nom complet de l'objectif` (nom de l'objectif repris de la section 1.2).
- Le même titre se répète dans Protocole, Données brutes et Résultats réduits et analyse - discussion, pour suivre chaque expérience d'une partie à l'autre.
- Dans Résultats réduits et analyse - discussion, sous chaque titre d'expérience : le graphique ou le tableau réduit, puis le paragraphe d'analyse et discussion. On ne regroupe pas les analyses à la fin de la sous-section.
- Une expérience sans graphique ou tableau réduit garde son titre, suivi d'une phrase de renvoi (« Le Tableau n donne déjà toutes les informations pour l'analyse de l'expérience n. »).
- Quand une manipulation n'a qu'une série par condition (par ex. un gaz, un matériau), le titre peut prendre la forme `Expérience - <condition>`.

---

## 12. Listes

| Type | Rendu | Usage |
|---|---|---|
| Liste non ordonnée | tiret cadratin « — » (style `babel` français) | Objectifs, énumérations |
| Liste ordonnée | `1.`, `2.`, `3.` | Étapes du protocole |

Les listes sont en retrait par rapport au texte.

---

## 13. Typographie des nombres et unités

- **Virgule décimale partout** : texte, légendes, tableaux et graphiques.
- Espace entre la valeur et l'unité : `12 mV`, `9,4 GHz`. L'unité est droite, jamais en italique.
- Unités du Système international et préfixes standard (mV, kHz, GHz, µT…).
- Notation scientifique avec croix : `a,bc × 10ⁿ` (jamais « e »).
- Les unités sont **toujours entre crochets droits** `[unité]` quand elles sont séparées de leur grandeur : en-têtes et cellules de tableaux (y compris un petit tableau `T | 297,1 | [K]`), axes, légendes de symboles. Dans le texte courant, l'unité suit la valeur sans crochets (`12 mV`).
- Les variables sont **toujours en italique** (mathématique), partout : texte, tableaux, graphiques, légendes ; indices descriptifs en romain ($x_{\mathrm{mes}}$, $x_{\mathrm{att}}$).
- Angles : `30°`. Dans le texte, les couples s'écrivent entre parenthèses, `(a°, b°)`.
- Résultat final au format `grandeur = (valeur ± incertitude) unité`, l'incertitude arrondie à 1 ou 2 chiffres significatifs et la valeur arrondie à la même décimale.
- Pour uniformiser, utiliser `siunitx` (`\num{}`, `\SI{}{}`) avec `output-decimal-marker={,}`.

---

## 14. Références croisées et citations

- Renvois avec majuscule et numéro : « le Tableau n », « le Graphique n », « la Figure n », « l'équation (x.n) ». À générer avec `\ref` ou `cleveref` (jamais en dur).
- Les références dans le texte (renvois aux tableaux, graphiques, figures et équations, ainsi que les citations bibliographiques) sont en **italique souligné** : « <u>*Tableau n*</u> », « <u>*équation (x.n)*</u> », « <u>*[n]*</u> ». En LaTeX : `\underline{\textit{…}}`, via une macro dédiée (ex. `\refit`, `\citeit`) pour ne pas le répéter à la main.
- Une référence à une figure ou à un tableau reprend **exactement le libellé de la légende** : nom avec majuscule + numéro, p. ex. « <u>*Figure 16*</u> » (jamais « figure 16 » ni un renvoi sans numéro). En LaTeX : `\figref{fig:…}` → « Figure n » et `\tabref{tab:…}` → « Tableau n » (macros du préambule, `\ref` + italique souligné) ; pour un graphique ou une équation : `\refit{Graphique}{\ref}{…}`, `\refit{équation}{\eqref}{…}`. Chaque figure référencée porte un `\label` placé après son `\caption`.
- Citations bibliographiques entre crochets : `[n]`, placées en fin de phrase, avant le point.
- La notice de la manipulation est citée dès sa première mention.

---

## 15. Signatures

```
Yverdon-les-Bains le <DATE>                   ← à gauche

                                <AUTEURS>     ← centré
```

Lieu et date sur une ligne, puis les noms des auteurs centrés en dessous, avec de la place pour signer.

---

## 16. Bibliographie

- Section numérotée « Bibliographie », liste à étiquettes numériques `[1]`, `[2]`…
- Format d'une entrée : `[n] AUTEURS EN PETITES CAPITALES. Titre en italique. Année.`
- Ordre : ordre d'apparition dans le texte.
- À inclure au minimum :
  - la **notice de chaque manipulation** (`<NOTICE_n>`), avec ses auteurs ;
  - le **cours PHY3** (APD) ou le **formulaire PHY3** quand une formule ou une constante en vient ;
  - la documentation du fabricant du kit, si elle est utilisée ;
  - les sources des valeurs tabulées (indices, vitesses, permittivités, modules…).

---

## 17. Style rédactionnel

- Registre neutre et scientifique. Les protocoles sont à l'infinitif ; la description des travaux réalisés à la 1re personne du pluriel (« Nous avons réalisé… ») ou au passif.
- Les analyses citent toujours les **valeurs mesurées avec leur unité** et renvoient au tableau ou au graphique concerné.
- Chaque analyse distingue ce qui est confirmé **qualitativement** de ce qui l'est **quantitativement** (écart relatif en %, compatibilité dans les incertitudes), et nomme les sources d'erreur (alignement, lecture, réglages, température, perturbations extérieures).
- Paragraphes de 4 à 10 lignes, une idée par paragraphe.
- **Pas de « ; » ni de « : » dans le texte rédigé** (paragraphes, analyses, discussions, conclusions, légendes). On coupe en deux phrases ou on relie avec un mot de liaison (« car », « donc », « ainsi », « c'est-à-dire »…). Seuls les éléments de structure gardent leur « : » : étiquettes de la page de titre, titres de formule (`Loi xxx :`), légendes des symboles (`a : description [unité]`), `Objectif n :` et `Tâche n-m :`.

---

## 18. Points de contrôle avant remise

- [ ] Tous les champs `<…>` sont remplis (page de titre, en-tête, pied de page, signatures).
- [ ] Les valeurs fixes [PHY3] sont exactes (TIN, Physique 3 (Phy3), HEIG-VD, Yverdon-les-Bains).
- [ ] Toutes les sous-sections du plan type sont présentes et rédigées.
- [ ] Les titres d'expérience sont identiques d'une partie à l'autre.
- [ ] Chaque tableau, figure et graphique a sa légende et est cité dans le texte.
- [ ] Les références dans le texte (renvois et citations) sont en italique souligné.
- [ ] Les valeurs sont identiques entre tableaux, graphiques et texte.
- [ ] Chaque résultat final porte son incertitude et est comparé à une valeur attendue.
- [ ] La virgule décimale est utilisée partout et les chiffres significatifs sont cohérents.
- [ ] Les nombres d'éléments sont les mêmes partout (gaz, matériaux, expériences, mesures annoncés vs réalisés).
- [ ] Le texte rédigé ne contient ni « ; » ni « : » (hors éléments de structure, voir §17).
- [ ] Il n'y a pas de légende en double (« , , »), de texte provisoire (« ? ? ? ») ni de page presque vide.
- [ ] La bibliographie contient la notice de chaque manipulation et toutes les sources citées.

---

## 19. Préambule LaTeX conseillé

```latex
\documentclass[12pt,a4paper]{article}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage{lmodern}
\usepackage[french]{babel}
\usepackage[a4paper,left=3cm,right=3cm,top=2.5cm,bottom=2.5cm]{geometry}
\usepackage{parskip}                 % pas d'alinéa, espace entre paragraphes
\usepackage{amsmath,amssymb}
\usepackage{graphicx,subcaption}
\usepackage{booktabs}
\usepackage{siunitx}
\sisetup{output-decimal-marker={,}}
\usepackage{pgfplots}\pgfplotsset{compat=1.18}
\usepackage{float,newfloat}
\DeclareFloatingEnvironment[fileext=log,listname={Liste des graphiques},
  name=Graphique]{graphique}
\usepackage{caption}
\DeclareCaptionLabelSeparator{tiret}{ - }
\captionsetup{labelsep=tiret}        % "Figure 1 - Titre"
\captionsetup[figure]{labelfont=sc}
\captionsetup[table]{labelfont=sc}
\numberwithin{equation}{section}     % (2.1), (2.2)…
\setcounter{tocdepth}{3}

% ---- Valeurs fixes PHY3 ----
\newcommand{\departement}{Technologies industrielles (TIN)}
\newcommand{\unite}{Physique 3 (Phy3)}
\newcommand{\lieu}{Yverdon-les-Bains}

% ---- Valeurs de la volée ----
\newcommand{\auteurs}{<AUTEURS>}
\newcommand{\initiales}{<INITIALES>}
\newcommand{\professeur}{<PROFESSEUR>}
\newcommand{\assistant}{<ASSISTANT>}
\newcommand{\classe}{<CLASSE>}
\newcommand{\salle}{<SALLE>}

% ---- Valeurs du labo ----
\newcommand{\numlabo}{<NUM_LABO>}
\newcommand{\titrelabo}{<TITRE_LABO>}
\newcommand{\datelabo}{<DATE>}

\usepackage{fancyhdr}
\pagestyle{fancy}\fancyhf{}
\fancyhead[L]{Labo \numlabo: \titrelabo}
\fancyhead[R]{Rapport de laboratoire}
\fancyfoot[L]{HEIG-VD | \initiales}
\fancyfoot[R]{Page \thepage}
\renewcommand{\headrulewidth}{0.4pt}
\renewcommand{\footrulewidth}{0.4pt}
\usepackage[hidelinks]{hyperref}
\usepackage{cleveref}
```

Ordre dans `document` : page de titre (`\thispagestyle{empty}`) → `\pagenumbering{roman}` → `\tableofcontents` → `\newpage\listoffigures` → `\listofgraphiques` → `\listoftables` → `\newpage\pagenumbering{arabic}` → sections, chacune précédée de `\newpage` (niveau 1).
