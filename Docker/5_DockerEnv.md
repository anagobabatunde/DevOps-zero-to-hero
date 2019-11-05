 # Les variables d'environnement

il y a deux manière de mettre des variables d'environnement

La première est de le passer directement lors de la création du container
```
docker run -tid --name $name --env MYVARIABLE="value" $containerName
```
>**--env** : permet de mettre l'argument qui suit dans l'env

Dès lors que l'on aura besoin de mettre plusieur VarEnv il ne serai pas judicieux d'utiliser **--env**

```
docker run -tid --name $name --env-file file $containerName
```

>**--env-file** : permet de mettre de mettre le contenu du fichier qui va suivre dans les VarEnv