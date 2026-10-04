Setup for moodle localy via Docker  

PreRequisites :  
-Docker desktop installed and launched  
-With windows - wsl2 activated (wsl --install) and integrated to docker desktop (Settings, Ressources, WSL integration)  

'''bash  
git clone https://github.com/stayxyats/Setup-docker-for-moodle moodle-docker  
cd moodle-docker  
git clone --depth 1 -b MOODLE_405_STABLE https://github.com/moodle/moodle.git moodle  
docker compose up -d  
docker compose exec web chown -R www-data:www-data /var/www/moodledata  
chmod -R 777 moodle  
'''

BaseType -> PostgreSQL  
Serveur -> db  
DB name -> moodle
user -> moodle  
password -> moodle
