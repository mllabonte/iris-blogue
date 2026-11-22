---
title: "La dualité de l’intervention physique et électronique"
description: "Une étiquette saisie à la main peut guider des interventions pendant des années. IRIS est né du besoin de retrouver et de vérifier ce qu’elle désigne."
date: 2026-11-22 11:00:00 -0500
---

Sur un port de commutateur, je lis `A102-005`. Est-ce le bon local? Est-ce le numéro que j’ai vu sur la plaque? Mes doigts étaient-ils bien placés sur le clavier? À l’ère de l’intelligence artificielle, on parle beaucoup de surveiller et de valider l’intervention d’un robot. Nos propres gestes méritent la même attention. Quelques caractères tapés en quelques secondes serviront de référence à mes collègues pendant des années.

À l’écran, la prise existe parce qu’elle est nommée. Mais si le nom est faux, et que le plan reprend la même erreur, les deux documents peuvent se donner raison sans que personne ait vérifié la prise. Comment savoir qui elle est? **Raconte-moi son origine.**

## Du local au commutateur

Dans un petit local, un enseignant prépare son prochain cours. Il dépose sa matière sans se demander quel chemin empruntent ses fichiers. Sous son bureau, un petit embout donne accès au système nerveux de l’établissement. Sur la plaque, la prise porte un nom tiré de son local et de la place qu’elle occupe parmi ses sœurs.

Derrière la plaque, un câble traverse des murs et des plafonds jusqu’à une salle de télécommunications. Le panneau de raccordement est le terminus de ce câble permanent. Pour que la prise rejoigne le réseau, je relie le port du panneau à un port du commutateur avec un cordon de brassage. Le port choisi fait partie du trajet qu’il faudra pouvoir retrouver.

## De retour au bureau

Une fois le raccordement fait, je reporte le nom de la prise dans la description du port du commutateur, en ligne de commande. Sur le plan de l’étage, je pose un point aux coordonnées `(x, y)` de la prise et j’y inscris le même nom. La description du port me donne une piste depuis le commutateur. Le plan ramène cette piste à un endroit précis dans le local. Entre les deux, le fichier des panneaux me permet de retrouver le raccordement.

La prochaine personne à consulter ces renseignements voudra peut-être orienter un bureau, raccorder un nouvel appareil ou localiser une panne. Un chiffre inversé, un point au mauvais endroit ou un cordon déplacé sans mise à jour suffit à la faire partir sur une fausse piste. L’erreur peut faire boule de neige quand elle est recopiée à son tour. À la fin, la prise est toujours dans le mur, mais personne ne sait avec certitude à quoi correspond son nom.

## Pourquoi IRIS

Je veux pouvoir partir du plan ou du commutateur et remonter jusqu’à la même prise, avec son port de panneau et son brassage lorsqu’il est connu. Si deux prises portent la même étiquette, je veux voir les deux et disposer d’assez de contexte pour les distinguer. Si une liaison reste à vérifier, je veux pouvoir l’indiquer et la corriger au moment de l’intervention. C’est la raison d’être d’IRIS : garder ensemble le nom, l’emplacement et le chemin de la prise, pour que la documentation reste utile à la prochaine personne qui en aura besoin.
