# gh
bash <(curl -s https://pterodactyl-installer.se)

panel install

bash <(curl -s https://raw.githubusercontent.com/freediamodns/sanjitpanel/refs/heads/main/panel)

wings

sudo su
bash <(curl -s https://raw.githubusercontent.com/freediamodns/sanjitpanel/refs/heads/main/wings)

cmds

cd pterodactyl

sudo su

nano /etc/pterodactyl/config.yml

paste you config

cd wings

docker-compose up -d --force-recreate



























# 🚀 Sanjit Panel & Wings Setup Guide

![GitHub Repo Size](https://img.shields.io/github/repo-size/clevertech9977/sanjitpanel)
![License](https://img.shields.io/github/license/clevertech9977/sanjitpanel)

Welcome to the **Sanjit Panel & Wings Installer**. Follow these **step-by-step commands**, ready to copy.

---

## ⚡ Step-by-Step Installation

### Step 1️⃣: Switch to root
```bash
sudo su
Step 2️⃣: Install Sanjit Panel & Wings
bash
Copy code
bash <(curl -s https://raw.githubusercontent.com/clevertech9977/sanjitpanel/main/wings)
Step 3️⃣: Navigate to Pterodactyl config
bash
Copy code
cd pterodactyl
sudo su
nano /etc/pterodactyl/config.yml
Paste your configuration in config.yml

Step 4️⃣: Start Wings with Docker
bash
Copy code
cd wings
docker-compose up -d --force-recreate
Step 5️⃣: Check running containers
bash
Copy code
docker ps
Step 6️⃣: Stop Wings containers
bash
Copy code
docker-compose down
Step 7️⃣: Restart Wings
bash
Copy code
docker-compose restart
Step 8️⃣: Follow logs for troubleshooting
bash
Copy code
docker-compose logs -f
🛠️ Troubleshooting Common Errors
Git blocking installation
bash
Copy code
sudo fuser -v /usr/bin/git
sudo umount /usr/bin/git
sudo rm /usr/bin/git
sudo rm -rf /usr/lib/git
sudo rm -rf /etc/gitconfig
sudo apt update
sudo apt install git
Docker-compose permission issues
bash
Copy code
sudo chmod +x /usr/local/bin/docker-compose
sudo systemctl restart docker
Overlay filesystem / container errors
bash
Copy code
sudo umount /shared
sudo umount /usr/bin/git
SSH or VM connection problems
bash
Copy code
ssh -p 443 user@localhost
Make sure VM is running with correct ports.

🔹 Notes & Tips
✅ Run all commands as root.

✅ Ensure Docker and Docker Compose are installed.

⚠️ Avoid multiple VM or overlay environments that block /usr/bin/git.

💡 Use docker-compose logs -f to debug any issues.

📌 Quick Links
Sanjit Panel GitHub

Docker Docs

Pterodactyl Docs

⭐ How to enable copy buttons on GitHub
GitHub automatically shows copy buttons on fenced code blocks (```bash) when viewed in a repo.
Push this README to your repository:

bash
Copy code
git add README.md
git commit -m "Add full Sanjit Panel setup guide with troubleshooting"
git push origin main
Now, any user visiting your GitHub repo can click copy on each command and run it directly.





#!/bin/bash
# ===============================================
# 🚀 Sanjit Panel + Wings All-in-One Installer
# ===============================================

echo "🔹 Switching to root..."
sudo su

echo "🔹 Fixing Git issues if present..."
if [ -f /usr/bin/git ]; then
    sudo fuser -v /usr/bin/git
    sudo umount /usr/bin/git || true
    sudo rm -rf /usr/bin/git /usr/lib/git /etc/gitconfig
fi
sudo apt update && sudo apt install -y git curl docker.io docker-compose

echo "🔹 Installing Sanjit Panel & Wings..."
bash <(curl -s https://raw.githubusercontent.com/clevertech9977/sanjitpanel/main/wings)

echo "🔹 Starting Wings with Docker..."
cd wings
docker-compose up -d --force-recreate

echo "🔹 Checking running containers..."
docker ps

echo "🔹 Setup complete!"
echo "🔹 Navigate to Pterodactyl config if needed:"
echo "cd pterodactyl && sudo nano /etc/pterodactyl/config.yml"

echo "🔹 Troubleshooting tips:"
echo "- Use 'docker-compose logs -f' to view logs"
echo "- Ensure Docker service is running: 'sudo systemctl restart docker'"
echo "- Run all commands as root for best results"
🔹 Usage:
Copy this script to a file:

bash
Copy code
nano install_sanjit.sh
Paste the script above, save and exit (CTRL+O, CTRL+X).

Make it executable:

bash
Copy code
chmod +x install_sanjit.sh
Run it:

bash
Copy code
./install_sanjit.sh
Hii itafanya Git fixes, Docker install, Sanjit Panel & Wings install, na container start kwa copy-paste moja tu.



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
