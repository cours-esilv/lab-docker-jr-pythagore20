# Utiliser une image légère d'un serveur web comme image parent
FROM nginx:alpine

# Définir le répertoire de travail dans le conteneur
WORKDIR /usr/share/nginx/html

# Copier le contenu du répertoire 'app/front' dans le conteneur à /usr/share/nginx/html
COPY ./ /usr/share/nginx/html

# Définir la variable d'environnement pour l'URL du back-end
ENV WS_BACK_URL=http://backend:5000

# Utiliser un entrypoint pour définir la variable d'environnement et démarrer nginx
ENTRYPOINT ["sh", "-c", "envsubst '$$WS_BACK_URL' < /usr/share/nginx/html/index.html > /usr/share/nginx/html/index.html && exec nginx -g 'daemon off;'"]
