sudo apt update
sudo apt install nginx
---
sudo ufw app list
---
sudo ufw allow 'Nginx HTTP'
Or
sudo ufw enable
---
sudo ufw status
---
systemctl status nginx
--
curl -4 icanhazip.com
---
Managing the Nginx Process

sudo systemctl stop nginx

sudo systemctl start nginx

sudo systemctl restart nginx

sudo systemctl reload nginx

sudo systemctl disable nginx

sudo systemctl enable nginx

---
Setting Up Server Blocks (Recommended)

sudo mkdir -p /var/www/your_domain/html

sudo chown -R $www-data:$www-data /var/www/your_domain/html

sudo chmod -R 755 /var/www/your_domain

sudo nano /var/www/your_domain/html/index.html

sudo nano /etc/nginx/sites-available/your_domain

server {
        listen 80;
        listen [::]:80;

        root /var/www/your_domain/html;
        index index.html index.htm index.nginx-debian.html;

        server_name your_domain www.your_domain;

        location / {
                try_files $uri $uri/ =404;
        }
}

sudo ln -s /etc/nginx/sites-available/tolearing /etc/nginx/sites-enabled/

sudo nano /etc/nginx/nginx.conf


sudo nginx -t

sudo systemctl restart nginx
