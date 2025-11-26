# README – SAE-502 : Pilotage d’un projet informatique
## Double réseau avec DHCP, Firewall, NAT et contrôles d’accès

---

## Équipe

- **Wasim** — Scrum Master  
- **Serkan** — Lead Developer  
- **Loan** — Membre du groupe  
- **Walid** — Membre du groupe  

---

## Objectif du projet

Ce projet consiste à :

- Construire un réseau complet dans GNS3 avec tous les équipements demandés  
- Mettre en place un double réseau interne de 6 machines chacun  
- Configurer un routeur DHCP fournissant deux services DHCP distincts  
- Déployer un firewall (FW) entre le routeur DHCP et l’accès Internet  
- Installer un NAT simulant la connexion vers l’extérieur  
- Paramétrer trois switchs pour répartir et trier les machines  
- Ajouter des règles firewall permettant :  
  - d’autoriser certaines machines à accéder à Internet  
  - et d’en bloquer d’autres  
- Documenter le réseau, gérer l’avancement via Trello  
- Versionner le projet étape par étape sur GitHub  

Le projet final doit permettre d’ouvrir le fichier GNS3 et d’obtenir un réseau **fonctionnel**, entièrement adressé via **DHCP**, avec un **firewall opérationnel** contrôlant l’accès à Internet.

---

## Description générale de la topologie

L’architecture du réseau suit la structure suivante :

- Un nœud **NAT** simulant la connexion externe  
- Un routeur **FW** jouant le rôle de pare-feu  
- Un routeur **DHCP** distribuant les adresses aux deux réseaux internes  
- Trois switchs : **S1**, **S2**, **S3**  
- Deux sous-réseaux internes distincts réunissant 12 machines  
- Des règles firewall spécifiques autorisant ou interdisant certains flux  

Cette topologie assure :

- une séparation claire des deux réseaux internes  
- un contrôle précis du trafic via le FW  
- un adressage entièrement automatisé grâce au DHCP  

---

## Fonctionnalités implémentées

### Double réseau interne (2 × 6 machines)
Topologie conforme aux spécifications du TP.

### DHCP fonctionnel
Le routeur DHCP attribue automatiquement les adresses IP aux machines des deux sous-réseaux.

### Firewall opérationnel
Le routeur FW :

- route le trafic interne ↔ externe  
- filtre le trafic sortant  
- peut autoriser ou bloquer Internet pour certaines machines  

### NAT fonctionnel
Le nœud NAT simule correctement un accès externe.

### Switchs configurés
Les trois switchs distribuent correctement les machines dans les deux réseaux.

### Travail collaboratif (Agile)
- Avancement géré via Trello  
- Commits réguliers sur GitHub  
- Rôles Scrum Master / Lead Developer respectés  

---

## Outils nécessaires

### 🔹 GNS3  
Téléchargement :  
https://gns3.com/software/download

### 🔹 Git Bash  
Pour cloner et gérer le dépôt Git :  
https://git-scm.com/downloads

### 🔹 VMware Workstation / Player  
Indispensable pour le fonctionnement du NAT sous GNS3 :  
https://www.vmware.com/products/workstation-player.html

### 🔹 Image Cisco C7200  
Utilisée pour les routeurs Cisco du projet :  
https://upw.io/4ui/c7200-advipservicesk9-mz.152-4.S5.image  

---

## Comment lancer le projet

1. Installer GNS3, Git Bash, VMware et importer l’image Cisco C7200  
2. Cloner le dépôt GitHub  
3. Ouvrir le projet dans GNS3  
4. Démarrer les routeurs puis les machines  
5. Vérifier que les machines obtiennent bien une adresse via DHCP  
6. Tester la connectivité interne  
7. Tester l’accès Internet simulé  
8. Vérifier les règles firewall (machines autorisées / bloquées)

---

## Organisation du travail (Méthode Agile)

### Trello
- Tableau configuré par le Scrum Master  
- Colonnes : **À faire**, **En cours**, **A Tester**, **Terminé**  
- Chaque membre déplaçait les tickets correspondant à son travail  
- Suivi continu de l’avancement

### Git / Versionnement
- Dépôt initialisé par le Lead Developer  
- Commits réguliers et cohérents  
- Fichiers volumineux exclus  
- Historique clair et structuré  

---

## Tests réalisés

Nous avons validé :

- Attribution automatique des adresses IP via DHCP  
- Communication interne dans chaque réseau  
- Communication entre les deux réseaux internes  
- Communication vers l’extérieur via le NAT  
- Blocage Internet pour certaines machines selon les règles firewall  
- Accès Internet autorisé uniquement pour les machines prévues  
- Fonctionnement global du routage  

---

## Contenu du dépôt

- Fichier du projet GNS3  
- README.md    

---

## Statut final
Le réseau est **opérationnel**, **documenté**, **versionné**, et respecte toutes les exigences du projet SAE-502.
# SAE-502
