# Docker Telegraf Grafana Monitoring
## Monitoring Infrastructure with Grafana, InfluxDB, and Telegraf

[![Deploy](https://github.com/dongtranthien/docker-telegraf-grafana-monitoring/actions/workflows/deploy.yml/badge.svg)](https://github.com/dongtranthien/docker-telegraf-grafana-monitoring/actions/workflows/deploy.yml)
![License](https://img.shields.io/github/license/dongtranthien/docker-telegraf-grafana-monitoring)

## Overview

🚀 Welcome to the Docker Telegraf Grafana Monitoring repository! 

💡 This project aims to simplify the deployment and configuration of Grafana, InfluxDB, and Telegraf for monitoring virtual private servers (VPS), Google Compute Engine (GCE) instances, and DigitalOcean Droplets. The primary motivation behind this project is to automate the manual steps involved in setting up Grafana, InfluxDB, and Telegraf, making it easier to adapt to changes in virtual server environments.

## Features

🛠️ Key Features:
- Automated deployment using GitHub Actions and remote SSH.
- Dockerized setup for Grafana, InfluxDB, and Telegraf.
- Automatic configuration steps, including token retrieval from InfluxDB and adding InfluxDB as a data source in Grafana.

## Getting Started

🚦 To get started with monitoring your infrastructure, follow these steps:

1. **Fork the Repository on Your GitHub Account:**
   - Fork this repository to your GitHub account to enable easy deployment on your own server.

2. **Configure Secrets:**
   - Add the following SSH and InfluxDB credentials as secrets in your GitHub repository settings:
     - `SSH_HOST_NAME`: Hostname or IP address of your server.
     - `SSH_USER_NAME`: Your SSH username.
     - `SSH_PRIVATE_KEY`: Your SSH private key.
     - `SSH_PORT`: SSH port (default is 22).
     - `INFLUXDB_USER_NAME`: InfluxDB username.
     - `INFLUXDB_PASSWORD`: InfluxDB password.
     - `INFLUXDB_ORGANIZATION`: InfluxDB organization name.
     - `INFLUXDB_BUCKET`: InfluxDB bucket name.

3. **GitHub Actions Deployment:**
   - Manually trigger the deployment workflow using the "workflow_dispatch" event in GitHub Actions.

4. **Access Grafana:**
   - Grafana will be available at `http://your-server-ip:3000` (default login credentials: admin/admin).

## Repository Structure

📂 Repository Structure:
- `.github/workflows/deploy.yml`: GitHub Actions workflow for automated deployment.
- `docker-compose.yml`: Docker Compose file defining services for InfluxDB, Grafana, and Telegraf.
- `telegraf.conf`: Telegraf configuration file with CPU and memory monitoring settings.

## Notes

📝 **Important Notes:**
- Ensure that your server allows inbound traffic on ports 3000 (Grafana) and 8086 (InfluxDB).
- This setup assumes Docker is installed on the remote server.
- Customizations can be made in the `docker-compose.yml` file and the `telegraf.conf` configuration file.

## License

📄 This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Feel free to contribute, open issues, or provide feedback to enhance this monitoring solution! 🚀
