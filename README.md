# Projet Ansible : Déploiement de GitLab BELLANGER Nicolas

## Description du projet

Ce projet vise à déployer un serveur **GitLab** de manière automatisée en utilisant **Ansible**. Il inclut également la mise en place optionnelle de bases de données PostgreSQL.

---

## Objectifs

1. **Déploiement d'un serveur GitLab via un rôle Ansible.**
2. **Déploiement de bases de données PostgreSQL (optionnel).**

---

## Commandes utiles

### Déploiement Ansible

Dans un premier temps, il vous faut changer l'addresse ip dans le fichier "inventory.yml" avec l'addresse de votre machine client.

Lancer les rôles :
```bash
ansible-playbook -i inventory.yaml playbook.yml
```
Vérfier vos containers docker sur votre machine cible :
```bash
docker ps
```
Pour accéder à votre gitlab, utiliser l'addresse IP de votre machine cliente :

Nom utilisateur : root

Pour trouver le mot de passe, allez dans votre machine cible :
```bash
docker exec -it <CONTAINER ID ou NAME> bash
cat /etc/gitlab/initial_root_password
```
