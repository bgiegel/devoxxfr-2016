# OutOfMemoryException : Quel est le coût des objets en Java ?

Une présentation intéressante ou j'ai appris pas mal de chose sur un sujet dont on ne parle pas assez souvent je trouve. La consommation mémoire des objets. Ou plutôt des structures des objets. Cette présentation donne envie de tout mesurer en revenant au boulot !

* Un objet sans rien prend déjà de la mémoire pour stocker le pointeur vers la classe par exemple. De base c'est 16 bytes en 64 bits.

* Mark word : données variables sur l'objet.

* Compresser oops: permet d'utiliser les 3 derniers bites non utilisé des adresses de pointeur pour faire gagner 30% d'espace disque.

* Padding : outil en ligne de commande : JOL
Pour stocker il faut des multiples de 8 quand ce n'est pas le cas on fait du padding (on rajout de bits ).

* La taille des String à changé au cours de versions pour passer de 32 à 24 byte. Et sur java 9 il y a des string compact de seulement 8 octets. Mais uniquement en utf8

* Linkedlist: A ne plus utilisé. Voir le talk sur le sujet de Jose Paumard.

* Hashmap 4ko pour 100 éléments !!!

* Jmap -hist : donne la quantité d'instance et la taille en mémoire des objets

* Une option de la jvm permet d'afficher l'histoire avant et après le GC.

* Pour exploiter un heap dump : visualVM ou yourKit

* Solutions : 
    * flyweight 
    * internalizers
    * Arraylist plutôt que Linkedlist
    * Utiliser des OpenAdressingHashMap

**Mesure, don't guess**. 
Pas la peine de supprimer toutes les hashMap sans mesurer ce qui se passe dans l'application.

