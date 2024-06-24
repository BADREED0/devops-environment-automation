# devops-environment-automation

## Description
Dans ce projet, nous utilisons trois outils DevOps : Docker, Vagrant et Ansible pour automatiser la création de deux environnements (test et prod) avec des conteneurs Apache.

## Prérequis
- Vagrant
- VirtualBox
- Ansible
- Docker    

## Instructions
1. Démarrer les machines virtuelles :
```bash
vagrant up
```
2. Une fois les VMs démarrées, utiliser Ansible pour déployer les conteneurs :
```bash
ansible-playbook -i ansible/inventory.ini ansible/deploy.yml
```

## Détails Techniques

- **Vagrant** est utilisé pour gérer les machines virtuelles.
- **Ansible** est utilisé pour provisionner les machines et déployer les conteneurs.
- **Docker** est utilisé pour créer et gérer les conteneurs d'application.

