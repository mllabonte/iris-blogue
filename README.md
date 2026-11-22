# Blogue technique IRIS

Le site utilise Jekyll pour afficher les articles Markdown sur GitHub Pages.

## Activer GitHub Pages

1. Ouvrir **Settings > Pages** dans le dépôt.
2. Sous **Build and deployment**, choisir **Deploy from a branch**.
3. Choisir **main** et **/ (root)**, puis cliquer sur **Save**.
4. Ouvrir le lien affiché dans **Settings > Pages** après le déploiement.

## Ajouter un article

1. Créer `_posts/AAAA-MM-JJ-titre-en-minuscules.md` avec la date d'écriture.
2. Inscrire le titre et le résumé dans l'en-tête YAML.
3. Rédiger le texte en Markdown sous l'en-tête.
4. Envoyer le commit sur GitHub. L'article apparaîtra sur la page d'accueil après la publication.

```markdown
---
title: "Titre de l’article"
description: "Une ou deux phrases pour présenter le sujet."
---

L’ouverture décrit une situation concrète.

## Le problème sur le terrain

## L’approche envisagée

## Les décisions et les questions ouvertes
```

Un brouillon peut rester dans le dépôt privé du cours jusqu'à sa publication. Ajouter seulement des images destinées au public.
