
# Projet DATASC.SEA
## Étude et conception d'une infrastructure PME sécurisée

**Projet pédagogique collectif — Administration systèmes et réseaux · 2026**

---

## 1. Présentation du projet

DATASC.SEA est une entreprise fictive spécialisée dans l'exploitation et l'analyse de données marines.

Ce projet a pour objectif d'analyser son infrastructure informatique, d'identifier les principaux risques pesant sur le système d'information et de proposer une architecture cible plus sécurisée, résiliente et simple à administrer.

Le travail repose sur une analyse des risques et sur l'étude de solutions adaptées aux besoins d'une PME.

## 2. Contexte et risques identifiés

L'analyse de l'infrastructure initiale a notamment fait ressortir les problèmes suivants :

- **Réseau :** dépendance à un commutateur central et absence de segmentation logique.
- **Systèmes :** dépendance à un hyperviseur unique et présence de systèmes obsolètes.
- **Sauvegardes :** stockage saturé et stratégie de restauration insuffisante.
- **Contrôle des accès :** gestion des droits à renforcer et accès distants via TeamViewer.
- **Cybersécurité :** Wi-Fi utilisant le chiffrement WEP, risques de ransomware et de phishing.
- **Continuité d'activité :** absence de plan de reprise et de continuité d'activité formalisé (PRA/PCA).
- **Risques physiques :** exposition des locaux au risque d'inondation.

---

## 3. Architecture cible proposée

### Systèmes et virtualisation

- Deux serveurs Dell PowerEdge R360 sous **Microsoft Hyper-V**.
- Windows Server 2022 pour les services d'infrastructure.
- Active Directory pour la gestion centralisée des identités, des groupes et des permissions.
- Gestion des comptes inactifs et application du principe du moindre privilège.
- Migration du serveur Web vers un hébergement externe chez Hostinger.
- Supervision et amélioration du suivi des événements système.

### Réseau et haute disponibilité

- Segmentation du réseau à l'aide de VLAN et de règles de filtrage (ACL).
- Deux commutateurs Netgear GS728TP, avec étude de la résilience par stacking et LACP.
- Deux pare-feu Netgate 2100 sous pfSense, avec mécanisme de haute disponibilité CARP.
- Accès Internet principal FTTO et accès secondaire FTTH.
- Mise en place prévue d'un VPN WireGuard.
- Remplacement du chiffrement Wi-Fi WEP par WPA2/WPA3.

### Messagerie et sécurité

- Migration envisagée vers Microsoft 365 et Exchange Online.
- Protection de la messagerie avec SPF, DKIM et DMARC.
- Réduction de l'exposition des services internes.
- Microsoft Entra Connect identifié comme une possibilité d'évolution ultérieure.

### Sauvegardes et continuité d'activité

La stratégie étudiée s'appuie sur le principe **3-2-1-1-0** :

- NAS Synology DS225+ de 4 To en RAID 1.
- Sauvegardes complètes et incrémentales.
- Réplication vers AWS S3 Standard-IA.
- Archivage à long terme avec AWS Glacier Deep Archive.
- Copie hors ligne sur disque Seagate IronWolf Pro de 4 To.
- Définition d'objectifs de perte de données (RPO) et de reprise de service (RTO).

---

## 4. Environnement technique

| Domaine | Technologies et solutions |
|---|---|
| Systèmes | Windows Server 2022 |
| Virtualisation | Microsoft Hyper-V |
| Identités | Active Directory |
| Réseau | TCP/IP, IPv4, VLAN, ACL, LACP |
| Sécurité réseau | pfSense, CARP, WireGuard |
| Messagerie | Microsoft 365, Exchange Online, SPF, DKIM, DMARC |
| Sauvegardes | Synology, AWS S3, Glacier Deep Archive |
| Supervision | Centreon |

## 5. Analyse et démarche

Le projet a été réalisé en équipe. La démarche comprend :

1. L'analyse de l'infrastructure existante et l'identification des vulnérabilités.
2. L'évaluation des principaux risques et de leurs conséquences.
3. L'étude de solutions techniques adaptées aux besoins de l'entreprise.
4. La conception d'une architecture cible intégrant sécurité, segmentation, redondance et sauvegardes.
5. L'estimation budgétaire des évolutions proposées.

Le budget global estimé dans le rapport se situe entre **40 000 € et 50 000 €**.

## 6. Documents du projet

Les livrables seront ajoutés au dépôt après préparation des versions destinées à la consultation publique :

- Rapport final du projet (PDF).
- Présentation du projet (PDF).
- Schéma logique de l'architecture cible (PDF et image).

---

## 7. Retour d'expérience

Ce projet a permis d'aborder les enjeux d'un diagnostic d'infrastructure, de l'analyse des risques et de la conception d'une architecture adaptée à une PME.

Il met notamment en évidence l'importance de la segmentation réseau, de la maîtrise des accès, de la redondance des services et d'une stratégie de sauvegarde permettant de mieux faire face aux incidents.
