# From zero to Jenkins in 5 minutes

This a practical guide with runnable example about how to get a Jenkins
installation using Docker.

## Requirements

1. Docker v>=1.10. [See this installation guide](https://docs.docker.com/engine/installation/linux/ubuntulinux/)
1. Python PIP.

   ```bash
   ~/jenkins$ sudo apt install python-pip
   ```

1. Composer (listed in `requirements.txt`).

   ```bash
   ~/jenkins$ sudo pip install -r requirements.txt
   ```

## Running

Composer has the configuration for volume mounting, port binding and image
management.

```bash
~/jenkins$ docker-compose up
```

**NOTE:** watch carefully the stdout on first start. It will show you data
required to complete configuration. Once all configuration is ready, you can
stop the container with `Ctrl + C` safely and daemonize the container with `-d`
flag.

```bash
~/jenkins$ docker-compose up -d
```

# Default vaules

* Web interface: http://localhost:8080/
* Local path for Jenkins' data storage: `./data`
