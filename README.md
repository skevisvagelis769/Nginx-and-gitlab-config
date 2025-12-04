================== Gitlab setup ==========================

mkdir gitlab
cd gitlab
mkdir config data logs
cd config 
nano gitlab.rb 

cd .. 

nano docker-compose.yml
docker compose up


================= NGINX setup ===============================
sudo apt install nginx

sudo nano /etc/nginx/sites-available/gitlab.conf

sudo ln -s /etc/nginx/sites-available/gitlab.conf /etc/nginx/sites-enabled/

sudo nginx -t
sudo systemctl reload nginx
