# Utilisez une image Python existante en tant que base
FROM python:3.9

# Définissez le répertoire de travail dans le conteneur
WORKDIR /app

# Copiez le fichier requirements.txt dans le conteneur
COPY ./back/requirements.txt .

# Installez les dépendances Python
RUN pip install --no-cache-dir -r requirements.txt

# Copiez le contenu du répertoire back dans le conteneur
COPY ./back .

# Définissez la commande par défaut à exécuter lorsque le conteneur démarre
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]
