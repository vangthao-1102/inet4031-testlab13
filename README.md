# Docker Lab: Containerizing a Three-Tier Application
**INET 4031 - Introductions to Systems**

This lab introduces Docker and Docker Compose by having you containerize a
real, multi-service application. You will package three components: Apache,
Flask, and MariaDB. These will be packaged into separate containers and wired together so they function as a complete application.

The application code and scaffolding are provided. Your job is to complete the Dockerfiles, verify the stack runs correctly, and document your work below.

> **Directions and explanations for this lab are on the repository Wiki.**
> Refer to the Wiki pages for step-by-step instructions.

---

*The sections below are for you to fill out. Replace each placeholder with your own content before submitting. Having a detailed README is the best practice for showing your work in future GitHub repositories.*

---

# Project Overview

The application serves to help create a simple container that hosts a ticketing system for users. The user can add ticket through the terminal or through te website if they wished to do so. The main problem this application solves is to create and learn what containers are and how they can be setup to run a web server. The user will be interacting with starting up and closing the application through Docker.

# Prerequisites

Before starting this lab, the user must make a new VM that has enough space and the correct hardware components (refer to wiki). But, if the VM has already been made, there is no need to tweak anything else before the lab begins. The only new thing that needs to be installed would be visual studio code as that is going to be the interface that users will be using instead of the normal terminal.

As for what is needed to be installed inside the VM, the user will need to install all of Docker and make sure that the configurations for it is running and working. Without Docker downloaded, the lab will not work as intended. Docker is the container that is going to be used in the lab, without this no container can be set up.

1. Docker: the engine
2. Docker Compose: tool that helps to run container applications
3. Have a git created
4. Double check sudo is enabled on Docker

# Getting Started

1. Clone repo using - git clone (insert link of repo)
2. Create Enviornment - cp .env.example .env
3. Build and Start the Containers - sudo docker-compose up --build -d
4. Verify working - sudo docker ps

# Configuration

The .env file is where all the sensitive data is located. it also allows for the user to configure if needed. The variables contained are all related to the mySQL to allow for users to login. It also involves variables that relate to connections, such as Flask. In this repo, there is no .env file as this is something that users should create on their own to run their own enviornments. This ensures that everything runs and is working.

# Verification

Things to do to double check working and healthy:

1. Open browser tab and input - http://localhost:80 or http://(your VM IP):80
2. Run check script - make sure to turn this into an executable. A passing check is when everything is passed and a final message tells that everything has been passed.

# Feedback (Optional)

This Lab was interesting. Getting to learn how to connect SSH through visual studio code was something that I really liked. Using the terminal all the time is fine, but the visual studio code interface is a lot better when it comes to organization. Being able to learn how to get containers up and running was also very interesting. Overall, the lab helped to teach and give on hands learning on how to properly start a Docker container. As well as learning how to hide files and knowing how to create configuration files.

# Lab 13 - Kubernetes 

New changes made to this is the shift to Kubernetes instead of Docker Compose. The application is now being ran through using Deployments, Services, and Secrets. Doing this allows for dynamic health checks and restoration when containers are down, as compared to Docker Compose. 

1. Use command *kubectl apply -f k8s/* to deply the application
2. *http://(VM-IP):30080* is the URL access to check dashboard

# Feedback (Lab13): 
Clear and concise lab instructions. Biggest takeaway is the inbetween questions given to the user to answer before moving onto doing more of the interactive parts of the lab. As tedious and sometimes a bit annoying the questions are, they serve to help build concepts and the "why" of what is being done in the more interactive parts of the lab 13. Seeing the live updates of pods/containers working and being deployed is also very good as it provides immediate live feedback to the user. 
