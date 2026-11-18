# Politique de sécurité — Miza (ميزة)

## Signaler une vulnérabilité

Si vous découvrez une vulnérabilité de sécurité dans Miza, veuillez la signaler de manière responsable.

**Ne PAS ouvrir un ticket GitHub public pour des vulnérabilités de sécurité.**

Contactez directement le mainteneur : **Amen Allah Ben Abdrabah**
- GitHub : [@amenallah00](https://github.com/amenallah00)
- Institution : ENICarthage, Tunisie

### Ce qu'il faut inclure

- Description de la vulnérabilité
- Étapes pour reproduire
- Impact potentiel
- Correction suggérée (si applicable)

### Délai de réponse

- Accusé de réception sous 48 heures
- Mise à jour de statut sous 7 jours
- Correction et divulgation coordonnées avec le rapporteur

## Versions supportées

| Version | Supportée |
|---------|-----------|
| latest  | Oui       |

## Bonnes pratiques pour l'auto-hébergement

- Toujours changer la `SECRET_KEY` par défaut en production
- Utiliser HTTPS en production
- Maintenir les dépendances à jour
- Restreindre l'accès à la base de données au service backend uniquement
- Vérifier les variables d'environnement avant le déploiement
