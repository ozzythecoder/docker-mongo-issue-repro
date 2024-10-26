# Reproduction of Payload issue

This is a repro of an issue with Payload 3.0's "website" template. When selecting postgres in the CLI tool, the generated [docker compose file](docker-compose.yaml) lists Mongo and not Postgres as a dependency. Running `docker compose up` right away starts a crashing instance.

To reproduce:
- Run `npm create-payload-app@beta`
- Select "website" template
- Select "Postgres" database
- Run `docker compose up`
