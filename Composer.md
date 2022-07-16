Composer

curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php

HASH=`curl -sS https://composer.github.io/installer.sig`

echo $HASH

php -r "if (hash_file('SHA384', '/tmp/composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

composer


php composer.phar --version

sudo mv composer.phar /usr/bin/composer

mv composer.phar ~/.local/bin/composer

composer --version


alias composer="php /usr/local/bin/composer.phar"

source ~/.bashrc
