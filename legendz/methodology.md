# Méthodologie hebdomadaire — Pool des Legendz

## Objectif
Maximiser les points attendus de l'alignement actif en choisissant correctement les 4 joueurs au banc et en utilisant avec prudence l'unique changement hebdomadaire.

## Structure du roster
Le roster comporte 24 sélections.

Le banc doit toujours contenir exactement :
- 2 attaquants
- 1 défenseur
- 1 gardien

Tous les autres choix comptent.

## Contraintes de l'alignement actif
- Maximum de 12 attaquants actifs
- Minimum de 2 défenseurs actifs
- Exactement 2 gardiens actifs

## Calendrier des périodes
La semaine standard va du dimanche au samedi.

La première période du 29 septembre au 3 octobre 2026 autorise 255 changements et est traitée comme une période spéciale.

À partir du 4 octobre :
- 1 seul changement d'alignement par semaine
- changement effectif immédiatement

## Principe d'optimisation
Le rapport hebdomadaire doit surtout répondre à deux questions :

1. Quels sont les 4 joueurs à laisser au banc?
   - 2 attaquants
   - 1 défenseur
   - 1 gardien

2. L'unique changement hebdomadaire vaut-il réellement la peine?

Avec seulement un changement par semaine, un changement de court terme doit être beaucoup plus fortement pénalisé qu'au pool des Comptables.

## Continuité inter-semaines
Toute recommandation doit considérer l'alignement hérité au début de la semaine suivante.

Le modèle doit utiliser une fenêtre glissante d'environ 7 à 10 jours et éviter les rental switches qui forceraient un changement inverse dès la semaine suivante.

### Types de changement

#### Sustainable switch
Le joueur entrant améliore ou maintient la valeur cette semaine et la suivante.
- Priorité élevée.

#### Short-term switch
Le gain est surtout immédiat mais demeure acceptable pour la semaine suivante.
- Priorité moyenne.

#### Rental switch
Le changement sert surtout à aller chercher un ou quelques matchs et crée un risque élevé de devoir revenir en arrière.
- À éviter sauf gain attendu important.

## Disponibilité
La blessure, la suspension, le retranchement ou le risque de scratch doivent être évalués avant le ranking.

- Vert : disponible normalement
- Jaune : incertain / day-to-day / game-time decision
- Rouge : OUT / IR / suspendu / retranché

Un joueur rouge devrait être prioritaire pour le banc.

## Volume de matchs
Le nombre de matchs attendus demeure un facteur majeur.

Pour les gardiens, utiliser les départs projetés plutôt que le nombre de matchs de l'équipe.

## Qualité et rôle
Évaluer :
- projection de points
- temps de glace
- PP1 / PP2
- ligne
- partenaires
- rôle récent

## Forme récente
Évaluer principalement les 5 derniers matchs :
- points
- tirs
- TOI
- production sur le PP
- évolution du rôle

## Opposition
Évaluer :
- forme des 10 derniers matchs de l'adversaire
- buts accordés
- PK
- gardien probable
- fatigue / back-to-back
- domicile / extérieur

## Agents libres
Même si PoolExpert peut afficher des options liées aux joueurs non repêchés, les règles maison du pool n'autorisent pas l'ajout d'agents libres.

Aucune recommandation ne doit donc proposer un joueur non repêché.

## Format recommandé du rapport

### Banc recommandé
- 2 attaquants
- 1 défenseur
- 1 gardien

### Alignement actif
Tous les autres joueurs.

### Changement hebdomadaire potentiel
Si un changement est recommandé :
- jour recommandé
- joueur sortant
- joueur entrant
- gain attendu
- effet sur la semaine suivante
- classification : Sustainable / Short-term / Rental
- niveau de confiance

### À surveiller
- blessures
- changements de trio
- PP
- gardiens confirmés
- calendrier
- éventuels changements de rôle


## Pondération officielle V1 — Legendz

### Patineurs

| Critère | Poids |
|---|---:|
| Matchs attendus | 25 % |
| Projection + rôle | 30 % |
| Forme récente | 10 % |
| Opposition | 8 % |
| Distribution du calendrier | 7 % |
| Continuité / valeur stratégique | 20 % |

Total : 100 %

### Détail de Projection + rôle
- Projection de points : 13
- PP1 / PP2 : 6
- Temps de glace attendu : 4
- Ligne à forces égales : 3
- Qualité des partenaires : 4

## Modèle spécifique aux gardiens

| Critère | Poids |
|---|---:|
| Départs projetés | 30 % |
| Qualité / projection du gardien | 20 % |
| Probabilité de victoire | 15 % |
| Opposition | 10 % |
| Forme récente | 5 % |
| Probabilité de blanchissage | 5 % |
| Distribution du calendrier | 5 % |
| Continuité vers la semaine suivante | 10 % |

Total : 100 %

## Contraintes du ranking
- Ne jamais comparer directement des joueurs de positions différentes pour décider du banc.
- Le système doit choisir exactement 2 attaquants, 1 défenseur et 1 gardien pour le banc.
- Les équipes NHL restent actives et ne sont pas rankées.
- Aucun joueur non repêché ne peut être proposé.
- Un seul changement peut être recommandé par semaine.
- Tout changement doit être évalué sur une fenêtre glissante de 7 à 10 jours.

## Règle Rental switch
Un Rental switch ne devrait généralement pas être recommandé pour un gain attendu inférieur à environ 1 point.

Ce seuil constitue une hypothèse V1 et devra être validé avec les résultats réels du pool.
