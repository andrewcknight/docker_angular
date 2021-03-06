# Angular & Docker

## Create Angular Application
1. Create project folder
2. Navigate to the folder
3. Run to install Angular CLI: npm install -g @angular/cli
4. Run to create project: ng new project-name --directory ./ (directory piece if you want flat creation)
5. To run application: ng serve

## Add Angular Material
1. Navigate to project folder
2. Run: ng add @angular/material
3. For additional options: https://material.angular.io/guide/getting-started#install-angular-material
4. To run application: ng serve

## Commit to GIT repository
1. git init
2. git add *
3. git commit -m "first commit"
4. git remote add origin URL_GOES_HERE
5. git push -u origin master

## Create Angular Docker Image
1. Create Dockerfile - use name "Dockerfile" or your own custom name
    See example Dockerfile to understand how the nginx dependency is pulled in
2. Create a .dockerignore file (similar to .gitignore) to define which files and folders we want Docker to ignore.
3. Run docker build: `docker build -t andrewcknight/angular-docker-test .` (don't forget the period!)
4. Verify image creation by running: `docker image ls`
5. Run docker image: `docker run --name angular-docker-test-app-container -d -p 8080:80 andrewcknight/angular-docker-test`
6. Confirm the container is running at: http://localhost:8080

To learn more: https://medium.com/@wkrzywiec/build-and-run-angular-application-in-a-docker-container-b65dbbc50be8

## Commit Docker Image to Repository
1. Confirm that you have run your docker build before pushing your image to the remote repository.
2. To push your image to your repository run: `docker push andrewcknight/angular-docker-test`
    (you will need to login to Docker first)
3. Find the example repsoitory here: https://hub.docker.com/repository/docker/andrewcknight/angular-docker-test


# More with Angular

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.23.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
