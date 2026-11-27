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

La page affiche maintenant ce que je lui donne depuis le code Python. Au premier essai, c’était une ligne de texte. Ensuite, j’ai pu voir comment le gabarit prenait ces mêmes renseignements et les plaçait à l’écran. Cette première fiche m’a donné un point de départ pour l’essai suivant.

## Naviguer dans le plan

*27 novembre 2026. Échange condensé à partir de la séance dans VS Code.*

J’ai repris dans VS Code le plan de travail préparé avec Codex dans le cloud. Je voulais essayer la navigation sur une grande image avant de construire le formulaire. Un plan de cette taille doit rester maniable même quand on zoome pour lire un petit numéro de local.

**Moi.** Commençons par une grande image fictive, le zoom, le déplacement et un repère fixe. Je veux essayer ça dans le navigateur avant d’ajouter le formulaire.

**Vex (Codex dans VS Code).** Le plan fictif de 2 400 × 1 500 pixels s’affiche à gauche et la fiche A102-005 à droite. Dans Chrome, j’ai vérifié que la molette zoome vers le pointeur, que la roulette maintenue permet de déplacer le plan et que le repère reste au bon endroit après un redimensionnement.

**Moi.** Est-ce que je peux aussi déplacer le plan en maintenant le clic gauche dans une zone libre? Je trouve ce geste intuitif.

**Vex.** Oui. Tu peux maintenant glisser le plan avec le clic gauche ou la roulette. Si le geste commence sur le repère ou son étiquette, le plan reste en place.

**Moi.** À quoi sert le dossier `static/`?

**Vex.** Django remplit le gabarit HTML avec les données de la prise. Le navigateur télécharge ensuite l’image, le CSS et le JavaScript. Le JavaScript fait bouger le plan et le repère ensemble à l’intérieur du cadre.

### Le premier push refusé

J’avais sélectionné seulement le dossier `static/` pour mon commit. L’image, le CSS et le JavaScript y étaient, mais j’avais oublié le gabarit et la configuration Django. Au moment du `push`, GitHub a aussi refusé l’envoi avec le message `non-fast-forward`.

**Vex.** Il y a deux choses à régler. Complète ton commit avec les deux fichiers manquants. Ensuite, récupère les quatre commits de documentation déjà sur GitHub et réapplique ton commit par-dessus avec `git pull --rebase origin main`. L’avertissement sur les fins de ligne Windows n’a pas causé le refus.

**Moi.** Est-ce que ça risque de briser le travail fait sur la page du plan?

**Vex.** Les quatre commits touchent la documentation. Ton commit porte sur les fichiers du plan. Après le rebase, recharge la page et réessaie le déplacement au clic gauche.

C’est ce que j’ai fait. Le plan fonctionnait encore et le commit a été poussé sur GitHub. Je retiens deux gestes pour la prochaine fois. Je vérifie les fichiers sélectionnés avec `git diff --cached --stat`. Avant de pousser, je peux faire `git fetch origin`, puis `git status --short --branch`, pour voir si GitHub a avancé pendant que je travaillais.

La prochaine étape sera de cliquer sur **Ajouter une prise**, de placer un repère provisoire sur le plan et de faire apparaître ses champs dans la fiche de droite. Je pourrai essayer le placement et l’annulation dans le navigateur avant de passer à l’enregistrement dans SQLite.

Je referme ce fil et, dans VS Code, Codex renaît sous le nom de Vex. Désormais, le va-et-vient que je garde, c’est celui du plan sous ma souris.
