
  

# Docker ou Machine virtuelle ?

  

![](dockerVS.png)

  

  

## Commande Basique

  

lister les containers :

> **docker**  **ps**

  

Créer un container

```
docker pull $name:$version 
```

Lancer un container
```
docker run $name
```

Malgré le docker run , on n'appercevra pas le container il faudrait éxécuter un
```
docker ps -a
```
>**-a** : ALL

Pour lister **TOUT** les containers même ceux qui ont le status exit

Lorsque l'on run le container il se exécute sa tâche et s'éteint automatiquement

Pour pallier à cela, pour garder la main sur le container
```
docker run -di $name:$version
```
 
>**-d** : dettach

>**-i** : interactive

>**--name**:  préciser le nom du container

Avec cette method, le container se lancera et restera actif on peu le voir en listant les containers ou en listant tous les containers


Se connecter à un container

```
docker exec -ti $name sh
```
>**-t**: TTY

>**sh**: se connecter avec un shell