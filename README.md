# exercice_Traefik
Mise en place d'un conteneur Reverse-proxy "Traefik" et 2 conteneurs Whoami

# Guide d'installation

![docker.png](https://doc.traefik.io/traefik/assets/img/providers/docker.png)




## Pré-requis windows
- Docker desktop
- Distribution linux (WSL2)
- Visual studio code (confort)
- Documentation officielle Traefik : https://doc.traefik.io/traefik/
 
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
#tips : l'option "-d" permet de lancer les conteneurs en mode détachés.
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

### Ajouts possible
- config https avec certificats TLS (ajout port 443)
- possibilité d'ajouter un fichier de config .yml ou .toml au lieu de saisir directement les commandes dans le docker compose.
