## P3

#### EVPN
Ethernet VPN
Protocol permettant déchanger des informations en couche.
Evite la redondance des requetes de reconnaissance au sein d'un large reseau.
 - Type 2 : Route MAC/IP : Transporte les adresses MAC et IP des hotes connectes au reseau.
 - Type 3 : Route Multicast : Indique aux VTEP qui participe a la diffusion d'un VNI.

#### Loopback
Interface virtuelle pour definir une adresse ip
Permet d'avoir une adresse stable afin que les protocoles puissent communiquer avec.

#### RR
Reflect Routing
Centralise les routes sur un seul routeur et permet aux Leafs de connaitre les routes possibles sur le reseau.

#### VTEP
VXLAN Tunnel Endpoint
Element reseau qui encapsule et decapsule les paquets en provenance ou a destination d'autres VTEP (Routeur Leaf).

#### MPLS
Multiprotocol Label Switching
Technologie de transport de paquet qui labelisse les pauets plutot que d'utiliser directement les IP.
Evite des requete IP pour identifier la table de routage. 


#### Leaf-Spine
Un Leaf dans le cadre d'un VXLAN est un VTEP relie a un Spine (= Switch).
Chaque Leaf est relié à TOUS les Spines, mais les Leafs ne sont pas connectés entre eux directement, ni les Spines entre eux.
Donc la longueur reseau est similaire pour tous, et ainsi le reseau est previsible, fonctionnel si un Spine tombe.