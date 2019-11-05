# Docker Volume avec ```-v```
le volume est une sorte de partage entre la machine qui heberge docker et le/les containers

```
docker run --rm -it -v $(PWD):/workdir/ debian:jessie-slim /bin/bash
```
>**-v**: volume

Cette command permet de partager le directory local avec le directory dans le container

Dans le cas du server nginx

```
docker run -tid -p 8080:80 -v $(PWD):/usr/share/nginix/html/ --name web nginx:latest
```

# Docker Volume avec ```docker volume``` (volume persistant)

```
docker volume create
```

```
docker volume inpect
```

```
docker volume ls
```

```
docker volume prune
```
>Remove all unused local volumes

```
docker volume rm
```

créer un container nginx et le monter avec un docker volume
```
docker run -tid --name web -p 8080:80 --mount source=$(nameDVolume),target=$(dirInContainer) nginx:latest
```
>**--mount** : pour monter le volume , prends 2 options , **source** : pour specifier le volume persistant créer avant avec la commande ```docker volume create``` et prends aussi comme option **target** : pour specifier le directory cible