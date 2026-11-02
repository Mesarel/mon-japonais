# Mon Japonais V0.6 — Environnement de test

## Objectif
Préparer une synchronisation automatique sécurisée entre PC et téléphone.

## Test 1 — Journal local
- Enregistrement des réponses correctes : validé
- Enregistrement des réponses incorrectes : validé
- Conservation du journal après réouverture : validé
- Enregistrement hors connexion simulée : validé
- Identifiants uniques des actions : validé
- Dates des actions : validé

## Test 2 — Détection des doublons
- Actions présentes dans le journal original : 4
- Actions simulées avec deux copies : 8
- Actions uniques attendues après déduplication : 4
- Points attendus après déduplication : 30

## Sécurité
- Tests réalisés avec Firefox TEST
- Aucune synchronisation Supabase activée
- Site principal V0.5.2 conservé sur main
- Progression principale : 160 points et 18 mots
