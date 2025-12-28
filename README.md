# gh
# 🚀 Sanjit Panel & Wings Setup Guide

![GitHub Repo Size](https://img.shields.io/github/repo-size/clevertech9977/sanjitpanel)
![License](https://img.shields.io/github/license/clevertech9977/sanjitpanel)

Welcome to the **Sanjit Panel** installation guide. This README will help you set up both **Panel** and **Wings** quickly on your server.

---

## 1️⃣ Panel Installation

Run the following command to install **Panel**:

```bash
# Switch to root user
sudo su

# Install panel
bash <(curl -s https://raw.githubusercontent.com/clevertech9977/sanjitpanel/main/wings)

# Switch to root user if not already
sudo su

# Install Wings
bash <(curl -s https://raw.githubusercontent.com/clevertech9977/sanjitpanel/main/wings)

cd pterodactyl
sudo su
nano /etc/pterodactyl/config.yml


cd wings
docker-compose up -d --force-recreate


# Check running containers
docker ps

# Stop containers
docker-compose down

# Restart Wings
docker-compose restart


docker-compose logs -f
