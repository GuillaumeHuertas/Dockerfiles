# Image de base
FROM debian:latest

# Mise-à-jour et installation des derniers paquets
RUN apt-get update \
&& apt-get -y upgrade

# Installation de wget
RUN apt-get install -y wget unzip

# Change le mot de passe du Super Utilisateur 
RUN echo "root:root" | chpasswd

# Créé l'utilisateur vault
RUN useradd -ms /bin/bash  vault

# Se connecte à l'utilisateur vault
USER vault
# Repertoire de connection
WORKDIR /home/vault

# Télécharge l'archive, dézipe et se déplace dedans
RUN wget https://github.com/GuillaumeHuertas/JINTM/archive/master.zip \
&& unzip master.zip \
&& rm -rf master.zip

# Se déplace dans le répertoire JINTM
WORKDIR /home/vault/JINTM-master




