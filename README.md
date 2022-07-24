# exercice_Traefik
Mise en place d'un conteneur Reverse-proxy "Traefik" et 2 conteneurs Whoami
#Guide d'installation

## Pré-requis windows
- Docker desktop
- Distribution linux (WSL2)
- Visual studio code (confort)
 
Possibilité de rester dans la console de votre Wsl ou d'utiliser visual studio code en saississant la command ```code .``` 

### Création d'un dossier (os: Debian WSL2)

```bash
mkdir traefik
cd traefik
```

### Récuperation du fichier de config des conteneurs

```bash
git pull https://github.com/Djez-Himself/exercice_Traefik.git
```

### Création des conteneurs

```bash
docker compose up -d 
#tips : la command -d permet de lancer les conteneurs en mode détachés.
```
### Afficher les conteneurs
```bash
docker ps
```

### Accés au portail Traefik et url serveur whoami.

```url
http://localhost:8181
```

```url
http://first.localhost
```

```url
http://second.localhost
```


