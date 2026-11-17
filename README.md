# Vingt Faces

Un « livre dont vous êtes le héros » sans rails, à la D&D, narré par une IA.
Tu écris librement ce que tu tentes ; selon la difficulté, tu lances un d20.

Tout le jeu tient dans un seul fichier : **`vingt-faces.html`**.

## Jouer

1. Ouvre `vingt-faces.html` dans Koder (aperçu / preview) ou dans n'importe quel navigateur.
2. Au premier lancement, colle ta clé API Anthropic (créée sur platform.claude.com → API keys).
   Elle reste sur ton appareil et n'est envoyée qu'à `api.anthropic.com`.
3. Crée ton héros, choisis un monde, et écris ce que tu veux.

## Ce qu'il y a dedans

- **Tout est possible** : texte libre, le narrateur fixe une difficulté au lieu de refuser.
- **Dés** : d20 + caractéristique + maîtrise + équipement contre un degré de difficulté ;
  20 naturel = réussite critique, 1 naturel = échec critique ; avantage / désavantage.
  C'est le programme qui lance le dé, pas l'IA.
- **Inventaire réel** : tout ce que tu ramasses devient un objet (quantité, type, valeur, bonus),
  que tu peux utiliser, équiper, examiner, donner ou jeter.
- **Sprites générés sur le coup** : chaque objet, chaque sort et le portrait du héros sont
  dessinés en pixel art 16×16 par l'IA au moment où ils apparaissent.
- **Magie limitée** : mana, coût par sort, magie improvisée plus chère et plus risquée,
  surcharge payée en points de vie, mana qui ne revient qu'avec le repos.
- **Vie, mort, niveaux** : points de vie, jet de la dernière chance à 0 PV, XP, niveaux,
  points de caractéristique, statuts, quêtes, lieux visités, chronique.
- **Sauvegardes** : automatique à chaque tour, bouton 💾, 3 emplacements, export / import par code.
- **DEV** : Réglages → DEV → code `BURGER` → mode dieu (immortel, mana et or infinis, dé forcé)
  et outils de test.

## Technique

- Modèle : `claude-sonnet-5-5`. Ouverte ailleurs que dans Claude, la page appelle l'API avec ta clé (effort `low`).
  Publiée comme artifact dans Claude, elle passe par ton compte Claude, sans clé (effort `medium`).
- Sorties structurées (JSON) pour l'arbitrage, streaming pour le récit, cache de prompt pour le coût.
- Aucune dépendance, aucun fichier externe.
