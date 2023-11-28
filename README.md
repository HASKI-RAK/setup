# HASKI Setup
This Repository provides the needed files for setting up the HASKI System on a server.
[Docker](https://www.docker.com/) and [Traefik](https://traefik.io/) are used for the setup.

Moreover, this Setup Repository uses the following Repositories/Docker Images:
- [HASKI Backend](https://github.com/HASKI-RAK/HASKI-Backend)
- [HASKI Frontend](https://github.com/HASKI-RAK/HASKI-Frontend)
- [Yet Analytics LRSQL](https://github.com/yetanalytics/lrsql/)
- [Postgres](https://hub.docker.com/_/postgres/)
- [PGAdmin4](https://hub.docker.com/r/dpage/pgadmin4/)
- [Bitnami Moodle](https://hub.docker.com/r/bitnami/moodle/#!)

Additionally, we recommend to use the following extensions for your Moodle:
- [HASKI Theme](https://github.com/HASKI-RAK/theme_haskiminimal)
- [HASKI xAPI Logstore Extension](https://github.com/HASKI-RAK/Moodle-xAPI-Plugin)


For setting up the project, please follow the steps outlined in the [Wiki](https://github.com/HASKI-RAK/setup/wiki).
Please remember to change any sensible data in the docker compose files to your needs!

After following all steps, you can access the different services via your webbrowser.
