# Scalable Distributed Video-to-Audio Conversion System: A Microservices Approach with Kubernetes  

## Overview

This project showcases the implementation of microservice architecture and distributed systems using a stack of Python, Kubernetes, RabbitMQ, MongoDB, and MySQL. It's designed to efficiently convert video files into MP3 format, orchestrated through a series of specialized services for authentication, gateway routing, file conversion, and user notification. The system employs Kubernetes for seamless orchestration, RabbitMQ for reliable message queuing, MongoDB with GridFS for effective large file storage, and MySQL for robust data persistence.

## Quick Start

### Prerequisites
- Docker & Kubernetes (Minikube/cloud)
- Helm (for RabbitMQ setup)
- Python 3.8 or higher
- MongoDB & MySQL for database services

### Setup
To initialize the system, clone the repository, navigate to the project directory, and deploy the services using either Docker Compose or Kubernetes manifests.

## Core Services

- **Authentication Service**: Handles user authentication processes, utilizing Flask to generate and manage JWTs for secure interservice communication.
  
- **Gateway Service**: Acts as the primary entry point for the application, efficiently routing incoming requests to the appropriate backend services with Python and Flask.
  
- **Converter Service**: The core component responsible for converting video files to MP3 format, leveraging Python and FFmpeg for processing.
  
- **Notification Service**: Engages users by notifying them upon successful conversion of their files, enhancing the overall user experience.

## Architecture Insights

- **Kubernetes** is at the heart of service deployment, offering unparalleled scalability and resilience.
- **RabbitMQ** ensures efficient asynchronous communication across services, bolstering system scalability and reliability.
- **MongoDB & GridFS** provide a solid foundation for storing and managing large files without a hitch.
- **Synchronous & Asynchronous Communication** strategies are meticulously balanced to achieve peak system performance and decoupling.
- **Consistency Models** are carefully chosen based on service requirements, guaranteeing data integrity and seamless availability.

## Deployment Highlights

- **Authentication Service** makes use of Docker for containerization, with Kubernetes handling the deployment across the cluster.
- **Kubernetes Deployments, StatefulSets, and Ingress** are strategically leveraged to optimize service delivery and accessibility.
- **RabbitMQ** stands as a cornerstone for messaging within the system, deployed via Helm charts for robust scalability.
- **Converter Service** is designed to dynamically scale within Kubernetes, ensuring it meets demand without faltering.

This architecture not only exemplifies a modern approach to distributed systems but also provides a scalable, efficient solution for video-to-audio conversion needs.