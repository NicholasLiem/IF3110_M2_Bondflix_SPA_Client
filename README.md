# Tugas Besar 2 - Pengembangan Aplikasi Berbasis Web

<img src='./asset/logo.png'>

## **Deksripsi Web App - Web App Description**

## **Daftar Kebutuhan - Requirements List**

## **Cara Menginstall dan Menjalankan Program - How to Install and Run The Program**

1. Clone this repository

```sh
git clone https://github.com/haziqam/bondflix-spa-service.git
```

2. Change the current directory to `bondflix-spa-service` folder

```sh
cd bondflix-spa-service
```

### FOR DEVELOPMENT:

3. [Recommended] Install dependencies locally. The code will still run normally even if you don't install the dependencies locally, since it will be installed inside the docker container. Installing dependencies locally will ensure intellisense and importing work properly in your IDE.

```sh
yarn
```

4. Change the ENVIRONMENT variable to `dev` in the .env file. You can do so by commenting out the first line in the .env file and un-commenting the second line in the .env file.

```env
# ENVIRONMENT=prod
ENVIRONMENT=dev
```

5. Build docker image. After build finished, you will be able to access the web on localhost:5173. To stop the app, press CTRL+C.

```sh
docker compose up --build
```

6. To run the image without rebuilding the docker image,use this command. If you made changes to the dependencies, the Dockerfile, or the docker-compose.yml file, you should rebuild the container. But if you just made changes to the code, you don't need to rebuild it.

```sh
docker compose up
```

### FOR PRODUCTION:

3. Change the ENVIRONMENT variable to `prod` in the .env file. You can do so by commenting out the second line in the .env file and un-commenting the first line in the .env file

```env
ENVIRONMENT=prod
# ENVIRONMENT=dev
```

4. Build the docker image. After build finished, you will be able to access the web on localhost:4173. To stop the app, press CTRL+C

```sh
docker compose up --build
```

5. To run the image without rebuilding the docker image,use this command.

```sh
docker compose up
```

## Project Structure

```
│   .env
│   .gitignore
│   docker-compose.yml
│   README.md
│   yarn.lock
│
├───asset
│       logo.png
│
├───bondflix-spa-service
│   │   .eslintrc.cjs
│   │   .gitignore
│   │   index.html
│   │   package.json
│   │   README.md
│   │   tsconfig.json
│   │   tsconfig.node.json
│   │   vite.config.ts
│   │   yarn-error.log
│   │   yarn.lock
│   │
│   ├───dist
│   │   │   index.html
│   │   │   vite.svg
│   │   │
│   │   └───assets
│   │           index-c7e05d32.js
│   │           index-d526a0c5.css
│   │           react-35ef61ed.svg
│   │
│   ├───node_modules
│   ├───public
│   │       vite.svg
│   │
│   └───src
│       │   App.css
│       │   App.tsx
│       │   index.css
│       │   main.tsx
│       │   vite-env.d.ts
│       │
│       ├───assets
│       │       react.svg
│       │
│       ├───common
│       │       test.ts
│       │
│       ├───pages
│       │   ├───Login
│       │   │       Login.components.tsx
│       │   │       Login.tsx
│       │   │
│       │   └───Register
│       └───shared-components
└───dockerfile
        Dockerfile.dev
        Dockerfile.prod
```
