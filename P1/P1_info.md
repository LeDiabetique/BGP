## BADASS Project

#### GNS3
Graphical Network Simulator-3.

Simulateur de réseau permettant de créer et tester des architectures réseau sans matériel physique.

#### Busybox
Environnement systeme minimaliste
Contient plusieurs commandes de  base (ls, cp, mv, cat, ...)
Compatible Linux

#### FRRouting
Service de routage IP
Implemente les differents protocoles et software pour communiquer. (Zebra, ISIS, BGP, OSPF)


#### ZEBRA
Zebra est le composant central de FRRouting
Il sert d'interface de routage entre les differents protocoles et le noyau.

#### BGP
Border Gateway Protocol
Reseau externe - FAI (Fournisseur d'acces internet) vers FAI.


#### OSPF
Open Shortest Path First
Reseau interne(Moyen/Grand) - Entreprise / Reseau Local : Ordinateur vers Ordinateur (en passant par le routeur)


#### IS-IS
Intermediate System to Intermediate System
Reseau interne (Grand) - Le routeur connait toute la topologie du niveau 1 et 2

#### IS-IS vs OSPF
OSPF ne connait que sa propre zone alors que IS-IS connait une plus grande topologie et donc limite les transactions pour atteindre un chemin.


#### Exemple Complet

- On envoie un message a destination d'un utilisateur dans un autre reseau externe.
- Mon routeur utilise OSPF pour transporter mon message jusqu'a sortir du reseau.
- Le routeur en bordure utilise BGP pour communiquer avec le routeur de mon destinataire distant.
- Le routeur destinataire recoit le message et transmet via OSPF jusqu'au destinataire en interne.


#### Useful commands
sudo usermod -aG docker hdiot *Add mon user au groupe sudo*
 - Donner les droits user pour la commande dumpcap.
    - sudo chgrp hdiot /usr/bin/dumpcap
    - sudo chmod 754 /usr/bin/dumcap
    - sudo setcap 'CAP_NET_RAW+eip CAP_NET_ADMIN+eip' /usr/bin/dumcap

#### DL
    - GNS3
    - Docker


Bien creer le fichier vtysh.conf dans /etc/frr/
Modifier les settings du daemon "vi /etc/frr/daemons" et mettre bgpd ospfd isisd a yes