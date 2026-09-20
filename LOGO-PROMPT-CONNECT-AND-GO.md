# Prompt logo — « Connect&Go »

Brief dérivé de l'identité existante (voir `DESIGN.md`) : monde obsidienne,
réseau de nœuds, dégradé violet, Bricolage Grotesque. Le signe actuel dit
« le clic (le point) + la connexion (les deux arcs) ». Pour **Connect&Go**,
on garde le point-nœud et on ajoute le mouvement : la connexion qui repart.

---

## 1. Prompt maître (FR — GPT-Image, Ideogram, Firefly, Claude/SVG)

> Crée un logo vectoriel professionnel pour **« Connect&Go »**, studio digital
> belge (sites web et applications mobiles sur mesure, un seul artisan derrière
> chaque projet). Le logo doit dire deux choses en un seul geste : **connecter**
> et **avancer**.
>
> **Symbole** : un monogramme géométrique construit sur une grille circulaire.
> Un arc ouvert en forme de « C », tracé au trait épais à bouts arrondis, qui
> s'ouvre vers la droite et dont l'extrémité se prolonge en un chevron / une
> pointe de flèche orientée vers l'avant — le « Go ». Au pivot exact entre l'arc
> et la flèche, un **point plein lumineux** : le clic, le nœud du réseau.
> Le tout tient dans un carré, parfaitement équilibré, lisible à 16 px.
>
> **Wordmark** : « Connect&Go » en une seule ligne, sans-serif grotesque
> contemporaine et légèrement condensée (esprit Bricolage Grotesque / Space
> Grotesk, graisse 700), crénage serré, pas de majuscules intégrales.
> « Connect » en encre claire, « &Go » en violet ; l'esperluette est le point
> de bascule du mot, légèrement plus lourde, elle peut reprendre la courbure
> de l'arc du symbole.
>
> **Couleurs** (strictement) : fond obsidienne `#0B0B16`, encre chaude
> `#F2EEE6`, dégradé violet linéaire `#C4B5FD → #6366F1`, cœur lumineux
> `#C4B5FD`. Deux couleurs maximum en simultané sur le signe.
>
> **Style** : vectoriel plat, trait constant, géométrie stricte, précision
> suisse, zéro effet. Pas d'ombre portée, pas de 3D, pas de biseau, pas de
> reflet, pas de texture, pas de dégradé de fond. L'élégance vient de la
> justesse des courbes, pas de l'ornement.
>
> **Livrables** : (a) lockup horizontal symbole + wordmark, (b) le symbole seul
> dans une pastille arrondie (rayon 24 %) pour avatar et favicon,
> (c) version monochrome une seule couleur pour l'impression.
> Présente-les sur fond sombre `#0B0B16` **et** sur fond clair.

## 2. Prompt maître (EN — Midjourney)

> Minimal geometric vector logo for **"Connect&Go"**, a solo digital studio
> building custom websites and mobile apps. Symbol: an open thick-stroke arc
> forming a "C" with rounded caps, opening rightward and resolving into a
> forward-pointing chevron — motion out of connection; a single glowing solid
> dot sits at the pivot, the click, the network node. Wordmark below or beside:
> "Connect&Go" in a contemporary condensed grotesque, weight 700, tight
> tracking, "Connect" in warm off-white `#F2EEE6`, "&Go" in a violet gradient
> `#C4B5FD → #6366F1`, the ampersand slightly heavier, echoing the arc.
> Obsidian background `#0B0B16`. Flat vector, constant stroke width, strict
> geometric grid, Swiss precision, legible at 16px. No shadow, no 3D, no bevel,
> no gloss, no texture, no mascot. Logo presentation sheet, generous negative
> space. --style raw --ar 3:2 --v 7

## 3. Trois pistes à faire tester en parallèle

1. **Le nœud qui repart** — deux arcs face à face (héritage du signe actuel),
   mais l'arc de droite s'ouvre en flèche ; le point central reste.
   *La piste la plus juste : elle capitalise sur l'identité déjà en ligne.*
2. **L'esperluette-lien** — le `&` devient le symbole : dessiné d'un seul trait
   continu où la boucle est un nœud et la queue une flèche. Monogramme parfait,
   très mémorisable, fonctionne seul sans le mot.
3. **C→G** — le « C » et le « G » emboîtés, le terminal du G formant la pointe
   de flèche ; le point lumineux dans le creux du G. Le plus corporate.

## 4. Liste de rejet (negative prompt)

`3D, dégradé arc-en-ciel, ombre portée, effet néon, glow diffus, mascotte,
globe, souris d'ordinateur, prise électrique, fusée, engrenage, mains qui se
serrent, swoosh générique, dégradé bleu-cyan SaaS, texte illisible ou
déformé, plus de deux couleurs, sérif, script, maillage, photo, texture papier,
badge circulaire type écusson, effet miroir/reflet de sol`

## 5. Contrôles avant validation

- Lisible en **16 × 16 px** (favicon) et gravé en une seule couleur.
- Le symbole reste compréhensible **sans** le wordmark.
- Fonctionne en **noir sur blanc** et en **blanc sur obsidienne**.
- Contraste du wordmark ≥ 4.5:1 sur `#0B0B16` (le violet clair `#C4B5FD` passe,
  l'indigo `#6366F1` ne passe pas en petit texte — le réserver aux grands aplats).
- Aucune lettre déformée par le générateur : vérifier « Connect&Go » caractère
  par caractère, l'esperluette surtout.
- Fournir en **SVG** final, texte vectorisé, comme `logo.svg` aujourd'hui.
