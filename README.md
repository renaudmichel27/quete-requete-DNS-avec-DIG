Utilise la commande dig pour récupérer les informations suivantes :

    les adresses IP version 4 du site web de la Wild Code School ! www.wildcodeschool.com

dig A www.wildcodeschool.com -ou meme plus court - dig +short A www.wildcodeschool.com
199.60.103.225  et   199.60.103.31 
on voit une chaîne de CNAME vers HubSpot
le site www est servi via HubSpot.
    
    les adresses IP version 6 d'odyssey et en déduire l'hébergeur de ton fournisseur de quête préféré

dig +short AAAA odyssey.wildcodeschool.com
CNAME cible : ghs.googlehosted.com. 
IPv6 : 2a00:1450:4007:80d::2013
le service hébergé chez Google
    
    (Bonus) les noms des serveurs de noms faisant autorité sur le domaine wildcodeschool.com et le serveur primaire.
dig +short NS wildcodeschool.com et dig +short SOA wildcodeschool.com
kim.ns.cloudflare.com. ---  cash.ns.cloudflare.com.  ---   
l’autorité DNS est Cloudflare


    
    (Bonus) Refaire les requêtes précédentes en précisant l'utilisation du serveur récursif quad9 (9.9.9.9 ou 2620:fe::9)
dig @9.9.9.9 +short A www.wildcodeschool.com
dig @2620:fe::9 +short A www.wildcodeschool.com   (adresse de quad9 ipv6)
voir copie ecran
