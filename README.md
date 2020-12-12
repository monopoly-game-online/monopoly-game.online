# Monopoly

##### Clear project
```bash
docker system prune -a
docker volume prune
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
docker rmi $(docker images -a -q)
```

##### Env project
```bash
docker-compose up -d --build
docker-compose run web python3 manage.py makemigrations
docker-compose run web python3 manage.py migrate
docker-compose run web python3 manage.py test
docker-compose run web python3 manage.py createsuperuser
```
