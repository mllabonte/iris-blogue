---
title: "Qu’est-ce qui doit exister en premier dans IRIS?"
description: "En reprenant mon plan de conception, j’ai classé les idées d’IRIS selon ce qu’elles changent dans le travail de l’équipe réseau."
---

En relisant le plan de conception d’IRIS, j’ai repris toutes les idées qui pourraient devenir des issues. Je reconnaissais chaque besoin, mais ils n’avaient plus tous la même urgence quand je les ramenais à une journée de travail. Certains déterminent si je peux me servir de l’application. D’autres me donneraient envie de l’ouvrir en premier avant d’aller sur le terrain.

J’ai repris le plan section par section et j’ai regardé ce que chaque proposition changeait pour l’administrateur ou l’opérateur. Codex m’a aidé à organiser les idées, à repérer les recoupements et à mettre les dépendances dans l’ordre. J’ai précisé les priorités à partir de nos interventions et de ce que je veux pouvoir faire avec une première version.

## De la vision client au backlog

| Étape | Ce que j’ai demandé ou décidé | Résultat |
| --- | --- | --- |
| **1. Partir de la vision client** | Je voulais comprendre les issues avant d’en créer. L’exemple RéservaSalle du module 4 m’a donné un point de départ. | La formule « En tant que…, je veux…, afin de… » m’a permis de relier chaque proposition à un besoin. |
| **2. Reprendre mon plan** | J’ai demandé à Codex de reprendre mon plan section par section, de proposer les issues correspondantes et de relever les idées ajoutées depuis. | J’ai obtenu une première liste couvrant la gestion des prises, la consultation, la validation et les intégrations. |
| **3. Revoir les propositions** | J’ai précisé les labels `story` et `tech`, ajouté la distinction visuelle des types de pose et demandé de séparer les intégrations Meraki et Poly. | J’ai regroupé les façons de consulter le raccordement d’une prise dans une même fiche pour l’opérateur. La gestion des panneaux et le traitement des signalements sont restés des tâches distinctes. |
| **4. Réduire la portée** | J’ai reporté la détection des superpositions, la numérotation automatique et la reprise de l’inventaire. J’ai placé le copier-coller des descriptions avant SNMP et remis l’écriture sur les commutateurs à plus tard. | J’ai retenu 28 propositions pour le classement. Les idées mises de côté restent consignées dans mes notes. |
| **5. Classer par priorité** | J’ai distingué ce qui fait fonctionner IRIS, ce qui le rend utile au quotidien et ce qui pourrait en faire l’outil que j’ouvre en premier. | J’ai réparti le backlog entre le **noyau**, les **ajouts requis au noyau**, les **ajouts souhaités** et les **améliorations futures**. |

## Noyau

Le noyau est le minimum qui permet de faire fonctionner IRIS. Je veux pouvoir tenir l’inventaire à jour et suivre le raccordement d’une prise entre le plan et le panneau. Si ce parcours tient avec quelques prises, j’ai déjà quelque chose à utiliser et à tester.

## Ajouts requis au noyau

À ce niveau, le programme fonctionne déjà. Je me demande alors s’il ferait du sens dans notre travail. Un inventaire peut s’ouvrir et afficher ses données, mais j’ai besoin de pouvoir comprendre ce que je vois, repérer les écarts et retrouver le contexte d’une correction. C’est là que la confiance dans la documentation commence à se construire.

## Ajouts souhaités

Ce sont les choses qui pourraient rendre IRIS indispensable à mes yeux. Je pense aux gestes qu’on répète à chaque intervention et aux renseignements qu’on finit toujours par aller chercher ailleurs. Si IRIS m’épargne assez de ces détours, il peut devenir le premier endroit où je regarde. Entre-temps, l’équipe peut continuer de travailler avec les fonctions déjà en place.

## Améliorations futures

Certaines idées auront plus de sens une fois qu’on aura essayé IRIS dans des situations concrètes. Je les ai gardées avec les raisons qui m’y avaient fait penser. Quand j’y reviendrai, je pourrai juger si le besoin est toujours là et si l’inventaire est prêt à les accueillir.

Ce tri me ramène à une question assez simple pour le premier jalon. Qu’est-ce que je dois pouvoir vérifier dès que je commence à enregistrer de vraies situations de raccordement dans IRIS? J’ai maintenant un point de départ pour les premières issues et les premiers tests.
