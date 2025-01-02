# ResearchSpace Earthquake App

## Overview
The ResearchSpace Earthquake App is designed to provide an efficient setup for exploring and analyzing earthquake data within a ResearchSpace (RS) instance. This repository is structured into two main directories:

1. **`/rs-earthquake-app`** - Contains the core RS application, including its configuration files and page templates.
2. **`/rs-earthquake-docker`** - Contains the Docker setup for deploying the RS instance.

### Prerequisites
To ensure proper functionality, you must have:
- A local Blazegraph instance running.
- 

---

## Directory Structure

### `/rs-earthquake-app`
This directory contains:
- **Configuration Files**: These include settings specific to the RS Earthquake App.
- **Data**: All necessary page templates required for the app.

### `/rs-earthquake-docker`
This directory includes:
- **Dockerfiles**: Used to set up the RS instance.
- **Configuration Files**: Files required for Docker to configure and run the RS environment.
- **Scripts**: Helper scripts to build, run, and manage the Docker containers.

---

## Setup Instructions

### 1. Start a Local Blazegraph Instance
1. Download and set up Blazegraph from [Blazegraph GitHub](https://github.com/blazegraph/database).
2. Start the Blazegraph server locally.
3. Note the SPARQL endpoint (e.g., `http://localhost:9999/blazegraph/sparql`).

### 2. Configure SPARQL Endpoint
Update all relevant configuration files in `/rs-earthquake-app` and `/rs-earthquake-docker` to include the Blazegraph SPARQL endpoint (default.ttl)

### 3. Build and Run the Docker Environment
1. Navigate to `/rs-earthquake-docker`.
2. Build the Docker image:
   ```bash
   cd /local
   chmod +x fix-folder-permissions.sh
   ./fix-folder-permissions.sh
   docker-compose up -d
   ```

### 4. Access the Application
Open your browser and navigate to `http://localhost:8080` (or the port specified in the Docker setup).

---

## Troubleshooting
- **Blazegraph Connection Issues**: Ensure Blazegraph is running locally and the endpoint URL is correct.
- **Docker Build Errors**: Check the Dockerfile and ensure all dependencies are available.
- **Application Errors**: Verify that the configuration files in `/rs-earthquake-app` are correctly updated with your SPARQL endpoint.


## How-to WSL
1) Install blazegraph:
   https://migrationskb.github.io/MGKB/blazegraph
   ```
   sudo apt update
   sudo apt install default-jre 
   java --version 
   sudo apt install default-jdk
   javac --version 
   wget https://github.com/blazegraph/database/releases/download/BLAZEGRAPH_2_1_6_RC/blazegraph.jar
   
   java -server -Xmx4g -jar blazegraph.jar
   
   ```

2) Clone repo
3) Navigate to `/rs-earthquake-docker/local`
4) Start container, it is already configured using:
   ```
   docker-compose up -d
   ```