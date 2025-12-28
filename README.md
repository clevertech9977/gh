# gh
panel install
bash <(curl -s https://raw.githubusercontent.com/freediamodns/sanjitpanel/refs/heads/main/wings)

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
