---
title: "Le robot qui dessine"
categories:
  - Blog
tags:
  - Mindstorms
  - CoderDojo
excerpt: Un robot Mindstorms qui permet de dessiner
toc: true
toc_label: "sections"
toc_icon: "tasks"
toc_sticky: true
assetsFolder: /assets/images/posts/2017-12-27/
---

## Les principes de fonctionnement

Le robot qui dessine est construit sur une base de rover.

![Rover Monté]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinateurv2-all-small.png)


### Comment poser et lever le stylo ?

Un petit moteur annexe est placé dans le rover pour poser/lever le stylo.

Ce moteur va actionner un bras mobile à l'avant. Lorsque le bras est en position basse le robot peut écrire. Quand il est en position haute le stylo ne touche plus la feuille.

Dans la conception il est important que le stylo se trouve entre les roues avant. De cette manière lorsque le robot pivote, le stylo peut dessiner un angle.

![Porte-stylo Monté]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinateurv2-all-avec-porte-stylo-small.png)


Comme le moteur tourne sur un plan horizontal et que l'on veut convertir ce mouvement en déplacement vertical linéaire on va utiliser deux mécanismes.

Les deux engrenages font tourner un axe qui est perpendiculaire au moteur. L'engrenage jaune est entraîné par le moteur, il fait tourner l'engrenage noir qui fait tourner l'axe auquel le bras est relié.

![Linear actuator 1]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/linear-actuator-1.png)

Le bras à l'avant convertit la rotation de l'axe en mouvement de haut en bas. Lorsque l'axe tourne les barres du bas tournent avec l'axe. Le reste des barres suit le mouvement car les connecteurs gris sont sans friction.

![Linear actuator 2]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/linear-actuator-2-small.png)

### Les points d'attention

Après plusieurs essais ratés nous avons constaté que le robot ne doit pas avoir pas être trop lourd (il emporte la feuille de papier) et ne doit pas avoir trop de poids à l'arrière (il pivote sur la roue folle à l'arrière au lieu de pivoter sur les roues avant)


### Le plan de montage

Le rover va être construit en quatre parties :
- [le moteur du porte-stylo]({{site.baseurl}}blog/le-robot-qui-dessine-v2/#le-moteur-du-porte-stylo),
- [le porte-stylo]({{site.baseurl}}blog/le-robot-qui-dessine-v2/#le-porte-stylo),
- [le chassis]({{site.baseurl}}blog/le-robot-qui-dessine-v2/#le-chassis),
- TODO
- [la brique de contrôle]({{site.baseurl}}blog/le-robot-qui-dessine-v2/#la-brique-de-controle).

![Rover Eclaté]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinateurv2-avec-porte-stylo-exploded.png)

La liste complète des pièces nécessaires peut être téléchargée [ici]({{site.baseurl}}{{page.assetsFolder}}/BOM-dessinateurv2-avec-porte-stylo.xlsx). Toutes les pièces proviennent du kit EV3 Home sauf la roue folle. Cet élément peut être remplacé par un montage utilisant une petite roue ou acheté en complément pour une dizaine d'euros.

## Le moteur du porte-stylo

L'objectif dans cette étape est de monter le moteur qui actionne le porte-stylo.

![Montage terminé]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/1-completed-small.png)

Il faut assembler un petit moteur, plusieurs engrenages pour changer l'axe de rotation et des pièces pour assembler le tout.

![Vision explosée]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/1-exploded-small.png)

Les pièces nécessaires

![BOM]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/BOM-moteur.png)

Monter le cadre et les deux engrenages.

![1]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/1-1-steps-small.png)

Ajouter les supports sur le cadre.

![3]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/1-3-steps-small.png)

Ajouter la barre verticale des bras du porte-stylo. La partie basse tourne avec l'axe. En haut, la pièce de connexion grise est sans friction. La même en noir ne permetra pas au bras de bouger.

![5]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/1-5-steps-small.png)

Placer les supports sur le moteur

![2]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/1-2-steps-small.png)

![7]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/1-7-steps.png)

Connecter le petit moteur aux engrenages

![9]({{site.baseurl}}{{page.assetsFolder}}/1-petit-moteur/1-9-steps-small.png)

## Le porte-stylo

L'objectif dans cette étape est d'assembler le porte stylo et le fixer au moteur de l'étape précédente.

![Montage terminé]({{site.baseurl}}{{page.assetsFolder}}/4-porte-stylo/4-completed-small.png)

Les pièces nécessaires

![BOM]({{site.baseurl}}{{page.assetsFolder}}/4-porte-stylo/BOM-stylo.png)

Il faut assembler les deux bras qui seront raccordés au moteur et le support du stylo.

Montez les deux bras. Il faut absolument utiliser les connecteurs gris sans friction pour que les bras puissent poser/lever le stylo.

![1]({{site.baseurl}}{{page.assetsFolder}}/4-porte-stylo/4-1-steps-small.png)

Assemblez le support du stylo

![2]({{site.baseurl}}{{page.assetsFolder}}/4-porte-stylo/4-2-steps-small.png)

Assemblez les trois éléments

![all]({{site.baseurl}}{{page.assetsFolder}}/4-porte-stylo/4-all-steps.png)

Fixez le porte-stylo sur la barre verticale déjà en place côté moteur

![With motor]({{site.baseurl}}{{page.assetsFolder}}/4-porte-stylo/4-with-motor.png)

## Le chassis

L'objectif dans cette étape est d'assembler le chassis.

![Montage terminé]({{site.baseurl}}{{page.assetsFolder}}/2-roues/2-completed-small.png)

Les pièces nécessaires

![BOM]({{site.baseurl}}{{page.assetsFolder}}/2-roues/BOM-chassis.png)

Il faut assembler les gros moteurs, les roues, des barres derrières et dessous pour assurer la rigidité et la roue folle.

Montez les roues sur les moteurs pour les deux côtés.

![1]({{site.baseurl}}{{page.assetsFolder}}/2-roues/2-1-steps.png)

Assemblez la barre de dessous

![3]({{site.baseurl}}{{page.assetsFolder}}/2-roues/2-3-steps-small.png)

Assemblez la barre arrière

![4]({{site.baseurl}}{{page.assetsFolder}}/2-roues/2-4-steps-small.png)

Assemblez la roue folle

![5]({{site.baseurl}}{{page.assetsFolder}}/2-roues/2-5-steps.png)

Vous pouvez maintenant assembler le tout

![Vision explosée]({{site.baseurl}}{{page.assetsFolder}}/2-roues/2-all-steps.png)

## La brique de contrôle

L'objectif dans cette étape est d'assembler la dernière partie, la brique de contrôle.

![Montage terminé]({{site.baseurl}}{{page.assetsFolder}}/3-brique/3-completed-small.png)

Les pièces nécessaires

![BOM]({{site.baseurl}}{{page.assetsFolder}}/3-brique/BOM-brique.png)

Il faut assembler la brique de contrôle et les éléments qui permettront de la fixer au chassis.

Montez les supports arrière

![1]({{site.baseurl}}{{page.assetsFolder}}/3-brique/3-1-steps-small.png)

Assemblez les supports avant

![3]({{site.baseurl}}{{page.assetsFolder}}/3-brique/3-3-steps-small.png)

![4]({{site.baseurl}}{{page.assetsFolder}}/3-brique/3-4-steps-small.png)

Vous pouvez maintenant assembler  les éléments du support de la brique

![Vision explosée]({{site.baseurl}}{{page.assetsFolder}}/3-brique/3-all-steps.png)

