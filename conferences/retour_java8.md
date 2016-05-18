# Retours sur Java 8

Une conférence que tout bon développeur Java se devait d'aller voir. Même si Java 8 est sorti il y a quelques temps maintenant c'est toujours intéressant d'avoir le retour d'un développeur expérimenté tel que JM Doudoux.


* Rappel: les best practice sont empiriques et subjectives. Ce ne sont pas des règles et elles évoluent tout le temps.
* Optional: 
    * pas recommander pour les paramètres et dans les getter. Pas pour variable d'instance car pas serialisable.
    * Optional pour les types primitif : OptionalInt
    * Pas d'optional pour les tableau ou les collections
    * Limite au retour des fonctions d'api
* Arrays setall permet d'initialiser un tableau de manière parallèle. Mais attention aux points de contentions quand on utilise des classes Thread Safe.
* Utiliser des lambda plutôt que des classe interne.
* Utiliser le plus possible les interfaces fonctionnel de java.
* Garder des expressions le plus simple possible.
* Stream attention on a l'habitude de l'impératif plutôt que fonctionnel.
* Ne pas en abuser parfois une boucle est plus lisible.
* Debugguer stream est difficile. Pensez à utliser la méthode peek.
* Attention aux perfs avec LongStream qui fait de l'unboxing.
* Éviter les stream infini. Surtout en parallèle..
* Quelques Exemples de junit 5 qui utilise les lambda.
* Assertall et lambdas : Permet de faire des assertions groupées permettant d'avoir le nombre d'assert qui est passe dans un test.
* Expert throws pour tester les messages d'erreurs des exceptions.
* Jmh pour faire des tests de performances.
