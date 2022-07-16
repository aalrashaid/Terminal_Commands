nodejs
sudo apt update

sudo apt install nodejs
node -v

sudo apt install npm

Option 2 — Installing Node.js
cd ~
curl -sL https://deb.nodesource.com/setup_16.x -o /tmp/nodesource_setup.sh
nano /tmp/nodesource_setup.sh
sudo bash /tmp/nodesource_setup.sh
sudo apt install nodejs
node -v
---
Option 3 — Installing Node
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
source ~/.bashrc
source ~/.bash_profile
Option 3 — Installing Node
nvm install v14.10.0
nvm list
