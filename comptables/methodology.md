# Méthodologie hebdomadaire — Pool des Comptables

## Objectif
Maximiser les points attendus de l'alignement actif tout au long de la période hebdomadaire, tout en respectant la limite de deux changements et les contraintes de position.

L'équipe NHL sélectionnée (Minnesota Wild) est toujours active et n'est pas incluse dans le ranking des joueurs.

## Contraintes d'alignement
L'alignement actif doit toujours respecter :
- 8 attaquants
- 2 défenseurs
- 1 gardien
- 1 équipe NHL

## Processus standard
1. Vérifier le calendrier complet de la période.
2. Vérifier la disponibilité de chaque joueur.
3. Vérifier blessures, suspensions, retranchements, transactions et risques de scratch.
4. Estimer le nombre de matchs réellement attendus de chaque patineur.
5. Pour les gardiens, estimer le nombre probable de départs.
6. Vérifier le rôle actuel : trio, partenaires, TOI, PP1 / PP2.
7. Évaluer la forme récente individuelle sur les 5 derniers matchs.
8. Évaluer la difficulté des adversaires.
9. Analyser la distribution des matchs dans la semaine.
10. Calculer la valeur stratégique potentielle des changements.
11. Produire l'alignement recommandé et les options de changement.

## Rank 1 — Disponibilité
La disponibilité agit comme un filtre avant le score pondéré.

### Vert
Joueur disponible normalement.
- Multiplicateur : 1.00

### Jaune
Joueur incertain : day-to-day, game-time decision, retour progressif ou statut similaire.
- Le score reste calculé.
- Le score final est multiplié par la probabilité estimée de jouer.

Exemple :
- score hockey : 84
- probabilité de jouer : 60 %
- score ajusté : 50,4

### Rouge
OUT, IR, suspendu ou retranché.
- Recommandation automatique au banc, sauf exception explicitement documentée.

## Rank 2 — Nombre de matchs attendus — 30 %
Le volume de matchs est un facteur majeur puisque le pool compte les points bruts.

Il faut utiliser les matchs réellement attendus, et non seulement les matchs inscrits au calendrier.

Pour les gardiens, on utilise les départs projetés.

## Rank 3 — Projection et rôle — 35 %
Cette catégorie mesure la qualité intrinsèque de l'opportunité du joueur.

Répartition interne :
- Projection de points : 15
- PP1 / PP2 : 7
- Temps de glace attendu : 5
- Ligne à forces égales : 4
- Qualité des partenaires : 4

Une hausse récente de rôle doit être intégrée rapidement.

## Rank 4 — Forme récente — 12 %
Fenêtre principale : 5 derniers matchs.

Indicateurs :
- points
- tirs
- TOI
- production en avantage numérique
- changement de trio ou de rôle

La production brute ne doit pas être utilisée seule. Une séquence appuyée par une hausse de rôle est plus crédible qu'une séquence basée uniquement sur un pourcentage de tir élevé.

## Rank 5 — Opposition — 8 %
Évaluer notamment :
- forme des 10 derniers matchs de l'adversaire
- buts accordés
- penalty kill
- gardien adverse probable
- back-to-back
- domicile / extérieur

Ce critère sert surtout à départager des joueurs relativement proches.

## Rank 6 — Distribution du calendrier — 7 %
Analyser les jours exacts où les joueurs jouent.

Objectif :
- exploiter les séquences de matchs
- identifier les trous de calendrier
- profiter des back-to-back
- repérer les complémentarités entre un titulaire et un joueur du banc

Exemple :
un joueur actif lundi-mardi peut être remplacé plus tard par un joueur qui joue jeudi-vendredi-samedi.

## Rank 7 — Valeur stratégique du changement — 8 %
Chaque changement doit être évalué en fonction de sa valeur nette, et non seulement de son gain immédiat.

### Net Strategic Gain

La base demeure :

```text
points attendus du joueur entrant pour le reste de la période
-
points attendus du joueur sortant pour le reste de la période
=
gain attendu immédiat
```

Mais la recommandation finale doit aussi considérer la semaine suivante.

Le modèle doit fonctionner sur une fenêtre glissante d'environ 7 à 10 jours :

1. reste de la semaine actuelle;
2. début et calendrier de la semaine suivante;
3. coût potentiel d'un changement inverse;
4. coût d'opportunité lié à l'utilisation d'un changement futur.

Exemple :
- joueur sortant : 2 matchs restants × 0,55 = 1,10 point attendu
- joueur entrant : 4 matchs restants × 0,65 = 2,60 points attendus
- gain attendu immédiat = +1,50

Ce gain peut toutefois être réduit si le joueur entrant possède un mauvais calendrier la semaine suivante et qu'il faudra utiliser un nouveau changement pour revenir au joueur initial.

### Types de changement

#### Sustainable switch
Le joueur entrant améliore ou maintient la valeur de l'alignement cette semaine et la suivante.
- Priorité élevée.

#### Short-term switch
Le changement améliore surtout la semaine actuelle, mais reste raisonnablement défendable pour la semaine suivante.
- Priorité moyenne.

#### Rental switch
Le changement vise principalement un ou quelques matchs à très court terme et risque de forcer un changement inverse au début de la semaine suivante.
- Priorité faible sauf gain attendu significatif.

Un changement de fin de semaine ne doit donc jamais être recommandé uniquement parce qu'il ajoute un match. Le système doit d'abord vérifier l'alignement qui sera hérité le lundi suivant.

## Pondération officielle V1 — Patineurs

| Critère | Poids |
|---|---:|
| Matchs attendus | 30 % |
| Projection + rôle | 35 % |
| Forme récente | 12 % |
| Opposition | 8 % |
| Distribution du calendrier | 7 % |
| Valeur stratégique du changement | 8 % |

Total : 100 %

## Modèle spécifique aux gardiens
Les gardiens sont évalués séparément.

| Critère | Poids |
|---|---:|
| Départs projetés | 35 % |
| Qualité / projection du gardien | 25 % |
| Probabilité de victoire | 20 % |
| Qualité de l'adversaire | 10 % |
| Forme récente | 5 % |
| Probabilité de blanchissage | 5 % |

Total : 100 %

Le nombre de matchs de l'équipe ne doit jamais être utilisé comme substitut direct au nombre de départs projetés.

## Format du rapport hebdomadaire
Le rapport doit idéalement contenir :

### Alignement recommandé
- 8 attaquants
- 2 défenseurs
- 1 gardien

### Banc
- 4 joueurs

### Changements potentiels
Pour chaque changement proposé :
- jour recommandé
- joueur sortant
- joueur entrant
- matchs restants
- points attendus avant / après
- gain attendu
- niveau de confiance

### À surveiller
- blessures
- game-time decisions
- changement de trio
- changement de PP
- gardien confirmé ou non
- transaction ou rappel

## Gouvernance du modèle
Cette version constitue la V1 officielle.

Les poids ne doivent pas être modifiés de façon opportuniste après une mauvaise semaine. Les ajustements doivent reposer sur :
- plusieurs semaines de résultats;
- une faiblesse récurrente observée;
- ou une décision explicite documentée.

Toute modification importante doit être versionnée dans GitHub.
