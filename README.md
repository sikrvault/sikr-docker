# sikr-docker

These are the Dockerfiles and composer instructions for the sikr platform

# Composer

If you want to build the entire platform from scratch with the latest
version, just run:

    docker compose up

If you want other version, modify the docker-compose.yml file at your
convenience.

# Build image
You can build the base sikr-api image from scratch if you need it just by
doing:

    docker build -t <name> .

# License

As always, the project license is Apache 2.0. This applies to the API and
the frontend itself, not the dependencies such as nginx and postgresql.
Please refer to their project pages for more information about their license.
