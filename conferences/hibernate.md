# Hibernate tu connais... mais en fait tu connais pas

Une présentation sans prétention comme le signal Emmanuel Bernard au début de son talk. Cependant ca reste intéressant pour connaitre un peu toutes les nouveautés d'hibernate.

* Nouvelle dépendance : hibernate-java8. Permet de mapper les champs date de la BDD avec les nouvelles classes de l'API Date de Java8.

* Amélioration de performance pour flusher plus vite les données. On regarde le bytecode pour savoir quelle classe à été modifiée avant de checker les propriétés des objets pour voir si il y a une difference. Du coups plus besoin de tout analyser.

* Apparition des lazyGroup pour charger les données par use case.

* Dans le cache de 2nd niveau les objets sont stockés directement en mémoire. Donc gain de perf. Avant c'était un tableau clé valeur et les objets était recréer à chaque fois.

* Hibernate seach. Requête full text au niveau objet. Appelle lucene.

* Entitity @Indexed : annotations pour spécifier les champs à indexer ou pas.

* Hibernate OGM : Jpa pour le NoSQL

* Hibernate Validator: impl de bean validation. Permet de rajouter des annotations de validation dans le type générique des collections.

* Hibernate spatial permet d'utiliser les fonctionnalité de géolocalisation des base de données.

