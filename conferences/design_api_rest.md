# Le design d'API REST, un débat sans fin ?

Une bonne présentation de Guillaume Laforge mais sur un sujet qui ne me passionne pas plus que ça.

* Préféré des noms plutôt que des verbes pour les ressources.

* Préféré la forme pluriel

* Un lien fun (un carte du metro avec les codes http comme station) : Bit.ly/stcode

* Utiliser des bon status code

* Il n'y a pas que 200. 201 notamment quand on crée des ressources. Avec l'adresse de location. 202 peut être utiliser pour les requêtes asynchrone.

* Utiliser des curseurs pour paginer plutôt que des pages pour être insertion friendly

* Pour le tri on utilise les paramètres de la requête

* Versionning. Plus souvent on a dans l'URL la version. Ou sinon dans le header.