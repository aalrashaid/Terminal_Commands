sudo apt-get update
---
software-properties-common:
sudo apt -y install software-properties-common
sudo add-apt-repository ppa:ondrej/php
---
sudo apt-get update
---
sudo apt  install php7.4-cli php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath php7.4-fpm
php -v
sudo apt-get install php7.4-PACKAGE_NAME
sudo apt-get install -y php7.4-cli php7.4-json php7.4-common php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath php7.4-fpm

sudo apt install php-fpm php-mysql

php -m
---
sudo update-alternatives --config php

sudo update-alternatives --set php /usr/bin/php7.4
sudo update-alternatives --set phar /usr/bin/phar7.4
sudo update-alternatives --set phar.phar /usr/bin/phar.phar7.4
sudo update-alternatives --set phpize /usr/bin/phpize7.4
sudo update-alternatives --set php-config /usr/bin/php-config7.4
---
sudo mkdir /var/www/your_domain
--
sudo chown -R $USER:$USER /var/www/your_domain
--
server {
    listen 80;
    server_name [your_domain] [www.your_domain];
    root /var/www/[your_domain];

    index index.html index.htm index.php;

    location / {
        try_files $uri $uri/ =404;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
     }

    location ~ /\.ht {
        deny all;
    }

}

---
sudo ln -s /etc/nginx/sites-available/your_domain /etc/nginx/sites-enabled/
---
sudo unlink /etc/nginx/sites-enabled/default
---
sudo ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled/
---
sudo nginx -t
---
sudo systemctl reload nginx
---
nano /var/www/your_domain/index.html
--
nano /var/www/your_domain/info.php

<?php
phpinfo();
