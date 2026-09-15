# Entrainement de la VMA... et du cerveau

Trois jeux d'équipe pour un cycle de course à pied, conçus pour un écran interactif tactile posé dans un gymnase. Le principe est toujours le même : **chaque course rapporte une action sur l'écran**, et l'énigme se résout pendant la récupération.

L'application tient dans une page web autonome. Pas de serveur, pas de compte, pas de connexion nécessaire une fois chargée.

---

## Pourquoi ces trois jeux

Les trois sollicitent une compétence mentale différente, ce qui fait tourner les rôles dans l'équipe et donne leur chance aux élèves qui ne brillent ni en EPS ni en classe.

| Jeu | Compétence | Une course donne droit à |
|---|---|---|
| Mastermind | Déduction combinatoire | Une proposition de code |
| Memory | Mémorisation et transmission orale | Une carte retournée |
| Bataille navale | Déduction spatiale | Un tir |

Aucun des trois ne demande de prérequis scolaire, et dans les trois **chaque équipe avance sur sa propre piste** : l'ordre de retour des coureurs n'a aucune importance, ce qui est indispensable quand les groupes de VMA rentrent en désordre.

## Règles de course à poser avant de commencer

- Chaque élève pose son plot à sa distance personnelle. Pour 30 secondes à 100 % de VMA : **distance = VMA × 8,33** (VMA 12 → 100 m, donc plot à 50 m en aller-retour).
- Un coéquipier chronomètre. **Hors de la fourchette 28 à 32 secondes, l'action est annulée.** Sans cette règle, les élèves sprintent pour gagner des tours et se grillent en trois passages.
- **Seul le coureur qui vient de rentrer touche l'écran.** Les autres restent à trois mètres et conseillent à la voix. C'est la règle qui évite l'attroupement et qui fait tourner la prise de décision.

## Format d'une leçon de 35 minutes

| Temps | Contenu |
|---|---|
| 0–4 min | Mise en place des plots, explication du jeu |
| 4–12 min | Manche 1 |
| 12–15 min | Pause active, annonce du jeu suivant |
| 15–23 min | Manche 2 |
| 23–26 min | Pause |
| 26–34 min | Manche 3 |
| 34–35 min | Classement |

Soit 7 à 9 répétitions de 30 secondes à 100 % de VMA par élève, avec un rapport travail/récupération autour de 1 pour 4.

## Note sur le Memory

**Place l'écran au point de demi-tour, dos à la zone d'attente.** Si les non-coureurs voient l'écran, ils voient aussi les cartes des autres équipes, tout le monde dispose de la même information et le jeu se réduit à une course à qui annonce le premier.

La transmission orale est le cœur du jeu. Progression conseillée :

1. **Manche 1, rien.** Les élèves découvrent que retenir douze positions de tête, à quatre, ne fonctionne pas.
2. **Manche 2, une feuille blanche et un crayon par équipe.** Pas de grille pré-imprimée : ils vont dessiner eux-mêmes le rectangle de 6 sur 4. Faire le lien entre organisation spatiale de l'information et fiabilité est un vrai contenu de leçon, à débriefer en trois minutes à la fin.

Impose que le coureur **annonce sa carte à voix haute dès son arrivée**, avant que quiconque écrive.

---

## Utilisation de l'application

- **Accueil** : score cumulé de chaque équipe dans son rectangle de sautoir, liseré blanc pour l'équipe en tête, et les trois jeux avec leur état.
- **Terminer la manche** : calcule le classement, attribue un point à l'équipe en tête (ou à toutes les équipes à égalité) et ramène à l'accueil.
- **Réglages** : nombre d'équipes de 2 à 5, durée de révélation du Memory, taille de la grille de bataille navale.
- **Plein écran** et maintien de l'écran allumé, dans le coin de l'accueil.
- La partie est **sauvegardée automatiquement** dans le navigateur : un rafraîchissement de page ou une coupure de courant ne fait rien perdre.

### Réglages conseillés

| Situation | Réglage |
|---|---|
| Classe jeune ou en difficulté | Memory à 3 s, bataille navale en 8 × 8 |
| Classe à l'aise | Memory à 1,5 s, bataille navale en 10 × 10 |
| Manches courtes (moins de 6 min) | Bataille navale en 8 × 8 obligatoirement |

## Installation sur un écran interactif

Les écrans Legamaster récents (gamme Evolve 2, certifiés Google EDLA) donnent accès au Play Store.

1. Installer **Chrome** depuis le Play Store.
2. Ouvrir l'adresse du dépôt publié, puis menu ⋮ → **Ajouter à l'écran d'accueil**.
3. L'application se lance ensuite comme une vraie app, sans barre d'adresse, en plein écran.
4. Dans les réglages d'affichage de l'écran, mettre l'**extinction automatique sur « jamais »** ou sur une durée supérieure à la leçon.

Après une première ouverture en ligne, l'application fonctionne **sans réseau** : le service worker garde tout en cache.

Sur un modèle plus ancien sans Play Store, le navigateur intégré suffit ; utiliser le bouton « Plein écran » de l'accueil.

## Contenu du dépôt

```
index.html      l'application entière (HTML, CSS, JS, pictogrammes SVG)
manifest.json   pour l'installation sur l'écran d'accueil
sw.js           cache hors connexion
icon-192.png    icônes de l'application
icon-512.png
```

Aucune dépendance externe, aucune bibliothèque, aucune police à télécharger.

## Modifier

Tout est dans `index.html`. Les points les plus utiles :

- `ALL_TEAMS` : noms et couleurs des sautoirs.
- `COLORS` : les six couleurs de plots du Mastermind.
- `SPORTS` : les douze pictogrammes, dessinés en SVG.
- `FLEET` : composition de la flotte de la bataille navale.
- `CFG` : valeurs par défaut des réglages.

## Licence

MIT. Utilisation, modification et partage libres, y compris en classe.
