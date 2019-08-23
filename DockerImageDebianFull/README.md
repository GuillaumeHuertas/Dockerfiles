# Ce Dockerfile à pour but de tester les script de génération de code du projet : 
# https://github.com/GuillaumeHuertas/JINTM.git

Debian:latest
Il met-à-jour les pâquets et installe : 
  - git
  - open-jdk-8
  - maven
  - curl
  - node.js
  - npm latest
  - anglar/cli
 
Change le password root en "root".
Créé un utilisateur "vault" et se connecte avec celui-ci et se déplace dans son home.
Clone le dépôt https://github.com/GuillaumeHuertas/JINTM.git et le met-à-jour.

