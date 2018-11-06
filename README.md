# doc.firewall 🏢

![firewall](https://azurecomcdn.azureedge.net/mediahandler/acomblog/media/Default/blog/fb10e181-7a4d-4ceb-98ab-45ac18906291.png)


## Generations 🔖

> Historiquement on distingue 3 génération de firewall:

### First: packet filters
Cette méthode inspecte les paquets et les compares à des règles de filtrages.

### Second generation: stateful filters
Concu pour fonctionner avec la 1ère génerations mais intervient au niveau de la couche 4 (transport)

### Third generation: application layer
Introduit [Link to Header](### Applicatif (WAF):)

## Types: 📄
### Bridge/Matériels:
Ce sont les firewalls présents les matériels physiques (externe, sur des rooters, ..)

#### Doc:
  - [emisisoft](https://blog.emsisoft.com/fr/4147/tec090701fr/)
  -
### ACL:
*Access Control List*
Il s'agit d'une liste d'addresse et de ports authorizés ou bloquées par le firewall.

Les ACL sont dispnible sur la chouche *physique* ou au seins d'application centralisant leurs configurations.
Les ACLs conviennent pour des portocoles dont les ports sont statiques mais ne fonctionnent pas sur des protocoles dynamiques comme le torrent par exemple

Il y a 3 type d'**ACL**:
- Standard:
    filtrant au regard de l'ip source et d'une partie de l'ip destination grace à des *masques génériques*.
- Étendue:
    Utilisant l'ip destination, une partie de l'adresse de destination (masques génériques),
    le type de protocole, le port (source/destination),
    les flux (tcp/ip), le type de service et par priorités d'addresses IPs.
- Nommée-Étendue:
    C'est une ACL étendue à laquelle on ajoute un label.

#### Doc:
  - [wikipédia](https://fr.wikipedia.org/wiki/Access_Control_List)
  - [windows](https://docs.microsoft.com/fr-fr/windows-server/networking/sdn/manage/configure-datacenter-firewall-acls)
  - [linux](http://lea-linux.org/documentations/Gestion_des_ACL)

#### Products:
  - [cisco](https://www.cisco.com/c/en/us/support/docs/security/ios-firewall/23602-confaccesslists.html)
  - [Netfilter](https://www.netfilter.org/) **=>**  [tutoriel](https://blog.garamotte.net/posts/2017/01/28/fr-firewall-configuration-with-iptables.html)
  - [Isafer](https://fr.wikipedia.org/wiki/ISafer)

### Policy:
### Applicatif (WAF):
Les pare-feux applicatifs vérifient la conformité des paques au regard d'un protocole.
ex: que du http sur le port 80

Ils permettent de véfifier que le contenu sur des ports dynamiques ou `à contenu sale`
ex: FTP/DNS/HTTP échange d'information bas niveau (ip ports) au niveau applicatif.

#### Doc:
  - [wikipédia](https://fr.wikipedia.org/wiki/Web_application_firewall)
  - [cert-ist](https://www.cert-ist.com/pub/files/Document_Cert-IST_000333.pdf)


#### Products:
  - [qosmos](http://qosmos.com/)
  - [aws](https://aws.amazon.com/fr/waf/)
  - [celonet](https://www.celeonet.fr/firewall-applicatif/)
  - [naxsi](https://github.com/nbs-system/naxsi)

### SD-WAN:
*Software Defined Wide Area Network.*

L'Open Networking User Group (ONUG) est un groupe de travail rassemblant les différents acteurs de la communauté SD-WAN

Il définis les cas d'usages ainsi que les critéres d'une solution SD-WAN.

Migration d'une connexion
MPLS-VPN >>> Internet Connection

#### Doc
  - [wikipédia](https://fr.wikipedia.org/wiki/SD-WAN)
  - [cisco](https://cisco.app.box.com/v/SD-WAN-pour-les-nuls)
  - [onug](https://www.onug.net/community/working-groups/software-defined-wide-area-network-sd-wan/)
  - [informatiquenews](https://www.informatiquenews.fr/reseau-mpls-vpn-temps-de-passer-sd-wan-thomas-desrues-juniper-networks-49636)

