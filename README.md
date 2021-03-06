# Dockerfiles 🐳

Dockerfiles that ships with dependencies for running Vapor projects (including [CStack](https://github.com/nodes-vapor/cstack)) on Linux. These images are used in [our Circle CI scripts](https://github.com/nodes-vapor/readme/tree/master/Configuration/.circleci).

Currently we have the following images:

- `Dockerfile-Swift3` which is using Swift 3 and is supposed to be used for Vapor 1 projects. The image is pushed to [here](https://hub.docker.com/r/brettrtoomey/vapor1-ci/).
- `Dockerfile-Swift4` which is using Swift 4 and is supposed to be used for Vapor 2 projects. The image is pushed to [here](https://hub.docker.com/r/brettrtoomey/vapor-ci/)
- `Dockerfile-Swift4.1` which is using Swift 4.1 and is supposed to be used for Vapor 2 or 3 projects. The image is pushed to [here](https://hub.docker.com/r/nodesvapor/vapor-ci) with tag "swift-4.1".
- `Dockerfile-Swift4.2` which is using Swift 4.2 (release) and is supposed to be used for Vapor 2 or 3 projects. The image is pushed to [here](https://hub.docker.com/r/nodesvapor/vapor-ci) with tag "swift-4.2".
- `Dockerfile-Swift5` which is using Swift 5.0 and is supposed to be used for Vapor 3 or 4 projects. The image is pushed to [here](https://hub.docker.com/r/nodesvapor/vapor-ci) with tag "swift-5.0".

## 🛠 Updating the Docker images

A guide for building new images based on Dockerfiles can be found [here](https://circleci.com/docs/2.0/custom-images/).

## ☁️ Hosting

To make it easier to run a Vapor app through a Docker container, we have the following Dockerfiles for guidance:

- `Hosting/Dockerfile-Swift4.1` which is using Swift 4.1 and is supposed to be used for Vapor 2 or Vapor 3 projects.
- `Hosting/Dockerfile-Swift4.2` which is using Swift 4.2 and is supposed to be used for Vapor 2 or Vapor 3 projects.
- `Hosting/Dockerfile-Swift5.0` which is using Swift 5.0 and is supposed to be used for Vapor 3 or Vapor 4 projects.

Further, we have the following Docker Compose files for spinning up full environments including database and Redis:

- `Hosting/docker-compose-mysql.yml` which is using MySQL 5.7 and the latest version of Redis.

## 👌 Testing

To make it easier to test Vapor apps locally on Linux using Docker, we have made the following Dockerfiles:

- `Testing/Dockerfile-Swift4.1` which is using Swift 4.1 and is supposed to be used for Vapor 2 or Vapor 3 projects.
- `Testing/Dockerfile-Swift4.2` which is using Swift 4.1 and is supposed to be used for Vapor 2 or Vapor 3 projects.

## 🌳 Environment variables

Environment variables are supported in Docker. Please read the [docs regarding environment variables](https://docs.docker.com/compose/environment-variables/) for info regarding how to configure them.

In short composer prioritizes environment variables in the following order:

 1. Compose file
 2. Shell environment variables
 3. Environment file
 4. Dockerfile
 5. Variable is not defined

If you want to use a `.env`-file, make sure to remove the environment section in your docker-compose file as described in the docs, referenced above.

## 🏆 Credits

This package is developed and maintained by the Vapor team at [Nodes](https://www.nodesagency.com).
The package owner for this project is [Steffen](https://github.com/steffendsommer).

## 📄 License

This package is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
