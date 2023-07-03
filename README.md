# Wordpress Template

This project template allows you to quickly initialize a Wordpress project using Docker compose.

## Prerequisites

- Git
- Docker compose
- Visual Studio Code has [XDebug extension](https://marketplace.visualstudio.com/items?itemName=xdebug.php-debug) installed.

## Usage

This project will use 3 docker containers including:

- Nginx (image: nginx:alpine, expose port: 8000)
- Wordpress (image: wordpress:php8.2-fpm)
- Maria database (image: mariadb:10.6.4-focal, expose port: 3306)


To initialize the containers, you need to first clone the project source code to the ` <project-name>` directory with the command:

```sh
git clone https://github.com/ngoc24794/wordpress-template.git <project-name>
cd <project-name>
```


In the `<project-name>` directory, change `xdebug.client_host` in `Wordpress\xdebug.ini` to your machine's IP address. Then run the command:

```sh
docker-compose up -d
```

> Note: The `docker-compose` command may be different depending on how you installed docker compose. You can try the `docker compose up -d` command. 

Verify the containers are running with the command:

```sh
docker ps
```

If successful then you will see 3 containers running. Open a browser and go to the address: `http://<host-ip>:8000` you will see Wordpress running.

You can change the value of environment variables in `docker-compose.yml` file.

## Debug

To debug the application, you open the `<project-name>` folder with Visual Studio Code. Set a break point and press the F5 key to launch `Listen for XDebug`. Refresh the browser and you will see Visual Studio Code stop the break point.

## License

MIT

**Free Software, Hell Yeah!**

