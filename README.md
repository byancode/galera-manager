# Galera Manager

This repository demonstrates, how we can run gmd in Docker.

## How to use

1. Run:

   ```bash
   docker run -d \
      -e ADMIN_USER=admin \
      -e ADMIN_PASSWORD=12345 \
      -v $(echo $HOME)/gmd/configs:/var/lib/gmd:rw \
      -v $(echo $HOME)/gmd/logs:/var/log/gmd:rw \
      -p 8080:8080 \
      --name gmd \
      byancode/galera-manager
   ```

1. Try accessing [http://localhost:8080/app](http://localhost:8080/app) in your browser.

1. Stop:

   ```bash
   docker stop gmd
   ```

1. Remove persistent data:

   ```bash
   rm -rf $(echo $HOME)/gmd/configs
   rm -rf $(echo $HOME)/gmd/logs
   ```
