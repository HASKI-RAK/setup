# HASKI Setup
This Repository provides the needed files for setting up the HASKI System on a server.
[Docker](https://www.docker.com/) and [Traefik](https://traefik.io/) are used for the setup.

Moreover, this Setup Repository uses the following Repositories/Docker Images:
- [HASKI Backend](https://github.com/HASKI-RAK/HASKI-Backend)
- [HASKI Frontend](https://github.com/HASKI-RAK/HASKI-Frontend)
- [Yet Analytics LRSQL](https://github.com/yetanalytics/lrsql/https://github.com/yetanalytics/lrsql/)
- [Postgres](https://hub.docker.com/_/postgres/)
- [PGAdmin4](https://hub.docker.com/r/dpage/pgadmin4/)
- [Bitnami Moodle](https://hub.docker.com/r/bitnami/moodle/#!)


For setting up the project, please follow those steps:
1. Customize the .env file to your needs. This file contains all variables for the complete system, that can be adjusted.
2. (Optional) Move into the HASKI_dev folder, customize the .env files and run the command `docker compose --env-file ../.env up -d`.
3. (Optional) Move into the HASKI_test folder, customize the .env files and run the command `docker compose --env-file ../.env up -d`.
4. Move into the HASKI_prod folder, customize the .env files and run the command `docker compose --env-file ../.env up -d`.
5. Move into the HASKI_traefik folder and run the command `docker compose --env-file ../.env up -d`.

Now, you can access the different services via your webbrowser.
The structure of the set up infrastructure can be seen here:
![Aufbau](https://github.com/HASKI-RAK/setup/assets/49634213/8a3fc02a-f18a-4894-8877-1ed9c0216e37)
