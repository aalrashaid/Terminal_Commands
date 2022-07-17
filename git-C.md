create a new repository on the command line :

echo "# Recipes-App" >> README.md
git init
git add README.md
git commit -m "new Laravel APP"
git branch -M main
git remote add origin https://github.com/aalrashaid/Recipes-App.git
git push -u origin main

push an existing repository from the command line:
git remote add origin https://github.com/aalrashaid/Recipes-App.git
git branch -M main
git push -u origin main
