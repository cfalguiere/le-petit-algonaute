---
title: "Le robot qui dessine"
categories:
  - Montage
tags:
  - Mindstorms
  - CoderDojo
excerpt: Montage d'un robot Mindstorms qui permet de dessiner
toc: true
toc_label: "sections"
toc_icon: "list"
toc_sticky: true
assetsFolder: /assets/images/posts/2017-12-27/
---

Dans la session du 18 Mars, Hema avait voulu faire un robot qui dessine. On avait bricolé un truc mais ce montage avait beaucoup de contraintes. En partilier, le lever de stylo par le côté traçait des bouts de ligne à chaque fois.

Ce montage permet de poser et lever de stylo à la verticule. Le stylo a été aussi positionné entre les deux roues pour que le stylo puisse faire un coin à angle droit (plus ou moins).

## Description du montage

Ce robot peut porter un stylo et il est possible de faire des dessins en déplaçant le robot.

<span class="fas fa-fw fa-robot" aria-hidden="true"></span>&nbsp; Robotique
<br>
<span class="fas fa-fw fa-shapes" aria-hidden="true"></span>&nbsp; Facile
<br>
<span class="fas fa-fw fa-clock" aria-hidden="true"></span>&nbsp; 1h


Le robot qui dessine est construit sur une base de rover.

![Rover Monté]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinateurv2-all-small.png)


### Comment poser et lever le stylo ?

Un petit moteur annexe est placé dans le rover pour poser/lever le stylo.

Ce moteur va actionner un bras mobile à l'avant. Lorsque le bras est en position basse le robot peut écrire. Quand il est en position haute le stylo ne touche plus la feuille.

Dans la conception il est important que le stylo se trouve entre les roues avant. De cette manière lorsque le robot pivote, le stylo peut dessiner un angle.

![Porte-stylo Monté]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinateurv2-all-avec-porte-stylo-small.png)


Comme le moteur tourne sur un plan horizontal et que l'on veut convertir ce mouvement en déplacement vertical linéaire on va utiliser deux mécanismes.

1) Les deux engrenages font tourner un axe qui est perpendiculaire au moteur. L'engrenage jaune est entraîné par le moteur. Il fait tourner l'engrenage noir qui fait tourner l'axe auquel le bras porte-stylo est relié.

![Linear actuator 1]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/linear-actuator-1.png)

2) Le bras porte-stylo à l'avant se déplace de haut en bas. Il convertit la rotation de l'axe entraîné par le moteur en mouvement de haut en bas. Lorsque l'axe tourne les barres du bas tournent avec l'axe. Le reste, les barres du haut et les montants verticaux suit le mouvement grace aux connecteurs sans friction (les connecteurs gris).

![Linear actuator 2]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/linear-actuator-2-small.png)



### Les points d'attention

Après plusieurs essais ratés nous avons constaté que le robot ne doit pas avoir pas être trop lourd (il emporte la feuille de papier) et ne doit pas avoir trop de poids à l'arrière (il pivote sur la roue folle à l'arrière au lieu de pivoter sur les roues avant)


### Le plan de montage

Le rover va être construit en quatre parties :
- [le moteur du porte-stylo]({{site.baseurl}}blog/le-robot-qui-dessine-v2/#le-moteur-du-porte-stylo) (au centre en bas),
- [le porte-stylo]({{site.baseurl}}blog/le-robot-qui-dessine-v2/#le-porte-stylo) (au centre en haut),
- [le chassis]({{site.baseurl}}blog/le-robot-qui-dessine-v2/#le-chassis) (à gauche),
- [la brique de contrôle]({{site.baseurl}}blog/le-robot-qui-dessine-v2/#la-brique-de-contr%C3%B4le) (à droite).

![Rover Eclaté]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinateurv2-avec-porte-stylo-exploded.png)

La liste complète des pièces nécessaires peut être téléchargée [ici]({{site.baseurl}}{{page.assetsFolder}}/BOM-dessinateurv2-avec-porte-stylo.xlsx).

Toutes les pièces proviennent du kit EV3 Home sauf la roue folle. Cet élément peut être remplacé par un montage utilisant une petite roue ou acheté en complément pour une dizaine d'euros.

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

L'objectif dans cette étape est d'assembler tous les éléments que l'on vient de construire et de commencer à tester le robot

## Finir le montage

Le robot tout assemblé va ressembler à ça.

![Montage terminé]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinateurv2-all-avec-porte-stylo-small.png)

Pour le moment, il est en 3 parties

![Vision explosée]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinateurv2-avec-porte-stylo-exploded.png)

Le schéma suivant montre à quel endroit le dessous du chassis se fixe sur le petit moteur.

![chassis-moteur]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/chassis-moteur-small.png)

Le schéma suivant montre à quel endroit la brique s'attache sur le chassis.

![chassis-brique]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/chassis-brique-small.png)

Il ne reste plus qu'à fixer les cables.
- les deux gros moteurs sont connectés sur B et C
- le petit moteur est connecté sur D

![cablage]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/cablage-small.png)

## Le projet exemple

Le projet exemple peut être téléchargé [là]({{site.baseurl}}{{page.assetsFolder}}/0-ensemble/dessinator-v2.ev3)

### Poser et lever le stylo

On peut tout d'abord tester le fonctionnement du stylo avec le programme suivant. Ce programme lève le stylo puis le repose.

Avant de lancer, il faut positionner la pointe du stylo au niveau de la feuille

![stylo]({{site.baseurl}}{{page.assetsFolder}}/5-programme/stylo.png)

> Lorsque le moteur tourne en marche arrière (-30) il soulève le stylo.
> Lorsque le moteur tourne en marche avant (30) il abaisse le stylo.

> L'angle de rotation du moteur doit rester petit (45 par exemple) car il suffit de déplacer le stylo sur moins de 1cm.



### Tracer un cercle

La figure la plus simple à tracer est le cercle.

Avant de lancer, il faut positionner la pointe du stylo au niveau de la feuille

![cercle]({{site.baseurl}}{{page.assetsFolder}}/5-programme/cercle-small.png)

> Si on ne fait tourner qu'une roue, le robot va tourner autour de l'autre roue. Ici, on fait avancer la roue commandée par le moteur B, la roue gauche. La roue droite reste immobile et le robot va pivoter sur cette roue. Si on fait ça suffisamment longtemps, le robot trace un cercle.

Quelques idées pour aller plus loin :
- comment peut on calculer le rayon de ce cerclsmae ?
- comment calculer le nombre de tours de roues nécessaires pour faire le cercle complet
- comment peut on faire un cercle plus large ?

Indices:
- le diamètre des roues est 4,32 cm
- vous pouvez utiliser les deux roues

### Tracer un carré

Tracer un carré nécessaire de faire 4 lignes droites et pivoter pour tourner à chaque coin. On va lever le stylo dans chaque coin pour éviter les gribouillages.
Attention, ce programme démarre (et fini) stylo levé. Si nécessaire, utilisez une partie du programme "stylo" pour  placer le stylo à la bonne hauteur.

![carré]({{site.baseurl}}{{page.assetsFolder}}/5-programme/carre.png)

> Pour faire pivoter le robot sur place, on va faire tourner une roue en marche avant pendant que l'autre tourne en marche arrière. De cette manière, le robot va pivoter autour d'un point qui est entre les deux roues au niveau du stylo.

> L'action "poser le stylo, faire une ligne droite, lever le stylo et pivoter" est répétée 4 fois (une fois par arrête du carré). On utilise un bloc boucle pour indiquer cette répétition. Le nombre de répétitions est indiqué à droite de la boucle, ici c'est 4.

> Sur le bloc qui permet de pivoter, le nombre de degrés est calculé pour que le robot pivote à environ 90°. Attention, le nombre de degré ici est le nombre de degré en tours de roue. Cela n'a pas forcément de rapport avec l'angle de rotation du robot.

Vous aurez peut être à changer le nombre de degrés de rotation du bloc qui pivote. Selon le type de sol le frottement est plus ou moins important et le robot tournera plus ou moins facilement. Il l'angle du virage du robot peut être différent de 90°. Il est possible de vérifier l'angle du rotation avec un capteur, mais pour l'instant on va rester sur un programme simple.


Quelques idées pour aller plus loin :
- comment peut on faire un carré plus grand ?
- comment peut on faire un triangle ?

Indices:
- il faudra changer la durée ou le nombre de rotations des blocs


## Quelques conseils pour finir

L'angle de rotation du moteur doit rester petit (45 par exemple) car il suffit de déplacer le stylo sur moins de 1cm :
- Lorsque le moteur tourne en marche arrière (-30) il soulève le stylo.
- Lorsque le moteur tourne en marche avant (30) il abaisse le stylo.

Restez à des vitesses moyennes entre 30 et 60 (ou -30 et -60 en marche arrière). Si la vitesse est trop basse, le frottement est très important et le robot avance mal. Si la vitesse est trop grande, les manoeuvres deviennent très imprécises.




