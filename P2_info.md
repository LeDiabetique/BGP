## BADASS Project


#### VXLAN
Virtual eXtensible Local Area Network
Ajoute une encapsulation d'un paquet via VTEP (VXLAN Tunnel Endpoints) qui a la reception du paquet IP, enleve l'encapsulation et donc simule comme si lón est encore dans le meme VLAN.
Permet de lier un reseau bien qu'il soit distant physiquement.

#### VXLAN vs VLAN
VLan ne s'etend que sur un reseau Local et est en 12 bits donc 4096 adresse possibles uniquement (24 bits pour VXLAN)


#### Leaf-Spine
Un Leaf dans le cadre d'un VXLAN est un VTEP relie a un Spine (= Switch).
Chaque Leaf est relié à TOUS les Spines, mais les Leafs ne sont pas connectés entre eux directement, ni les Spines entre eux.
Donc la longueur reseau est similaire pour tous, et ainsi le reseau est previsible, fonctionnel si un Spine tombe.

#### Static / Singlecast
Envoi d'un message a un user specifique.


#### Multicast
Envoi d'un message a un groupe, tout les utilisateurs de ce groupe le recoivent.

