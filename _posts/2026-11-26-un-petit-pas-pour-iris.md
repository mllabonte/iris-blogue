---
title: "Un petit pas pour IRIS…"
description: "De la page de bienvenue de Django à l’affichage d’une première prise fictive dans mon navigateur."
---

Dans le billet précédent, j’en étais à vouloir ouvrir une première page IRIS sur mon portable. Django répondait déjà avec sa page de bienvenue. Cette fois, je voulais voir une prise réseau à l’écran, même avec des données fictives. J’ai ouvert Codex dans VS Code et je lui ai demandé de reprendre à partir des notes du projet.

## La première page IRIS

*Première séance. Dialogue abrégé et reformulé à partir de mon échange avec Codex dans VS Code.*

**Moi.** Lis le fichier de reprise et guide-moi une étape à la fois.

**Codex.** Lance `Test-Path .\manage.py` dans PowerShell pour vérifier que tu es à la racine du projet.

**Moi.** J’obtiens `True`. Dans `config/urls.py`, je vois `path('admin/', admin.site.urls)`.

**Codex.** C’est l’adresse de l’administration. Pour la page d’accueil `/`, ajoute une route avec une chaîne vide et relie-la à une fonction `accueil`. Pour commencer, cette fonction peut renvoyer une simple réponse texte.

**Moi.** J’actualise la page et je vois le texte que j’ai écrit dans `views.py`.

**Codex.** Ton navigateur demande la page d’accueil, Django trouve la route et appelle ta fonction. Pour structurer la page, crée maintenant un gabarit HTML dans le dossier `templates`, à côté de `manage.py`.

**Moi.** J’avais créé le dossier sous `config`. Je l’ai déplacé à la racine.

**Codex.** Indique l’emplacement du dossier dans `settings.py`. Dans la vue, rassemble les valeurs dans un dictionnaire et donne-le à `render()`. Django placera l’étiquette, le panneau et le port aux endroits indiqués dans le gabarit.

**Moi.** J’actualise et je vois **Prise A102-005**, **Panneau A — position 05** et **SW-01 — port 12**.

### Garder une trace du changement

**Moi.** Je veux pousser ces changements sur GitHub. Guide-moi.

**Codex.** Vérifie d’abord les fichiers modifiés avec `git status --short --branch`. Sélectionne les quatre fichiers, puis vérifie la sélection avec `git diff --cached --stat`.

**Moi.** Les quatre fichiers sont sélectionnés. J’ai créé le commit avec mon propre message, puis je l’ai poussé sur GitHub.

La page affiche maintenant ce que je lui donne depuis le code Python. Au premier essai, c’était une ligne de texte. Ensuite, j’ai pu voir comment le gabarit prenait ces mêmes renseignements et les plaçait à l’écran. La prochaine étape sera d’enregistrer une prise dans SQLite et de la retrouver après avoir rechargé la page. Je reviendrai à ce billet au fil des premières séances de codage.
