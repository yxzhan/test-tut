# binder-template

[![Binder](https://binder.intel4coro.de/badge_logo.svg)](https://binder.intel4coro.de/v2/gh/IntEL4CoRo/binder-template.git/main)

This is a template repo for running robotics research Jupyter Notebooks on Binderhub.

Step-by step tutorials can be found here: https://vib.ai.uni-bremen.de/page/softwaretools/cloud-based-infrastructure#step-by-step-tutorial

## Development

### Run and build docker image Locally (Under repo directory)

- To make the current directory writable inside the jupyterlab:

  ```bash
  chmod -R g+w ./
  ```

- Build and run docker image:

  ```bash
  export GID=$(id -g) && \
  docker compose -f ./binder/docker-compose.yml up --build
  ```

- Open Web browser and go to http://localhost:8888/

- To stop and remove container:

  ```bash
  docker compose -f ./binder/docker-compose.yml down
  ```
