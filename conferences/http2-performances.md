# Pourquoi il ne suffira pas de faire du http 2.0 pour faire des applications performantes

Une université de très bonne qualitée. Des interactions avec le publique au début permettent d'expliquer de manière évidentes les problèmes qu'on rencontre avec les anciennes version d'HTTP.

Voilà quelques points qui ont retenus mon attention :

### Introduction
* Ne pas utiliser de moyenne de temps d'appel mais utiliser des percentiles
* TTFB : Time To First Byte. Permet de mesurer uniquement le temps de traitement de la page sans l'affichage
* Page load: temps total (traitement + affichage)
* TCP est fiable mais lent. Échange d'infos techniques, buffer, etc.
* Faire attention aux intermédiaires. Rend TCP non fiable dans certain cas

### Analyse de l'échange entre client et serveur
* Outils directement utilisable en JS dans l'objet window
* Google blink (moteur de rendu html de google) : la plupart du temps passé par le navigateur est pour le traitement du reseau.
* La bande passante ne sert à rien pour le web il faut en avoir assez mais en avoir beaucoup est inutile.
* MTU (maximum transmission Unit) : taille max du packet
* Jitter : la variation de vitesse (ordonnancement des paquets, retransmission, etc.)
* La bande passante à tendance à augmenter beaucoup plus vite que la latence
* La latence est limite par la réalité : la physique, l'émission des signaux.
* 5ms prend la lumière  pour 1000km
* Wifi est half duplex !
* Slow start : règle qui empêche d'envoyer trop d'octet au début d'une connexion
* Http2 : obliger de passer par tls(méthode h2) car aucun navigateur ne supporte la méthode h2c
* Push http2 : permet d'envoyer les JS et css lors d'une requête à une page web. Cela évite de faire des requêtes inutilement.
* Avec http2 on ne veut plus optimiser en faisant du sharding ( tout doit aller dans la même requête)
* Pas d'inline non plus (il le fait tout seul)
* Un octet non transmis est un bon octet
* Http2 améliore surtout les réseau mobile ou la latence  est un frein (3G typiquement)
* Iperf permet de simuler un serveur et un client en local
* Le localhost n'est PAS du tout représentatif du réseau. Si vous faites des benchmark ne le faite pas sur du localhost. Ou alors utilisez des outils pour simuler de la latence.
    * Outils de simuler ; chrome dev tools, TC linux, netsh windows, Charles proxy, ntl (mac)

### Analyse de l'échange entre le serveur et le backend
* Une requête client provoque beaucoups d'appels internes à différents services
* Kernel bypass permet de diminuer la latence en utilisant des cartes réseaux spécifique pour ne pas passer par la partie io du kernel qui prend 40℅ de la latence.
* Soap : le poids du protocole est énorme par rapport au contenu
* Udp Multicast: permet de faire du messaging plus équitable en terme de temps de réception de chaque subscriber (on remplace le broker par un switch qui duplique les messages)
* Possible de faire du http2 applicatif sur udp
* Ping permet de mesurer la jig (différence de latence entre chaque appel)
