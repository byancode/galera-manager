# Galera Manager

This repository demonstrates, how we can run gmd in Docker.

## How to use

1. Install
  ```bash
   mkdir -p $(echo $HOME)/gmd && cd $(echo $HOME)/gmd
   curl -sSL https://raw.githubusercontent.com/byancode/galera-manager/master/docker-compose.yml > docker-compose.yml
  ```

1. Run:

   ```bash
   docker compose up -d
   ```

1. Try accessing [http://localhost:8080/app](http://localhost:8080/app) in your browser.

1. Stop:

   ```bash
   docker compose down
   ```

1. Remove persistent data:

   ```bash
   rm -rf $(echo $HOME)/gmd/configs
   rm -rf $(echo $HOME)/gmd/logs
   ```
