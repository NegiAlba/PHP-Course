# Introduction à PHP

## Caractéristiques Principales de PHP

- Langage interprété
- Langage côté serveur (back-end)
- Langage executé instructions par instructions
- Multi-plateformes

### Spécialités de PHP

- Génération de texte :

  - HTML
  - PDF

- Génération de documents :
  - PDF
  - Images

### Fichiers PHP

- Code inséré dans une page HTML (qui contient l'extension .php)
- Entre des balises <?php et ?>

## Fonctionnement de PHP

L'interpréteur lit le code source PHP et génère un flux de sortie en fonction de 4 règles :

- Toute ligne située hors d'un bloc PHP (<?php ?>) est retournée telle quelle.
- Le code PHP est interprêté et génère eventuellement des résultats qui seront aussi récursivement intégrés au flux de sortie.
- Les erreurs éventuelles donnent lieu à des messages d'erreurs que l'on va aussi retrouver dans le flux de sortie.
- Une page HTML qui ne contient pas de bloc PHP (mais qui comporte l'extension .php) sera donc simplement renvoyée.

## Historique de PHP

PHP a été créé par un étudiant en informatique qui souhaite analyser les connexions à son site web. Il s'agit de **Rasmus Lerdorf**, un Groënlandais en 1994. C'est lui qui va développer les versions 1 et 2 de PHP. A l'époque signifie Personal Home Page.

En 1997, le langage sera repris par deux étudiants **Andi Gutmans** et **Zeev Suraski** qui vont sortir la v3 mais aussi lancer les outils **Zend**.

Depuis PHP a subi de nombreux remaniements (quasi-intégraux), il a obtenu une version objet avec la v4 et s'inspire du modèle de Java de côté là. La version 5 est synonyme de grands changements et s'inspire grandement de Java. Elle jouit d'une grande popularité puisqu'elle a été maintenue pendant de longues années (à tel point que la version 5.7 est encore beaucoup utilisé).

**La dernière version majeure de PHP est PHP8.1**, sachant que la v7 est sortie en 2015, il y a eu un support important sur celle-ci. Il n'y a jamais eu de version 6, parce que le début de développement de la v6 coïncide avec une période de soucis unicode, le temps d'intégrer ces changements techniques (ceux de la v6), on a préféré mettre à jour la version 5 (donc concrètement les modifications de la v6 commencent à partir de la 5.4) et au final on est passé de la v5 à la v7.

### Regain de popularité

Depuis 2011, PHP a subi un gain de popularité entre Wordpress et Facebook. Facebook crée en 2011 la HHVM (HipHop Virtual Machine) qui sera un pré-compilateur de code PHP (Just In Time). En 2014, il sortiront le langage Hack largement inspiré de PHP.
**Zend** réagira en accélérant le développement de PHP avec la v7 et la v8, en améliorant de manière considérable les performances de PHP avec une compilation AOT (Ahead Of Time).

### Quand ?

PHP signifie désormais **PHP Hypertext Processor**, mais on ne sait pas depuis quand.

## Utilisation de PHP aujourd'hui

PHP aujourd'hui reste le langage le plus utilisé sur le Web. Utilisé par de grands sites.

### CMS

Les CMS les plus populaires utilisent PHP

- Wordpress
- Joomla
- Drupal
- Prestashop
- Magento (même si sa popularité a décru fortement)

### Frameworks

De grands frameworks sont sous PHP

- Symfony
- Laravel
- Zend Framework

### Facile à prendre en main

Pour débuter sous PHP, il suffit d'une stack LAMP disponible grâce à plusieurs outils

Une stack LAMP est composée de Linux, Apache, MySQL (ou MariaDB) et de PHP.

Les outils les plus populaires qui offrent une stack LAMP portable sont :

XAMPP, WAMP, MAMP, Laragon et Docker.
