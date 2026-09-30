# NHL Pool Management

Dépôt de gestion hebdomadaire pour les pools NHL de Kémy.

## Objectif
Standardiser les rapports hebdomadaires, conserver les rosters, documenter les critères de classement et garder un historique des décisions.

## Pools
- `comptables/`
- `legendz/`

Chaque pool possède son propre roster, sa méthodologie, ses règles de scoring, ses critères de ranking et ses rapports hebdomadaires.

## Principe
Le classement hebdomadaire doit être reproductible et basé sur des critères documentés. Toute exception manuelle importante doit être consignée.

## Structure
```text
nhl-pool-management/
├── comptables/
│   ├── roster.yaml
│   ├── methodology.md
│   ├── scoring_rules.yaml
│   ├── ranking_weights.yaml
│   ├── manual_overrides.csv
│   └── reports/
└── legendz/
    ├── roster.yaml
    ├── methodology.md
    ├── scoring_rules.yaml
    ├── ranking_weights.yaml
    ├── manual_overrides.csv
    └── reports/
```
