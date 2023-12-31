# Tugas Besar 2 - Pengembangan Aplikasi Berbasis Web

<img src='./asset/logo.png'>

## **Deksripsi Web App - Web App Description**

Bondflix SPA Service adalah sebuah layanan SPA pada aplikasi web yang menjadikan satu halaman HTML dapat memuat semua sumber daya (HTML, CSS, dan JavaScript) yang diperlukan.

## **Daftar Kebutuhan - Requirements List**

1. Login Page dan Register Page
2. User Dashboard
3. Creator Dashboard
4. Administrator Dashboard
5. Error Page

## **Pembagian Tugas**

**Anggota Kelompok**

| Nama                   | NIM      | Panggilan |
| ---------------------- | -------- | --------- |
| Cetta Reswara Parahita | 13521133 | Cetta     |
| Nicholas Liem          | 13521135 | Nicholas  |
| Haziq Abiyyu Mahdy     | 13521170 | Haziq     |

| NIM                | Nama                   | Page Requirement                                             |
| ------------------ | ---------------------- | ------------------------------------------------------------ |
| 13521133           | Cetta                  | Error Page dan Admin Dasboard                                |
| 13521170, 13521135 | Haziq, Nicholas (Pair) | Login Page, Register Page, User Dashboard, Creator Dashboard |

## **Cara Menginstall dan Menjalankan Program - How to Install and Run The Program**

1. Clone this repository

```sh
git clone https://github.com/haziqam/bondflix-spa-service.git
```

2. Change the current directory to `bondflix-spa-service` folder

```sh
cd bondflix-spa-service/bondflix-spa-service
```

3. Make a new .env file based on .env.example (you can just remove .example from the file's name)

```sh
mv .env.example .env
```

### FOR DEVELOPMENT:

4. [Recommended] Install dependencies locally. The code will still run normally even if you don't install the dependencies locally, since they will be installed inside the docker container. Installing dependencies locally will ensure intellisense and importing work properly in your IDE.

```sh
yarn
```

5. Change the `ENVIRONMENT` variable to `dev` in the .env file. You can do so by commenting out the first line in the .env file and un-commenting the second line in the .env file.

```env
# ENVIRONMENT=prod
ENVIRONMENT=dev
```

6. Build docker image. After build finished, you will be able to access the web on localhost:5173. To stop the app, press CTRL+C.

```sh
docker compose up --build
```

7. To run the image without rebuilding the docker image,use this command. If you made changes to the dependencies, the Dockerfile, or the docker-compose.yml file, you should rebuild the container. But if you just made changes to the code, you don't need to rebuild it.

```sh
docker compose up
```

### FOR PRODUCTION:

4. Change the `ENVIRONMENT` variable to `prod` in the .env file. You can do so by commenting out the second line in the .env file and un-commenting the first line in the .env file

```env
ENVIRONMENT=prod
# ENVIRONMENT=dev
```

5. Build the docker image. After build finished, you will be able to access the web on localhost:4173. To stop the app, press CTRL+C

```sh
docker compose up --build
```

6. To run the image without rebuilding the docker image,use this command.

```sh
docker compose up
```

## Project Structure

[TODO: renew, add description]

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

## Link gambar:

https://drive.google.com/drive/folders/1nmaHUshMrZbp0c5iefb32JPjZ-T8J-ZA?usp=sharing
