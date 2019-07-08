# Image de base
FROM debian:latest

# Personne qui a rédigé le Dockerfile
MAINTAINER Guillaume Huertas <guillaumehuertas@free.fr>

# Mise-à-jour et installation des derniers paquets
RUN apt-get update \
&& apt-get -y upgrade \
&& apt-get install -y git

# Change le mot de passe du Super Utilisateur 
RUN echo "root:root" | chpasswd

# Créé l'utilisateur vault
RUN useradd -ms /bin/bash  vault

# Se connecte à l'utilisateur vault
USER vault
# Repertoire de connection
WORKDIR /home/vault

# Télécharge l'archive, dézipe et se déplace dedans
RUN git clone https://github.com/GuillaumeHuertas/JINTM.git 

# Télécharge le fichier à l'adresse indiqué
# ADD https://github.com/GuillaumeHuertas/JINTM/archive/master.zip /home/vault

# Se déplace dans le répertoire JINTM
WORKDIR /home/vault/JINTM

# Se lance au lancement de l'image
ENTRYPOINT git pull && /bin/bash

WORKDIR /home/vault/JINTM/Guillaume




