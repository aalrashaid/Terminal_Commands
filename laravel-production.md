production

composer install — optimize-autoloader — no-dev
npm install
npm run prod
npm run production
cp .env.example .env
php artisan key:generate
chmod 755 -R [nameofyourproject]/
chmod -R o+w bootstrap/cache
chmod -R o+w [nameofyourproject]/storage
php artisan storage:link
php artisan route:cache
php artisan route:clear
php artisan cache:clear
php artisan view:clear
php artisan config:clear
