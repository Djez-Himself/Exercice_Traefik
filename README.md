# exercice_Traefik
Mise en place d'un conteneur Reverse-proxy "Traefik" et 2 conteneurs Whoami
#Guide d'installation

#Pré-requis
- Docker
- Distribution linux

#Création d'un dossier (os: Debian WSL2)

```bash
mkdir traefik
cd traefik
```

#Récuperation du fichier de config des conteneurs

```bash
git pull https://github.com/Djez-Himself/exercice_Traefik.git
```

#Création des conteneurs

```bash
docker compose up -d 
#tips : la command -d permet de lancer les conteneur en mode détaché.
```

#Accés au portail Traefik et url serveur whoami.

```url
http://localhost:8181
```


