# Utiliser une image Python de base à partir de Docker Hub
FROM python:3.9-slim  # Adaptez la version de Python si nécessaire

# Définir le répertoire de travail à l'intérieur du conteneur
WORKDIR /app/back

# Copier le code source et le fichier requirements.txt dans le conteneur
COPY . .

# Installer les dépendances Python
RUN pip install -r requirements.txt

# Définir la commande à exécuter lors du démarrage du conteneur
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]
