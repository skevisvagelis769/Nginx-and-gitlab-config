The NGINX Reverse Proxy is currently handling routing for: 
http://opencloud2025.duckdns.org/
AND 
http://opencloud2025.duckdns.org/gitlab
where our GitLab is hosted.

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

sudo nano /etc/nginx/sites-available/grafana.conf


sudo ln -s /etc/nginx/sites-available/grafana.conf/etc/nginx/sites-enabled/

sudo nginx -t

sudo systemctl reload nginx
