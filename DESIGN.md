# Design

## Direction

**Studio obsidienne — réseau vivant**, le monde du client. La structure en trois écrans du brief d'origine s'est élargie pour répondre aux trois questions que le visiteur se posait sans trouver de réponse — ce que je vends, comment ça se passe, combien ça coûte — sans changer ni le monde ni le rythme. Une scène obsidienne filmée dans le noir : une constellation de nœuds reliés en 3D (Canvas temps réel) qui respire et réagit au visiteur, l'accent indigo/violet, les vitrines de verre, le carrousel des réalisations, la signature « C&C » en particules. Aucune requête tierce. Tout respecte `prefers-reduced-motion`.

## Logo

Signe : un **éclat de clic** — pastille pleine, cinq rayons, curseur posé en bas
à droite — en `--heat-core`. Il dit le geste que le visiteur vient de faire.
Wordmark : `Click` en encre, l'esperluette en `--heat-core`, `Connect` en dégradé
violet (`--heat-core` → `--heat-2`), Bricolage Grotesque 700 vectorisée. Le **o**
de Connect est remplacé par un symbole de mise en marche, tracé aux métriques
exactes du glyphe (anneau ouvert de 78°, épaisseur de fût). Le `i` de Click
utilise le glyphe `dotlessi` de la fonte : l'éclat lui sert de point.

Les trois fichiers de lockup sont engendrés par un même script à partir de la
fonte, crénage HarfBuzz compris — aucune dépendance de police au rendu.

| Fichier | Usage |
|---|---|
| `logo.svg` | Lockup horizontal, fond transparent — texte vectorisé |
| `logo-on-dark.svg` · `logo-on-light.svg` | Le lockup sur aplat obsidienne et sur blanc |
| `logo-mark.svg` | L'éclat seul (avatar, tampon, réseaux) |
| `logo-mono.svg` | Une seule couleur via `currentColor` — impression, facture |
| `favicon.svg` | L'éclat dans la pastille obsidienne, lisible à 32 px |
| `og-image.svg` · `og-image.png` | Image de partage 1200×630, texte vectorisé |

Dans les pages, le signe est inséré en SVG inline dans la pastille `.dc` du
wordmark et hérite des tokens (`var(--ink)`, `var(--heat)`, `var(--heat-core)`).

## Palette

| Rôle | Token | Valeur |
|---|---|---|
| Obsidienne indigo (fond) | `--bg` | `#0B0B16` |
| Panneau, verre | `--panel` `--glass` | `#12161F` · `rgba(18,22,31,.62)` |
| Encre claire chaude | `--ink` | `#F2EEE6` |
| Secondaire | `--ink-soft` | `#9AA2B4` |
| Violet clair — grand affichage, fills | `--heat` | `#8B7CFF` |
| Indigo — liens | `--heat-2` | `#6366F1` |
| Cœur clair | `--heat-core` | `#C4B5FD` |
| Petit texte violet (AA) | `--heat-txt` | `#A99CFF` |

## Typographie

- **Bricolage Grotesque** (`--f-display`) — titres, wordmark, chiffres.
- **Libre Franklin** (`--f-body`) — corps, boutons.
- **Spline Sans Mono** (`--f-mono`) — folios, étiquettes, téléphone.
Toutes auto-hébergées (`fonts.css`, `fonts/*.woff2`).

## Accueil (`index.html` + `home.css` + `home.js`)

1. **Qui** — scène obsidienne plein écran, réseau de nœuds 3D derrière le titre *Un site web qui vous ressemble, fait par une seule personne.*, portrait à droite (vignette au-dessus du titre sur mobile), deux pastilles (Sites web, Applications), bouton magnétique + téléphone, faits 25 / 1 / 24 h.
2. **Le travail** — carrousel « vitrine » (maquette ordinateur + téléphone, rotation auto, parallaxe) avec Jayden, Pizzeria Pino, Yuméa, Toukin ; sous le carrousel, trois vitrines de verre (sur mesure, un seul interlocuteur, et après). Puis le moment signature : les particules se reforment en « C&C ».
3. **Ce que je fais** (II) — **l'orbite** : six nœuds sur un anneau autour d'un cœur « Vincent · un seul interlocuteur », et un panneau de détail qui change au clic. Chaque nœud est un `<button>` (clavier, `aria-pressed`), le panneau est en `aria-live`. Rotation automatique de 4,2 s tant que le visiteur n'a rien touché, arrêtée dès le premier clic et jamais lancée sous `prefers-reduced-motion`. Deux nœuds portent un lien vers les pages SEO, un troisième vers le budget. Composant porté depuis le dépôt SECR3TLY et retokenisé sur l'obsidienne.
4. **La méthode** (III) — quatre cartes `.route-step` reliées par un filet horizontal qui rappelle les arêtes du réseau de fond ; chacune porte son délai en mono.
5. **Le budget** (IV) — trois vitrines de verre `.tier`, celle du milieu marquée « le plus demandé » (bordure chaude + `--bloom`) ; dessous, trois `.bnote` à filet gauche (après la mise en ligne, pourquoi pas moins cher, payer en plusieurs fois).
6. **Les engagements** (V) — six cartes `.pledge` en grille 3×2, pastille ronde à coche, formulées pour être vérifiables plutôt que promises (domaine à votre nom, prix ferme, validation avant code, pas d'abonnement obligatoire, sortie libre, réponse sous 24 h).
7. **Questions** (VI) — huit `<details>` `.qa-item`, accordéon natif sans JS, indicateur « + » qui pivote.
8. **Le contact** (VII) — formulaire nom / e-mail / téléphone / message, envoi AJAX, repli e-mail ; à côté, téléphone, WhatsApp, adresse.

Le moment signature reste entre les questions et le contact. La numérotation des folios court désormais de I à VII.

Motion : réseau vivant (parallaxe souris, nœud illuminé sous le curseur, pause hors viewport), révélations « la chaleur qui monte », boutons magnétiques, signature qui se trace, fil de progression à gauche, halo au curseur. Tout se fige sous `prefers-reduced-motion`.

## Pages de service, pages locales, blog et légales

`styles.css` + `page-theme.css` (surcharge obsidienne, chargée après) : mêmes tokens, même typo, hero à champ de points, cartes verre, accent violet.

- **Pages de service et locales** : application mobile, puis Liège, Seraing, Huy et Namur. Même gabarit (hero, `highlights-grid`, cartes métiers, bloc budget, méthode en 4 étapes, FAQ, liens croisés), mais un texte réellement distinct par ville — jamais la même page avec le nom changé.
- **Blog** (`blog.html` + `blog/*.html`) : liste en cartes `.post-card`, article en colonne de lecture de 720 px (`.post`), encadrés `.post-aside` à filet violet, tableaux `.post-table` à en-têtes mono, bloc de fin `.post-cta`. Styles ajoutés en fin de `page-theme.css`.
- Les liens en plein texte sont soulignés : sans cela, ils ne se distinguaient que par la couleur (WCAG 1.4.1).

## Ce qui n'existe plus

Le Labo et ses cinq outils, les pages crypto / IA / bots, le multilingue. Les sections thèse / artisan / champ de l'ancien accueil ; en revanche `.field-list` et `.qa`, restées dans `home.css`, resservent aux nouvelles sections « Ce que je fais » et « Questions ». Les essais clair / verre liquide / Slate-Mint ont été abandonnés à la demande du client, qui préfère son monde d'origine.
