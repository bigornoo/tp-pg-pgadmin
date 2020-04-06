# PosgreSQL and PostgreSQL admin in a docker-compose file + 2 kubernetes manifests.
It's an exercice to learn howto transform compose file to kubernetes manifests. It's for my personal use but it can be used by anyone who wants to learn both :)
## Docker :
2 services and 2 persistents volumes  
`$ docker-compose up -d`
## Kubernetes (in Docker for Desktop)
2 manifests: 
- one for the pod with 2 containers 
    - one for PostgreSQL
    - one for PG admin
- one for declare the service
```
$ kubectl apply -f pg-app.yml
$ kubectl apply -f pg-service.yml
```