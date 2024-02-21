# Scalable Distributed Video-to-Audio Conversion System: A Microservices Approach with Kubernetes  

## Overview

This project is designed to demonstrate a practical implementation of a microservice architecture and distributed systems using Python, Kubernetes, RabbitMQ, MongoDB, and MySQL.The project is structured around several key services, including an Authentication Service, Gateway Service, Converter Service, and Notification Service. It leverages Kubernetes for orchestration, RabbitMQ for message queuing, MongoDB with GridFS for storing large files, and MySQL for persisting user data. 

## Quick Start

### Prerequisites
- Docker & Kubernetes (Minikube/cloud)
- Helm (for RabbitMQ)
- Python 3.8+
- MongoDB & MySQL

### Setup
Clone the repository and navigate into it. Deploy the services using Docker Compose or Kubernetes manifests.

## Core Services

### Authentication Service
Manages user authentication, leveraging Flask to issue JWTs for secure interservice communication.

### Gateway Service
Serves as the application's front door, directing requests to the right service using Python and Flask.

### Converter Service
The heart of MicroConvert, this service uses Python and FFmpeg to convert videos to MP3 format efficiently.

### Notification Service
Informs users upon the successful conversion of their files, closing the loop in the user experience.

## Architecture Insights

- **Kubernetes** orchestrates service deployment, ensuring scalability and resilience.
- **RabbitMQ** facilitates asynchronous communication, enhancing system scalability and reliability.
- **MongoDB & GridFS** efficiently store and manage large video and audio files.
- **Synchronous & Asynchronous Communication** are balanced for optimal performance and decoupling.
- **Consistency Models** tailored to service needs, ensuring data integrity and availability.

## Deployment Highlights

- **Auth Service** employs Docker for containerization and Kubernetes for cluster deployment.
- **Kubernetes Concepts** like Deployments, StatefulSets, and Ingress are strategically utilized.
- **RabbitMQ** is robustly deployed with Helm charts, underpinning the messaging infrastructure.
- **Converter Service** scales dynamically in Kubernetes to meet processing demands.

## Final Thoughts

MicroConvert represents a holistic approach to microservice architecture, emphasizing scalability, efficiency, and robustness in video-to-audio conversion. Through strategic deployment and innovative service design, it sets a benchmark for distributed system applications.
