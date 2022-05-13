# MEVN Example project

[![License: MIT](https://img.shields.io/badge/License-MIT-red.svg)](https://opensource.org/licenses/MIT)
![Last commit](https://img.shields.io/github/last-commit/argoitz/MEVN-example-project)

# Pre-requisites

- Install [Docker compose](https://docs.docker.com/compose/install/)

# Getting started

- Clone the repository

```
git clone  https://github.com/argoitz/MEVN-example-project
```

- Go inside path

```
cd MEVN-example-project
```

- Create .env file in the backend and make the appropriate modifications

```
cp backend/.env.example backend/.env
```

- Go to backend path and install the dependencies

```
cd backend
npm install
```

- Go to client path and install the dependencies

```
cd ..
cd client
npm install
```

- Run Docker container (Dont panic, the frontend takes a bit longer to deploy, about 30 seconds longer. Check the MEVN-frontend container in your docker-desktop)

```
docker-compose up -d
```

Then you can access the website from:

    http://localhost:8080

Connect to docker container backend or client

```
winpty docker exec -it MEVN-Backend bash
winpty docker exec -it MEVN-Frontend bash
```

# Command list

```
git clone  https://github.com/argoitz/MEVN-example-project
cd MEVN-simple-project
cp backend/.env.example backend/.env
cd backend
npm install
cd ..
cd client
npm install
docker-compose up -d
```

# Importing API Collection in Postman

You can check the endpoints by importing this collection to your postman:
https://www.getpostman.com/collections/8de6385fec5d043a2687

## Author

- [Argoitz Estebanez](https://github.com/argoitz)
