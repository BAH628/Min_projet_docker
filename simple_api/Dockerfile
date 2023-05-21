FROM python:2.7-buster

LABEL maintainer="Maimouna <bmaimouna338@gmail.com>"

# Copiez le code source de l'API dans le conteneur
ADD student_age.py /

# Installez les dépendances nécessaires via pip
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y 
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0

VOLUME ["/data"]

# Exposez le port 5000 pour l'API
EXPOSE 5000

# Démarrez le conteneur en exécutant student_age.py
CMD ["python", "./student_age.py"]
