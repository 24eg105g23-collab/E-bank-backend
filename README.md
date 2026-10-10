# E-Bank Update Backend

This repository contains the application's server-side code:

- `backend/` — Spring Boot REST API (Java 21, port 8080)
- `server/` — Express API (Node.js, port 5000), used by the Vite `/api` and `/uploads` proxy

## Requirements

- Java 21 and Maven
- MySQL 8
- Node.js and npm (for the Express API)

## Run the Spring Boot API

Create the `ebank_update` database in MySQL, then check the local connection settings in `backend/src/main/resources/application.properties`.

From this repository's root:

```bash
mvn -f backend/pom.xml spring-boot:run
```

The API starts at `http://localhost:8080`.

## Run the Express API

From this repository's root:

```bash
npm ci --prefix server
npm start --prefix server
```

The Express API starts at `http://localhost:5000`. Local uploads and data files are excluded from Git.
