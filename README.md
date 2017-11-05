spring-boot-maven-angular-starter ![Build Status](https://travis-ci.org/shekhargulati/spring-boot-maven-angular-starter.svg?branch=master)
-----

This is a multi-module Spring Boot Angular Maven starter app with good defaults.
The frontend Angular app is built using [angular-cli](https://cli.angular.io/). The project packages Angular application code as a [WebJar](https://www.webjars.org/). This project is geared towards building monolithic applications. 

This project provides productive setup for building Spring Boot React applications. The application is divided into two Maven modules:

1. `backend`: This contains Java code of the application.
2. `frontend`: This contains source code for the Angular based frontend.

This project uses following versions:

1. Spring Boot 1.5.8
2. Angular 5.0.0
3. Node v8.9.0
4. Yarn v1.3.2

## Running the full application

You can build the package as a single artifact by running the `./mvnw clean install`.
Next, you can run the application by executing:

```bash
$ java -jar backend/target/ngboot-app.jar
```

The application will be accessible at `http://localhost:8080`.

## Features

This starter comes bundled with the following features:

1. Multi module Maven project: A multi module project to modularize backend and frontend code separately.
2. Maven wrapper: So, you don't need to install Maven on your machine.
3. Checkstyle: Enforce sane coding standard guidelines.
4. ErrorProne: Find errors in your code.
5. Frontend packaged as a WebJar.
6. CORS enabled: A global configuration is added to enable CORS so that frontend can work seamlessly with backend during development.
7. REST API base path: Sets the base REST API path to `/api`. You can configure it by changing `rest.api.base.path` property.
8. Maven release plugin

## Running the backend for development mode

There are multiple ways to run the backend. For development, you can use your favorite IDE and run the
`com.example.app.Application`. As soon as your code compiles, Spring Boot DevTools will reload the code.

You can also run the application using Maven.

```bash
$ cd backend
$  ../mvnw spring-boot:run
```

## Running the frontend for development mode

Make sure to install [yarn on your development machine](https://yarnpkg.com/en/docs/install).

To install all the required binaries for your project, you can run following command.

```
$ cd frontend
$ ../mvnw frontend:install-node-and-yarn frontend:yarn
```

Once the above command finishes, you can start the frontend using the `yarn start` command.

## Hot reloading

Both the frontend and backend support hot reloading.
