# AGENTS.md — Instructions permanentes du projet

## Règle principale

Avant toute intervention, tu dois lire la documentation du projet et examiner le code existant.

## Documents obligatoires à consulter

1. README.md
2. docs/CURRENT_STATE.md
3. docs/AI_HANDOVER.md
4. docs/FEATURES.md
5. docs/KNOWN_ISSUES.md
6. docs/ARCHITECTURE.md

## Protection de l'existant

- Ne jamais recréer une fonctionnalité existante.
- Ne jamais remplacer un composant fonctionnel sans justification.
- Ne jamais supprimer des données.
- Ne jamais réinitialiser PostgreSQL.
- Ne jamais supprimer ou réécrire une migration déjà appliquée.
- Ne jamais modifier une fonctionnalité sans examiner ses dépendances.
- Préserver la compatibilité avec Coolify.

## Développement

- Respecter TypeScript.
- Réutiliser les composants existants.
- Respecter l'architecture du projet.
- Valider les données côté serveur.
- Tester chaque modification significative.
- Documenter chaque changement important.

## Base de données

- PostgreSQL est la source de vérité.
- Prisma gère le schéma et les migrations.
- Toute modification structurelle doit avoir une migration.
- Les migrations de production doivent être non destructives par défaut.
- Ne jamais utiliser db push ou une réinitialisation destructive en production.

## Documentation

Après chaque intervention, mettre à jour les documents concernés :

- CURRENT_STATE.md
- FEATURES.md
- CHANGELOG.md
- KNOWN_ISSUES.md
- AI_HANDOVER.md si nécessaire.

Ne jamais déclarer une fonctionnalité terminée sans validation.

## Rapport final

À chaque intervention, indiquer :

- Ce qui existait avant.
- Ce qui a été modifié.
- Ce qui a été ajouté.
- Les tests réellement effectués.
- L'état du déploiement.
- Les éventuelles régressions.
- Les problèmes restants.
- La prochaine étape recommandée.

**Ne jamais sacrifier la stabilité du projet pour gagner du temps.**
