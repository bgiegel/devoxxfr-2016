# Jigsaw

Un présentation très attendue. Par une de plus grosse tronche du Devoxx selon moi : Remy Forax. Comme d'habitude il a du mal à tenir le timing de ses talk (trop bavard !). Je n'ai pas pris beaucoup de notes parce que j'essaye de suivre. C'est très technique. Cependant je recommandes pour tous ceux qui sont curieux d'en apprendre d'avantage sur le fonctionnement interne de Java.

* Problème : compil time info diff runtime info. On scan les dépendances de manière lineaires. Du coups si il y a 2 versions d'une même lib on va scanner jusqu'à trouver celle qui contient la classe dont on a besoin. Du coups on peut se trouver dans des cas ou une classe hérite d'une classe mère d'une autre version de la même lib !
* Certaines des libs sont trop grosse. 66Mo pour RT.jar. IOT ?
* Pas d'encapsulation forte. La jdk n'a qu'une ligne de défense...
* Si on utilise des jars non modularisés on créer un module automatiquement et on le met dans le modulepath
* Problème : Comment faire un système de gestion de dépendance avec tous les outils existant.


