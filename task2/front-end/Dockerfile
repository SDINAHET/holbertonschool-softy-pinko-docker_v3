# Utiliser la dernière image Nginx
FROM nginx:latest

# Copier les fichiers du front-end
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copier le fichier de configuration Nginx
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Exposer le port 9000
EXPOSE 9000
