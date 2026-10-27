# Projet Datasea
## Refonte et sécurisation d’une infrastructure PME

**Projet pédagogique collectif — Administration systèmes et réseaux**

---

## 1. Présentation du projet

Ce projet a pour objectif d’analyser une infrastructure informatique de PME, d’identifier ses principales faiblesses et d’étudier des solutions pour améliorer sa sécurité, sa fiabilité et son organisation.

## 2. Problématiques identifiées

L’analyse de l’infrastructure initiale a mis en évidence plusieurs points à améliorer :

- **Réseau :** dépendance à un commutateur central et incohérences dans le plan d’adressage IP.
- **Sauvegardes :** espace de stockage des sauvegardes de machines virtuelles saturé.
- **Gestion des comptes :** présence d’anciens profils et de comptes nécessitant une révision des accès.
- **Sécurité :** nécessité de mieux organiser les droits et de limiter les privilèges.

---

## 3. Axes de travail

### Réseau et adressage IP

- Révision du plan d’adressage IPv4.
- Segmentation logique du réseau à l’aide de VLAN.
- Étude des besoins en matière de redondance et de disponibilité.

### Systèmes et gestion des identités

- Organisation d’Active Directory.
- Gestion des utilisateurs, des groupes et des permissions.
- Réexamen des comptes inactifs ou privilégiés.
- Prise en compte du principe du moindre privilège.

### Virtualisation et sauvegardes

- Étude et utilisation de Proxmox comme plateforme de virtualisation.
- Réflexion sur la disponibilité des services et la continuité d’activité.
- Révision de la stratégie de sauvegarde.

---

## 4. Environnement technique

| Domaine | Technologies |
|---|---|
| Systèmes | Windows Server 2022 |
| Gestion des identités | Active Directory |
| Réseau | TCP/IP, IPv4, VLAN |
| Virtualisation | Proxmox |
| Sécurité | Gestion des accès, moindre privilège |
| Continuité d’activité | Disponibilité et sauvegardes |

---

## 5. Démarche et retour d’expérience

Réalisé en équipe, ce projet m’a permis de travailler sur le diagnostic d’une infrastructure, l’identification de risques et l’étude de solutions adaptées aux besoins d’une PME.

Il met en évidence plusieurs enjeux de l’administration informatique : maintenir un environnement fiable, maîtriser les accès et concilier sécurité, disponibilité et facilité d’exploitation.

---

## 6. Documents du projet

Les livrables du projet seront ajoutés ici après vérification de leur contenu et des éventuelles informations confidentielles.

- Rapport de projet — PDF
- Présentation du projet — PDF
