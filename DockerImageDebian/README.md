# Ce Dockerfile à pour but de tester les script d'installation de programmes : 
# https://github.com/GuillaumeHuertas/JINTM.git

Debian:latest
Il met-à-jour les pâquets et installe : 
  - git
 
Change le password root en "root".
Créé un utilisateur "vault" et se connecte avec celui-ci et se déplace dans son home.
Clone le dépôt https://github.com/GuillaumeHuertas/JINTM.git et le met-à-jour.