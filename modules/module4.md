## Introduction du module 4 et objectifs

- Concepts de base de la mise en réseau
- Différence entre des ressources de mise en réseaux publics et privés 
- Passerelle de réseau privé virtuel
- Réseau privé virtuel (VPN)
- Avantages d'AWS Direct Connect 
- Avantages des déploiements hybrides 
- Couches de sécurité utilisées dans une stratégie informatique
- Services que les clients utilisent pour interagir avec le réseau mondial AWS

---

## Amazon VPC (Virtual Private Cloud)

- service de mise en réseau que vous pouvez utiliser pour établir des limites autour de vos ressources AWS.
- mettre en service une section isolée du Cloud AWS. Dans cette section isolée, vous pouvez lancer des ressources dans un réseau virtuel que vous définissez. Dans un cloud privé virtuel (VPC), vous pouvez organiser vos ressources en sous-réseaux. Un sous-réseau est une section d'un VPC qui peut contenir des ressources telles que des instances Amazon EC2.

---

## Amazon VPC (Virtual Private Cloud)

![](../images/vpc.png)<!-- .element height="55%" width="55%" --> 

---

## Passerelle Internet (Internet Gateway)

Pour autoriser le trafic public à partir d'Internet à accéder à votre VPC, associez une passerelle Internet au VPC.

![](../images/ig.png)<!-- .element height="55%" width="55%" --> 

---

## Passerelle de réseau privé virtuel (Virtual Private Gateway)

- Une passerelle de réseau privé virtuel vous permet d'établir une connexion de réseau privé virtuel (VPN) entre votre VPC et un réseau privé, tel qu'un centre de données sur site ou un réseau interne d'entreprise. 
- Une passerelle réseau privé virtuel autorise le trafic vers le VPC uniquement s'il provient d'un réseau approuvé.

![](../images/passerelle-reseau-privee.png)<!-- .element height="55%" width="55%" --> 

## AWS Direct Connect

-  Service qui vous permet d'établir une connexion privée dédiée entre votre centre de données et un VPC

![](../images/direct-connect1.png)<!-- .element height="55%" width="55%" --> 

---

## AWS Direct Connect : Details

![](../images/direct-connect.png)<!-- .element height="55%" width="55%" --> 

---

## Sous-réseaux

- Un sous-réseau est une section d'un VPC dans laquelle vous pouvez regrouper des ressources en fonction des besoins de sécurité ou opérationnels. Les sous-réseaux peuvent être publics ou privés.
- Les sous-réseaux publics contiennent des ressources qui doivent être accessibles au public, telles que le site web d'une boutique en ligne.
- Les sous-réseaux privés contiennent des ressources qui ne doivent être accessibles que par l'intermédiaire de votre réseau privé, par exemple une base de données contenant les informations personnelles des clients et l'historique des commandes. 
- Dans un VPC, les sous-réseaux peuvent communiquer entre eux. Par exemple, vous pouvez avoir une application qui implique des instances Amazon EC2 dans un sous-réseau public communiquant avec des bases de données situées dans un sous-réseau privé.

---

## Sous-réseaux : Suite

![](../images/sous-reseau.png)<!-- .element height="55%" width="55%" --> 

---

## ACL réseau : schéma du principe

![](../images/acl.png)<!-- .element height="55%" width="55%" --> 

---

## ACL réseau

- Une liste de contrôle d'accès (ACL) réseau est un pare-feu virtuel qui contrôle le trafic entrant et sortant au niveau des sous-réseaux
- Chaque compte AWS inclut une liste ACL réseau par défaut
- Lors de la configuration de votre VPC, vous pouvez utiliser la liste ACL réseau par défaut de votre compte ou créer des listes ACL réseau personnalisées. 
- La liste ACL réseau par défaut de votre compte autorise tout le trafic entrant et sortant
-  Pour les ACL réseau personnalisées, tout le trafic entrant et sortant est refusé jusqu'à ce que vous ajoutiez des règles pour spécifier le trafic à autoriser
- Les listes ACL réseau effectuent un filtrage des paquets **sans état (stateless)** Ils ne se souviennent de rien et vérifient les paquets qui traversent la frontière du sous-réseau dans les deux sens : entrants et sortants. 
- Une fois qu'un paquet est entré dans un sous-réseau, ses autorisations doivent être évaluées pour les ressources du sous-réseau, telles que les instances Amazon EC2. 

---

## Groupe de sécurité : schéma du principe

![](../images/sg.png)<!-- .element height="55%" width="55%" --> 

---

## Groupe de sécurité

- Un groupe de sécurité est un pare-feu virtuel qui contrôle le trafic entrant et sortant d'une instance Amazon EC2.
- Par défaut, un groupe de sécurité refuse tout le trafic entrant et autorise tout le trafic sortant.
- Si vous avez plusieurs instances Amazon EC2 au sein d'un même VPC, vous pouvez les associer au même groupe de sécurité ou utiliser des groupes de sécurité différents pour chaque instance. 
- Les groupes de sécurité effectuent un filtrage des paquets avec état. Ils se souviennent des décisions antérieures prises pour les paquets entrants.

---

## Groupe de sécurité vs ACL

![](../images/sg-acl.png)<!-- .element height="55%" width="55%" --> 

---

## Simulation d'un paquet qui part d'une instance A à une instance B dans deux sous réseaux différents d'un même VPC

![](../images/simulation.png)<!-- .element height="55%" width="55%" --> 


