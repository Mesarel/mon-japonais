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

## Test 3 — Détection des conflits

- Deux journaux de 4 actions utilisés.
- Même identifiant pour une action différente.
- Valeur pointsDelta modifiée de 10 à 0.
- Conflit détecté : validé.
- Fusion refusée en présence du conflit : validé.
- Aucune donnée Supabase modifiée.

Résultat : le programme de test bloque la fusion lorsqu'un même identifiant correspond à des contenus différents.

## Test 4 — Fusion simulée entre deux appareils

- Journal appareil 1 : 4 actions.
- Journal appareil 2 : 5 actions, dont 4 communes.
- Actions reçues : 9.
- Actions uniques conservées : 5.
- Doublons écartés : 4.
- Points conservés : 40.
- Inversion de l'ordre des journaux : validée.
- Résultat identique dans les deux sens : validé.
- Aucune donnée Supabase modifiée.

Résultat : la fusion simulée conserve les actions distinctes
et évite le double comptage des actions communes.

Limite : la synchronisation automatique réelle et la
résolution des révisions concurrentes restent à développer.
