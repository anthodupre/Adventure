# Vingt Faces

Un « livre dont vous êtes le héros » sans rails, à la D&D, narré par une IA.
Tu écris librement ce que tu tentes ; selon la difficulté, tu lances un d20.

Tout le jeu tient dans un seul fichier : **`vingt-faces.html`**.

## Jouer

- **Dans Claude** : publié comme artifact, le jeu passe par ton compte Claude, sans clé.
- **Dans Koder ou un navigateur** : ouvre `vingt-faces.html` et colle ta clé API Anthropic
  (platform.claude.com → API keys). Elle reste sur ton appareil et n'est envoyée qu'à `api.anthropic.com`.

## Modèles

- Récit et arbitrage : `claude-sonnet-5-5`, effort `high`.
- Sprites : `claude-haiku-5-5`, effort `high`. Chaque sprite est dessiné sur le moment pour cet objet,
  ce personnage ou ce pouvoir précis, dans la direction artistique du monde ; rien n'est réutilisé d'une partie à l'autre.

## Ce qu'il y a dedans

- **21 mondes + un monde sur mesure**, chacun avec ses 10 archétypes, son vocabulaire (nom des pouvoirs, de l'énergie,
  de la monnaie) et sa direction artistique. Archétype sur mesure possible (profil, caractéristiques fortes, compétences).
- **10 situations de départ**, ou la tienne.
- **Dés** : d20 + caractéristique + maîtrise de compétence (22 compétences) + équipement, contre une difficulté ;
  20 naturel = réussite critique, 1 naturel = échec critique ; avantage / désavantage. C'est le programme qui lance le dé.
- **Inventaire réel** en 14 catégories, 5 raretés, filtres, tri, recherche, et 6 emplacements d'équipement.
- **Pouvoirs limités** : coût en énergie, pouvoirs improvisés plus chers, surcharge payée en points de vie.
- **Combat** : bandeau des adversaires avec leurs points de vie.
- **Monde** : quêtes, personnages rencontrés (avec portraits et attitude), factions et réputation,
  carte des lieux visités qui se dessine toute seule, chronique, notes personnelles.
- **Progression** : niveaux, points de caractéristique, nouvelles compétences, 18 succès, Panthéon des héros tombés.
- **Lecture** : thèmes Nuit / Parchemin / Contraste / Auto, trois polices de récit, taille et interligne réglables.
  Dans Claude : lecture à voix haute et dictée quand l'appareil le permet.
- **Sauvegardes** : automatique à chaque tour, bouton Sauver, 3 emplacements, export / import par code.
- **DEV** : Options → DEV → code `BURGER` → mode dieu (immortel, énergie et argent infinis, dé forcé) et outils de test.
