# NamelessMC Docker

This is the official Docker image for NamelessMC. Deploy with ease!

## Usage

### Install Docker

You have to manually install Docker first if you don't have it installed on your server. Check out the [official install guide](https://docs.docker.com/engine/installation).

### Automated Deployment

You will need to install [Docker Compose](https://docs.docker.com/compose/) for automated deploying.

```bash
sudo apt install docker-compose
```

Download [docker-compose.yml](https://github.com/NamelessMC/Nameless-Docker/raw/master/docker-compose.yml), optionally change some settings, then run `docker-compose up -d`. The default restart policy is `always` so your website will start back up after a reboot.

When the containers are up, visit the website in a browser to start the installer. By default it listens on any interface, port 80.

When the database configuration page shows up, fill in `db` for *database address*. For database username, password and database name, fill `nameless` for all of them, if you used default database credentials.


## Development

If you want to use Docker for developing NamelessMC, please see the [docker compose file in the main repo](https://github.com/NamelessMC/Nameless/blob/v2/docker-compose.yaml).

## Updating
First, follow regular update instructions on the website (uploading files etc). After the upgrade is complete and your website is back up, change the image tag to the new version (e.g. change from `v2-pr7` to `v2-pr8`) to get the newest PHP library versions.

## Available tags
| Tag | NamelessMC version | PHP version | Receives updates\* | Notes
| --- | ------------------ | ----------- | ---------------- | -----
**v2-pr12** | **v2.0.0-pr12** | **8.0** | **Yes** | **Recommended**
v2-pr12-php74 | v2.0.0-pr12 | 7.4 | Yes | For compatibility with legacy modules
dev | v2 development | 8.1 | Yes | Testing only, reinstall frequently.

### Legacy tags

| Tag | NamelessMC version | PHP version | Receives updates\* | Notes
| --- | ------------------ | ----------- | ---------------- | -----
v2-pr7 | v2.0.0-pr7 | 7.4 | Yes |
v2-pr8 | v2.0.0-pr8 | 7.4 | Yes |
v2-pr9 | v2.0.0-pr9 | 7.4 | Yes |
v2-pr9-php8 | v2.0.0-pr9 | 8.0 | Yes | Experimental
v2-pr10 | v2.0.0-pr10 | 8.0 | Yes | Use PHP 7.4 for compatibility
v2-pr10-php74 | v2.0.0-pr10 | 7.4 | Yes |
v2-pr11 | v2.0.0-pr11 | 8.0 | Yes |
v2-pr11-php74 | v2.0.0-pr11 | 7.4 | Yes | For compatibility with legacy modules
dev-php8 | v2 development | 8.0 | No | Use `:dev` instead, it now uses PHP 8

\* Image updates, not NamelessMC updates. Only the latest NamelessMC version is supported.
