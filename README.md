# Pihole Docker Setup

This is a simple setup for running [Pihole](https://github.com/pi-hole/pi-hole) through a [Docker](https://www.docker.com/) container.

Dependencies to install before trying to run this:
- [Docker](https://docs.docker.com/engine/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## How to run things

First create a `.env`:
1. Duplicate `.env.example` and rename that file to `.env`
2. Replace the dummy password in `.env` with a secure password of your choice
3. If applicable, replace the timezone (TZ) variable with [your timezone](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)

Next, run the following in the same directory as `docker-compose.yml` to start up Pihole.

```bash
docker compose up -d
```

Finally, if you ever need to shut down Pihole, run the following in the same directory as `docker-compose.yml`:

```bash
docker compose down
```

## Updating Pihole

1. Download the latest version of the image: `docker pull pihole/pihole`
2. Shut down Pihole: `docker compose down`
3. Throw away the old Pihole container: `docker rm -f pihole`
4. Start up Pihole: `docker compose up -d`
