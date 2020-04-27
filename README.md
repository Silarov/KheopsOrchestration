# Insecure Install

This branch contains a bash script and associated files for a simple all-in-one installation of an Insecure instance of KHEOPS.

To install:
1. Install Docker
2. Install Docker-Compose
3. Make sure that the current user is in the `docker` group.
4. Run the following command:

```shell
bash <(curl -sL https://raw.githubusercontent.com/OsiriX-Foundation/KheopsOrchestration/insecure-install-v0.9.4/kheopsinstall.sh)
```

This script will create a new directory named `kheops` in which it will download docker-compose configuration files, a keycloak realm configuration, and generate the necessary secrets.

Once installed Keycloak will be available at [http://127.0.0.1:8080](http://127.0.0.1:8080), and KHEOPS will be available at [http://127.0.0.1](http://127.0.0.1).


**notes**
- On MacOS, the default Docker memory limit of 2GB is not sufficient. 4GB is safer. 
- Also on MacOS, Safari does not trust connections to 127.0.0.1, so when loading a study in the OHIF viewer (which is loaded with https), Safari considers refuses the mixed security connection. Chrome respects the standards and considers connections to 127.0.0.1 to be secure so this issue does not occur.
