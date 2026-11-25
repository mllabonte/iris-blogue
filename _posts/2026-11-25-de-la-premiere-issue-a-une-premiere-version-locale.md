---
title: "De la première issue à une première version locale"
description: "Un échange avec Codex sur les premières issues d’IRIS, les prérequis qui manquaient et l’ordre dans lequel j’ai décidé d’avancer."
---

Je venais de classer les premières issues d’IRIS. Au moment d’en créer une sur GitHub, j’ai buté sur quelque chose de plus concret. Comment savoir ce qu’on veut tester quand on n’a encore jamais vu l’application à l’écran?

*J’ai condensé et reformulé les échanges ci-dessous pour le blogue, en gardant l’ordre des questions et des réponses.* [Montrer plutôt que raconter, INF 1410](https://cjauvin.github.io/inf1410-teluq/docs/travaux-not%C3%A9s/#montrer-plut%C3%B4t-que-raconter)

## Créer la première issue

**Moi.** Est-ce que je mets toutes mes user stories dans GitHub Issues ou seulement celles du noyau? Est-ce que je les fais moi-même dans VS Code?

**Codex.** Commence par le noyau. Crée toi-même une première issue avec GitHub CLI pour apprendre le geste. « Ajouter une prise réseau à l’inventaire » est un bon point de départ.

**Moi.** Le terminal ne reconnaît pas `gh`. Pourtant, il me semble qu’on avait déjà installé ce qu’il fallait pour `ci-demo`.

**Codex.** Pour `ci-demo`, tu avais utilisé Git et le bouton **Publish Branch** de VS Code. `gh` est GitHub CLI. Une fois installé et connecté à ton compte, il permet de créer une issue directement depuis le terminal.

**Moi.** La commande me montre un tableau avec `bug`, `documentation` et d’autres noms. C’est quoi?

**Codex.** Ce sont les labels disponibles dans le dépôt. Ajoute `story`, puis utilise-le pour classer ta première issue.

**Moi.** C’est fait. Je vois l’issue sur GitHub.

## Un critère qui suppose déjà un plan

**Moi.** Un des critères dit que la prise enregistrée apparaît à l’emplacement choisi sur le plan. Mais on n’a pas de plan et on n’a pas dit comment choisir l’emplacement. Il n’y a encore aucun programme!

**Codex.** L’issue décrit le résultat à atteindre. Elle fait ressortir un préalable à construire. Pour un premier essai, on peut fournir un plan fictif et permettre de cliquer dessus pour placer une prise. Un test peut aussi vérifier la règle qui empêche deux prises de revendiquer la même position de panneau.

**Moi.** J’aimerais quand même avoir une première vue. Je n’ai pas encore choisi comment l’application va s’afficher. J’ai l’impression de jouer à l’œuf ou la poule.

**Codex.** Fais une première vue assez simple pour l’essayer. Affiche un plan fictif et une prise, puis ajoute la possibilité de l’enregistrer. Recharge la page pour vérifier qu’elle est toujours là. Tu pourras préciser l’issue après avoir essayé le parcours.

## Où faire tourner IRIS?

**Moi.** Est-ce que le correcteur doit pouvoir ouvrir IRIS en ligne dès le premier jalon? Je comprends comment GitHub héberge le blogue. Comment ça marche pour une application qui enregistre des données?

**Codex.** L’application en ligne est exigée au jalon 4. Au jalon 1, tu peux la faire tourner sur ton portable. Django reçoit la demande d’enregistrement et écrit dans la base SQL. GitHub héberge le code et GitHub Actions exécute les tests.

**Moi.** Django, c’est le framework? Est-ce que je pourrai garder IRIS après le cours et le faire tourner dans Docker ou sur un serveur Windows au travail? Est-ce que la démo doit coûter quelque chose?

**Codex.** Oui, Django est le framework web. Les deux options d’hébergement interne sont possibles. Le cours n’impose aucun hébergeur payant. Pour IRIS, on envisage le même code dans deux installations, une démo en ligne avec des données fictives et une installation interne au cégep avec les vraies données.

## Remettre le travail dans l’ordre

**Moi.** Sans une base qui tourne, j’ai du mal à imaginer les autres issues et les premiers tests. Si je n’ai rien, comment tester?

**Codex.** Commence par ouvrir une page IRIS sur ton portable, avec Django et SQLite pour l’essai. Affiche une prise, puis enregistre-la depuis un formulaire. Ensuite, vérifie les deux conflits qu’on a définis. Une position déjà occupée dans le même panneau et un port déjà affecté sur le même commutateur doivent faire échouer l’ajout. GitHub Actions pourra lancer les mêmes tests à chaque push.

Je partais avec l’idée de remplir le backlog avant de toucher à l’application. En essayant de rédiger un seul critère, j’ai vu le moment où j’avais besoin d’une page devant moi. Mon prochain objectif tient en un geste. Ouvrir IRIS dans mon navigateur et savoir ce qui répond.
