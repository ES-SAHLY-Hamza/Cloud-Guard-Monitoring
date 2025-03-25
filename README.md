<img src="https://messungbacd.com/images/solutions/cloud-analysis.jpg" alt="Parc" width="1300" height="450"/>

# Monitoring Cloud and IoT 

Ce projet et son architecture ont été conçus dans le cadre d'une solution IoT basée sur une architecture microservices. Il permet la gestion et la surveillance des dispositifs connectés en temps réel.

## Description

Monitoring Cloud and IoT est une plateforme qui assure l'authentification des utilisateurs, l'administration des dispositifs IoT et la collecte des données transmises. Cette solution repose sur une architecture scalable et modulaire facilitant l'intégration de nouveaux services.

## Architecture du projet

L'application est composée de plusieurs microservices communiquant entre eux :

1. **Signing Microservice**
   - Gère l'authentification et l'autorisation des utilisateurs.
   - Technologies : Flask, PostgreSQL, Redis.

2. **Device Management Microservice**
   - Assure l'enregistrement, la configuration et le suivi des appareils IoT.
   - Technologies : Flask, PostgreSQL, Redis.

3. **Monitoring Microservice**
   - Collecte et affiche en temps réel les données envoyées par les dispositifs IoT.
   - Technologies : Flask, MongoDB, Socket.IO.

L'infrastructure repose sur **Docker** et **Kubernetes**, avec **RabbitMQ** pour la communication asynchrone entre les services.

## Communication entre microservices

- **Signing & Device Management** : Communication via API REST.
- **Device Management & Monitoring** : Communication asynchrone via RabbitMQ.
- **Monitoring** : Mise à jour des clients en temps réel avec WebSockets (Socket.IO).

## Technologies utilisées

- **Backend** : Flask (Python)
- **Base de données** : PostgreSQL, Redis, MongoDB
- **Messagerie** : RabbitMQ
- **Temps réel** : Socket.IO
- **Orchestration** : Kubernetes
- **Containerisation** : Docker
- **API Gateway** : Nginx
- **Monitoring** : Prometheus, Grafana
- **IoT Simulation** : MQTT

## Structure du projet

```
Monitoring-Cloud-IoT/
│── microservices/
│   │── device-management/
│   │── monitoring/
│   │── signing/
│   │── gateway/
│   │── nginx/
│── front-end/
│── kubernetes/
│── docker-compose.yml
│── README.md
```

## Installation et exécution

### Prérequis

- Python 3.9+
- Docker & Docker Compose
- Kubernetes (MicroK8s ou Minikube)
- PostgreSQL, Redis, MongoDB

### Lancer les services avec Docker Compose

```bash
docker-compose up --build
```

### Déploiement sur Kubernetes

```bash
kubectl apply -f kubernetes/
```

## Auteurs

Projet réalisé ES-SAHLY Hamza.

