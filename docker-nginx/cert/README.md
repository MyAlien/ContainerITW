# ContainerITW - MyAlienCorps - 2020

Veuillez mettre votre certificat ici si vous utilisez https au format .pem et contrôler qu'ils sont correctement configurés dans nginx.conf

vous pouvez générer un certificat auto-signé - éditez -days, -keyout et -out pour répondre à vos besoins:
"openssl req -newkey rsa:2048 -nodes -keyout key.pem -x509 -days 365 -out certificate.pem"
