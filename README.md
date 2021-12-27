# docker-react

### Run Frontend
`docker-compose up`

### Test Frontend Docker Container
```
docker-compose up
docker-compose ps
docker exec -it atadatem_frontend_1 npm run test
```

### Build Frontend Docker Container for production
```
cd frontend
docker build .
```

