# gke-online-boutique-cost-optimization

# GKE Online Boutique – Cost Optimization

## Project Overview

This project demonstrates the deployment of the **Online Boutique microservices application** on Google Kubernetes Engine (GKE).

The main objective is to deploy a cloud-native application while optimizing infrastructure costs, improving performance, and maintaining application availability using Kubernetes features.

## Technologies Used

- Google Cloud Platform (GCP)
- Google Kubernetes Engine (GKE)
- Kubernetes
- Docker
- kubectl
- Horizontal Pod Autoscaler (HPA)
- Pod Disruption Budget (PDB)
- Linux / Shell Commands

## Project Objectives

1. Create a GKE zonal cluster.
2. Deploy the Online Boutique application.
3. Create separate `dev` and `prod` namespaces.
4. Migrate workloads to an optimized node pool.
5. Configure Pod Disruption Budget for frontend.
6. Update the frontend Docker image.
7. Configure Horizontal Pod Autoscaling.
8. Enable cluster autoscaling.
9. Perform load testing with 8000 concurrent users.
10. Optimize application performance and infrastructure costs.

## Implementation

### Task 1: Create GKE Cluster and Deploy Application

- Created a zonal GKE cluster with 2 nodes.
- Configured the Rapid release channel.
- Created `dev` and `prod` namespaces.
- Deployed Online Boutique into the dev namespace.

### Task 2: Optimize Node Pool

- Created a new node pool using `e2-custom-2-3584`.
- Configured 2 nodes.
- Cordon and drained the default node pool.
- Migrated workloads to the optimized node pool.
- Deleted the default node pool.

### Task 3: Frontend Update

- Created a Pod Disruption Budget.
- Configured minimum availability to 1.
- Updated the frontend container image to version `v2.1`.
- Set ImagePullPolicy to `Always`.

### Task 4: Autoscaling

- Configured frontend Horizontal Pod Autoscaler.
- Set target CPU utilization to 50%.
- Configured minimum and maximum pod replicas.
- Enabled cluster autoscaling between 1 and 6 nodes.
- Performed load testing with 8000 concurrent users.
- Configured recommendationservice autoscaling between 1 and 5 replicas.

## Application Source Code

Google Cloud Online Boutique:
https://github.com/GoogleCloudPlatform/microservices-demo

## Key Learnings

- Understanding Google Kubernetes Engine.
- Deploying microservices using Kubernetes.
- Managing Kubernetes namespaces and node pools.
- Implementing Horizontal Pod Autoscaling.
- Configuring cluster autoscaling.
- Managing application availability using PDB.
- Performing load testing.
- Optimizing cloud infrastructure costs.

## Conclusion

Successfully deployed the Online Boutique microservices application on GKE and implemented Kubernetes cost optimization techniques, node pool migration, and autoscaling to improve resource utilization and application availability.

## Author

Cloud & DevOps Learner

**Skills:** Google Cloud | GKE | Kubernetes | Docker | Linux | Autoscaling
