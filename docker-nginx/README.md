# ContainerITW - MyAlienCorps - 2020

Guide de démarrage rapide:

# Vous devrez peut-être installer git: en cas d'erreur "commande non trouvée"
apt-get install -y git

1: Copiez, clonez ces fichiers où vous voulez qu'ils soient.
git clone https://github.com/MyAlien/ContainerITW/docker-nginx.git

2: Modifiez les fichiers pour qu'ils correspondent à votre domaine / environnement cible décommentez les paramètres ssl si nécessaire.
3: démarrer le conteneur
docker run -d --name nginx --restart unless-stopped -v /target/path/nginx:/etc/nginx/ -p 80:80 -p 443:443 nginx

4: vérifier les journaux: aucune sortie signifie que tout semble bien.
docker logs -f nginx

5: Pour recharger la conf sans avoir à redémarrer le conteneur:
docker exec -it nginx /etc/init.d/nginx reload