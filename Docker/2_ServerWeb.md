# Server Web

Lancer un container nginx
```
docker run -tid -p 8080:80 --name web nginx:latest
````
>**-p**: exposition de port -p (port machine local):(port container)

Inpecter un container
```
docker inpect $nameOfContainer
```

access to html ```/usr/share/nginx/html/index.html```