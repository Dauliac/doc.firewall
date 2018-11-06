# doc.firewall 🏢

## Generations 🔖
### First: packet filters
###

## Types: 📄

### ACL:
*Access Control List*
Il s'agit d'une liste d'addresse et de ports authorizés ou bloquées par le firewall.

Les ACL sont dispnible sur la chouche *physique* ou au seins d'application centralisant leurs configurations.
Les ACLs conviennent pour des portocoles dont les ports sont statiques mais ne fonctionnent pas sur des protocoles dynamiques comme le torrent par exemple

Il y a 3 type d'**ACL**:
- Standard:
    filtrant au regard de l'ip source et d'une partie de l'ip destination grace à des *masques génériques*
- Étendue:
    Utilisant l'ip destination, une partie de l'adresse de destination (masques génériques),
    le type de protocole, le port (source/destination),
    les flux (tcp/ip), le type de service et par priorités d'addresses IPs
- Nommée-Étendue:
    C'est une ACL étendue à laquelle on ajoute un label

#### Products:
  - [cisco](https://www.cisco.com/c/en/us/support/docs/security/ios-firewall/23602-confaccesslists.html)
  - [Netfilter](https://www.netfilter.org/) **=>**  [tutoriel](https://blog.garamotte.net/posts/2017/01/28/fr-firewall-configuration-with-iptables.html)

### Policy:
### Filters:
### Rules:
### WAF:
### SD-WAN:
*Software Defined Wide Area Network.*

L'Open Networking User Group (ONUG) est un groupe de travail rassemblant les différents acteurs de la communauté SD-WAN

Il définis les cas d'usages ainsi que les critéres d'une solution SD-WAN.

Migration d'une connexion
MPLS-VPN >>> Internet Connection

https://fr.wikipedia.org/wiki/SD-WAN
https://cisco.app.box.com/v/SD-WAN-pour-les-nuls
https://www.onug.net/community/working-groups/software-defined-wide-area-network-sd-wan/
https://www.informatiquenews.fr/reseau-mpls-vpn-temps-de-passer-sd-wan-thomas-desrues-juniper-networks-49636

