# HASKI Setup
This Repository provides the needed files for setting up the HASKI System on a server.
[Docker](https://www.docker.com/) and [Traefik](https://traefik.io/) are used for the setup.
The certificates within Traefik will be created by [Let's Encrypt](https://letsencrypt.org/).
Configuration can be done in `traefik->traefik.yml`.

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

------------------------------------------------------------------------------

# Structure of HASKI Setup

In the following pictures, you can see the structure of the HASKI-System when set up.

A user accesses the system via it's computer over the internet and will reach the server for the request.

The server will use Traefik as reverse proxy and forward the request to the right part of the system.

All parts - including Traefik - that are pictured within the server, are running as Docker Container.

![struktur2](https://github.com/HASKI-RAK/setup/assets/49634213/1d7cf82b-1add-4046-b1b7-345abb979771)


For clearifying the internal working of the system, the following picture will describe the communication within HASKI.

The user will access the Frontend of the application, which will get information from both, the Backend and Moodle.

These in turn are communicating with their dedicated database.

For Moodle it is a MariaDB and for the Backend it is a PostgreSQL.

While working on the system, the Frontend (and Moodle if configured) are sending xAPI-Statements to the LRS, which stores this data in a seperate PostgreSQL database.

![Struktur](https://github.com/HASKI-RAK/setup/assets/49634213/bffea1c2-3685-473d-b701-19d79e570026)
