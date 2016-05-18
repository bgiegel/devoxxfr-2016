# Get Hip with JHipster: Spring Boot + AngularJS + Bootstrap

Matt Raible est vraiment un des meilleurs Speaker que j'ai pu voir à Devoxx. Pour faire le Hipster il s'est habillé en costume, il portais une cravatte à l'ancienne mode et tenais un verre de whisky à la main. Nicolas Martignol (un des organisateur du Devoxx) avait même préparé un verre de champagne pour l'occasion !

* Commence par parler des tendances en Java comme les microservices et les déploiement sans conteneurs, ou encore le monitoring.
* Rappels sur Spring Boot : 
    * permet de creer des applications stand-alone en Java en embarquant un tomcat, jetty ou autre. 
    * Permet aussi de faciliter la configuration en fournissant des modèles de pom et de configuration spring en fonction du type de projet.
    * Spring initializer permet de générer un squelette d'application en fournissant les principales dependances du projet.
* Jhipster utilise Angular pour le front. La raison est que c'est de loin le framwork MVC Javascript le plus en vogue ces dernières années. Schémas Google Trends à l'appuie.
* Jhip utilise Yeoman pour générer une app springboot et angular. En incluant également bootstrap, html5 bien sûr et CSS3.
* On peut ensuite ajouter à sa guise des base SQL ou NoSQL, Maven ou Gradle, différents outils de caching, etc..
* Il recommande vivement Browsersync pour améliorer la vitesse de développement. Browsersync permet de rafraichir automatiquement l'application quand on sauvegarde le fichier. Il permet également de tester sur plusieurs navigateurs simultanément.
* Impressionnant : L'objectif de la démo est de créer de zéro une application de blog minimaliste et de la déployer sur Heroku... En 20 minutes !
* Jhipster commence par une série de questions à la création de l'application pour savoir ce qu'il va y avoir dedans.
* Petit conseil hors sujet : Supprimer la barre de progression dans npm améliore grandement la rapidité de l'outil.
* Créé plein de truc par défaut vue, contrôler rest, script de création de base et même jeu de test
* Jdl studio (outil développé par l'équipe de JHipster) permet de décrire simplement dans un fichier '.jh' les entities du projet. Ce fichier est ensuite utilisé pour générer les classes Java.
* Embarque de base plein d'outils comme metrics, load testing avec gatling, protractor.
* On peut apprendre en utilisant jhipster juste en regardant le code généré.
* Un livre : Jhipster minibook
