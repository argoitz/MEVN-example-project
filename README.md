# MEVN Example project

[![License: MIT](https://img.shields.io/badge/License-MIT-red.svg)](https://opensource.org/licenses/MIT)
![Last commit](https://img.shields.io/github/last-commit/argoitz/MEVN-example-project)
![badmath](https://img.shields.io/badge/Docker%20compose-2.5.0-blue.svg)
![badmath](https://img.shields.io/badge/Docker-20.10.14-blue.svg)

## Description

This is a dockerized MEVN project. This project depends on these two repositories:

- https://github.com/argoitz/bitgune-backend-test
- https://github.com/argoitz/bitgune-front-test

# Pre-requisites

- Install [Docker compose](https://docs.docker.com/compose/install/)
- To clone this project you need to use the --recurse-submodules flag before repository url.

# Getting started

- Clone the repository with submodules

```
git clone --recurse-submodules https://github.com/argoitz/MEVN-example-project.git
```

- Go inside path

```
cd MEVN-example-project
```

- Optional!

```
    !If you want to use your cloud DB you need to make this modifications:
    - Create .env file in the backend and make the appropriate modifications if you want to use cloud DB

        cp backend/.env.example backend/.env

    Go to back/database.js and replace localUri with uri variable in line 11

        .connect(uri, { useNewUrlParser: true, useUnifiedTopology: true })
```

- Go to back path and install the dependencies

```
cd back
npm install
```

- Go to front path and install the dependencies

```
cd ..
cd front
npm install
```

- Return back

```
cd ..
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
cd backend
npm install
cd ..
cd client
npm install
docker-compose up -d
```

# Usage

You can check the usage of both environments inside back/README.md and front/README.md

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Copyright (c) 2022 Argoitz Estebanez Barrado

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Author

- [Argoitz Estebanez](https://github.com/argoitz)
