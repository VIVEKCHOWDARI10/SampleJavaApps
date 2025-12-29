# End-to-End CI/CD Pipeline with Jenkins, Docker, Argo CD & AWS EKS

# Project Overview:

   This project demonstrates a complete CI/CD (Continuous Integration & Continuous Deployment) pipeline that automates the build, containerization, and deployment of a Spring Boot  application on AWS EKS using GitOps principles.

  The pipeline is designed to:

  1.Build application code using Jenkins

  2.Create and push Docker images to Docker Hub

  3.Update Kubernetes deployment manifests automatically
  
  4.Deploy changes to an EKS cluster using Argo CD



 #  Architecture :

GitHub (Application Repo)
        -
        >
     Jenkins (CI)
        -
        >
    Docker Hub
        -
        >
GitHub (Manifests Repo - GitOps)
        -
        >
     Argo CD
        -
        >
     AWS EKS Cluster


# Repositories Used :   
                          	
Application Source Code             	https://github.com/VIVEKCHOWDARI10/SampleJavaApps

Kubernetes Manifests (GitOps)       	https://github.com/VIVEKCHOWDARI10/Jenkins


# Tools & Technologies :

* AWS EC2 – Jenkins & CI host

* AWS EKS – Kubernetes cluster

* Jenkins – CI pipeline

* Docker – Containerization

* Docker Hub – Image registry

* Argo CD – Continuous Deployment (GitOps)

* GitHub – Source control

* Maven – Build tool

* Spring Boot – Application framework



# CI/CD Workflow :

1. Developer pushes code to the application GitHub repository

2. Jenkins pipeline is triggered

3. Jenkins Clones application repo

4. Builds the application using Maven

5. Builds a Docker image

6. Pushes the image to Docker Hub

7. Jenkins updates the Kubernetes deployment YAML with the new image tag

8. Argo CD detects changes in the manifests repository

9. Argo CD automatically syncs and deploys changes to AWS EKS

 10. Application is accessible via Kubernetes Service (LoadBalancer)


     
