# exercice_Traefik
Mise en place d'un conteneur Reverse-proxy "Traefik" et 2 conteneurs Whoami

# Guide d'installation

![docker.png](https://doc.traefik.io/traefik/assets/images/logo-traefik-proxy-logo.svg)




## Pré-requis windows
- Docker desktop
- Distribution linux (WSL2)
- Visual studio code (confort)
- Documentation officielle Traefik : https://doc.traefik.io/traefik/
 
Possibilité de rester dans la console de votre Wsl ou d'utiliser visual studio code en saississant la command ```code .``` 

## Création d'un dossier (os: Debian WSL2)

```bash
mkdir traefik
cd traefik
```

## Récuperation du fichier de config des conteneurs

```bash
git pull https://github.com/Djez-Himself/exercice_Traefik.git
```
## Edition des fichiers selon vos préférences : docker-compose.yml, traefik.yml et config.yml

### Modification sur docker-compose.yml
- network 
- container_name
- ports : "8181:8080" ex : 8888:8080 etc
- volumes

### Modification sur traefik.yml
- network #garder le même que sur votre docker-compose.yml
- filename #suivant le chemin utilisé

### Modification sur config.yml
- rule: "Host(`traefik.localhost`)"
- users: - ```"ben:$apr1$yN5SkU9i$/.72ViNpEiXNikGnMFNBV0"``` #dans cet exemple htpasswd -nb <ben> <123456>

```bash
sudo apt-get install apache2-utils
```
```bash
htpasswd -nb <user> <password>
```



## Création des conteneurs

```bash
docker compose up -d 
#tips : l'option "-d" permet de lancer les conteneurs en mode détachés.
```
## Afficher les conteneurs
```bash
docker ps
```

## Accés au portail Traefik et url serveur whoami.
### dashboad Traefik

```url
http://localhost:8181
```

```url
http://traefik.localhost
```
### Serveur Whoami
```url
http://first.localhost
```
```url
http://second.localhost
```

## Ajouts possible
- config https avec certificats TLS (ajout port 443)
- possibilité de modifier le fichier config.yml pour l'ajout de différents services ou middleware.
