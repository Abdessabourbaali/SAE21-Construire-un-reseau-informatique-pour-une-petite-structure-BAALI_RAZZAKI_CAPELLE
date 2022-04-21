# SAE-21, Construire un réseau informatique pour une petite structure

Durant la SAE-21, nous avons été chargé de mettre en place un réseau informatique pour une petite entreprise. 

Une tâche que nous seront certainement amené à réaliser dans un futur proche.

## Le cahier des charges est le suivant :

- Prévoire un plan d'addressage pour toute les machines de nôtre réseau

- La structure de l'entreprise comprend un service administratif, un service commercial et un service informatique

- Configurer un serveur web externe ( dans une DMZ ) contenant une page Web static, accessible au personne à l'interieur et à l'extérieur du réseau

- Un serveur DNS ( dans une DMZ ) qui assure la résolution des nom symbolique

- Un serveur Web interne ( Intra-net )

- Un serveur DHCP, qui fournira des IP à toutes les machines du réseau

- Mise en place d'un peu de sécurité

- Les différents accès : 
    - es administratifs devront pouvoir accéder à internet et aux serveurs internes et externe

    - Les commerciaux devront pouvoir accéder aux serveurs interne et externes

    - Le SI doit pouvoir avoir accès à toutes les machines en SSH

    - Aucun message provenant de l’internet ne doit pouvoir arriver vers le LAN. Par contre il peuvent atteindre le serveur web externe

## Matériel et logiciel choisies : 

- Nous avons choisie d'utiliser GNS3
- Pour le rendue, nous avons choise d'utiliser Github
- Pour ajouter de la sécurité, nous avons choisie de mettre en place des règles ACL


## Mise en place du réseau

La mise en place du réseau se découpe en deux grandes parties :

- Configuration de la partie virtuelle
- Configuration de la partie physique


## Travail préliminaire

Premièrement, nous avons commencé par mettre en place un environement de travail professionelle. Pour cela nous avons décidé d'utiliser Github afin d'organiser et de mettre en communs tous nos fichier.

Par la suite, on a réfléchis et mis en place plan d'addressage pour notre réseau. Ce plan est disponible dans les fichier joint sous le nom de "Plan_Addressage.drawio"

<img src="https://github.com/Abdessabourbaali/SAE21-Construire-un-reseau-informatique-pour-une-petite-structure-BAALI_RAZZAKI_CAPELLE/Plan_Addressage.png" style="width: 200px">

Une fois ces deux choses terminé, nous avons commener à réaliser la partie virtuelle puis dans les dernières séances nous nous sommes occupé de la partie physique.

## Mise en place et configuration de la partie virtuelle

Afin de créer et mettre en place la partie virtuelle, on a du configurer les routeurs, mettre en place des Vlans, un serveur DHCP, des règles ACL, des droit sur le service SSH, un serveur Web.
















Règles ACL d'apres R103, manière d'isoler les Vlan