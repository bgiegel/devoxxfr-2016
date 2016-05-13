# Boucle de feedback pour le développeur

J'aime bien ce genre de présentation car elles donnent plein de petites astuces qu'on peut appliquer directement en retournant au travail la semaine après le Devoxx.

Ici le thème est : Comment amélioré le feedback c'est a dire réduire le temps entre le moment ou on écrit le code et le moment ou l'on sait qu'il est erroné.

Les speakers nous montrent en livecoding (creation de services REST en Java) les différentes techniques pour avoir du feedback rapidement.

Voici quelques-unes des techniques qui ont retenues mon attention.

* Jetty démarre très vite

* Dans la configuration du plugin Jetty de Maven on a un paramètre : "scanIntervalSeconds" pour scanner le répertoire toutes les X secondes et refaire un deploy.

* Infinitest pour intellij : permet d'exécuter les tests unitaires automatiquement quand on change du code

* Workspace dans chrome : permet de répercuter les modifications que l'on fait dans chrome dev tools dans les fichiers du file système

* Grunt browserSync permet de rafraîchir le navigateur quand on modifie un fichier HTML ou JS. Permet également de tester sur plusieurs navigateurs en même temps.

* Reporter pour karma. Affiche une notification pour indiquer que les tests sont passés

* C'est important de réduire le temps de feedback pour rester concentrer. Perdre sa concentration fait perdre du temps.

* Pas de problème d'incompatibilite pour utiliser Jetty au lieu de Tomcat. En tout cas sur le code applicatif.