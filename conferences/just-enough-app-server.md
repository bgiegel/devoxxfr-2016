# Just enough app server

On est rarement déçu par les présentation d'Antonio Goncalves pour peu qu'on soit intéressé par le monde JEE. Dans cette conférence Antonio nous montre que les serveurs d'app ont bien évolués et qu'ils permettent de faire du microservices.

* Les server d'app sont par design séparer en petite spec. Pas de monolithes.
* Idée reçue : les server d'app sont lent. Tomcat démarre en 0,6s
* Les serveurs d'app sont plus rapide et font plus de chose : 34 spec javaee 7
* Consomme bcp mémoire ? Faux ! Tomcat 60mo. Wildfly 100mo
* Skinny war ou fat war en fonction de spring ou app server
* On peut packager en jar uniquement les libs dont on a besoin.
    * Dans javaEE : Wildfly swarm
    * Environnement Spring : Spring boot
    * Autre : dropwizard

Antonio détail l'outil Swarm :

* Swarm permet de package une application dans un jar avec le server et uniquement les libs dispo
* Permet aussi de faire déployer l'application plus vite que si le serveur était vide. Car moins de lib
* La configuration se fait dans le 'main'
* Possible de rajouter un module management

Antonio termine par une démo qui vise à déployer des EJB sur un Raspberry Pi. Et ca marche !
