# Carnet de Bord de groupe (Moad - Abdessabour - Jean Christophe)

### Séance du 25/03/2022 (TD non-encadrée) : 
---

* Nous avons configuré le pool DHCP sur le routeur partie virtuelle sur GNS3. Nous avons aussi commencer à penser à la configuration du serveur WEB, nous avons pour l'instant choisi d'utiliser le service apache (apache2).

### Séance du 29/03/2022 (TD encadrée) :
---

* Nous avons configuré le routeur plus précisément les pattes interne et externe.
* Configuration patte interne du routeur.

        conf t
        interface fastEthernet  0/0 "configuration patte interne"
        ip address 192.168.0.1 255.255.255.0
        no shutdown
        exit

* Configuration patte externe.

        conf t
        interface fastEthernet 0/1
        ip address dhcp
        no shutdown
        exit

* Configuration du pool DHCP sur le routeur, ceci va nous permettre d'avoir une adresse IP dans chaque machine (PC) du réseau.

        conf t
        ip dhcp pool LAN
        default-router 192.168.0.1
        dns-server 8.8.8.8
        network 192.168.0.0 255.255.255.0
        end
        wr mem

* Configuration du routeur en OSPF

        conf t
        routeur ospf 1
        network 192.168.0.0 0.0.0.255 area 0
        network 10.214.0.0 0.0.255.255 area 0
        end
        wr mem