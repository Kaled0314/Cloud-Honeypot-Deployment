# Cloud-Honeypot-Deployment

# Overview 

This project lists the entire process of configuring, deploying, and operating a T-Pot onto a secure cloud server. T-Pot is a platform built for multi-honeypots, meant to capture, analyze, and moitor malicious traffic in real time, providing insight into the methods and tools attackers are currently using. 

Honeypots are an extremely valuable asset within cybersecurity, they provide us with tools to deploy an isolated environment fully under our control where we can observe attackers without risking any of our data to potential exposure. This project applies that concept in a practical setting, walking through the entire deployment process from initial setup to active monitoring.

The walkthrough covers the provisioning of a cloud server through DigitalOcean, securing the environment through proper user management and SSH hardening, installing and configuring T-Pot, accessing the web interface to monitor incoming threats, and analyzing real world attack data as it is collected.

The goal of this project is to be a gateway introduction into working with Honeypots as they can come off as daunting to some. Wherever a student is at with their skills and knowledge, this project provides users a in depth view of how honeypot technology operates in a live, realistic scenario.

# Skills Learned

Cloud Server Deployment: Provisioned and configured a DigitalOcean droplet with sufficient resources to host the T-Pot platform.
Linux Server Administration: Managed system updates, user accounts, and administrative privileges to maintain a secure server environment.
Honeypot Installation and Configuration: Deployed T-Pot and developed a working understanding of its architecture and core services.
Web Interface Monitoring: Navigated the T-Pot web interface to observe and interpret live attack activity in real time.
Data Collection and Documentation: Recorded and documented honeypot activity over time to support analysis and review.

# Implementation

Step 1: Initialize a protected cloud environment
To kick things off, I set up a DigitalOcean account and launched a cloud droplet to serve as a secure and isolated environment for the project. Since the project would require running multiple honeypot services and monitoring tools at the same time, I made sure the droplet was equipped with enough resources to handle the workload, configuring it with 4 CPUs, 160 GB of RAM, and 5 TB of storage.
<img width="543" height="397" alt="Screenshot 2026-03-11 at 2 17 14 PM" src="https://github.com/user-attachments/assets/9c3c41c9-fa26-4a5f-b1cd-ee5800104fe6" />

Step 2: Creating a Non-Root User

After entering the droplet console, I began to create a Home user to install T-Pot and not under the Root user. The commands required to do this were: 
adduser home
Su - home

<img width="559" height="306" alt="Screenshot 2026-03-11 at 2 18 28 PM" src="https://github.com/user-attachments/assets/fd5493e3-effd-48df-9d38-b00a4ed29ae1" />

<img width="559" height="102" alt="Screenshot 2026-03-11 at 2 18 46 PM" src="https://github.com/user-attachments/assets/4286d85b-cd0e-40cc-bcaa-7223115315fb" />


