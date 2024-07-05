# QRThrough: Database & MQTT Broker Container

This repository contains the docker-compose files for the QRThrough project. The project is divided into two main components: the database and the MQTT broker. The database is a Postgres database that stores the data of the QRThrough project. The MQTT broker is a Mosquitto broker that is used to communicate device with MQTT protocol.

## Database

The database is a Postgres database that stores the data of the QRThrough project. The database is used to store the data of the QRThrough project. The database is created using the `docker-compose.yml` file in the `QRThrough_DB` directory.

Before running up the database, you need to configure the environment variables in the `docker-compose.yml` file. The environment variables are used to configure the database connection. The following environment variables are available:

- Postgres service:
  - `POSTGRES_USER`: The username of the database.
  - `POSTGRES_PASSWORD`: The password of the database.
- PGAdmin service:
  - `PGADMIN_DEFAULT_PASSWORD`: The password of the PGAdmin user.

To run up the database, you can use the following command:

```bash
cd QRThrough_DB
docker-compose up -d
```

To stop the database, you can use the following command:

```bash
cd QRThrough_DB
docker-compose down
```

## MQTT Broker

The MQTT broker is a Mosquitto broker that is used to communicate device with MQTT protocol. The MQTT broker is created using the `docker-compose.yml` file in the `QRThrough_MQTT` directory.

Before running up the MQTT broker, you need to configure the configuration file in the `mosquitto.conf` file. The configuration file is used to configure the MQTT broker. The following configuration options are available:

- `listener 1883`: The port of the MQTT broker.
- `protocol websockets`: The protocol of the MQTT broker.
- `password_file /mosquitto/config/pwfile`: The password file of the MQTT broker.
- `listener 1883`: The port of the MQTT broker.
- `persistence true`: The persistence of the MQTT broker.
- `persistence_location /mosquitto/data/`: The persistence location of the MQTT broker.
- `log_dest file /mosquitto/log/mosquitto.log`: The log destination of the MQTT broker.

To run up the MQTT broker, you can use the following command:

```bash
cd QRThrough_MQTT
docker-compose up -d
```

To stop the MQTT broker, you can use the following command:

```bash
cd QRThrough_MQTT
docker-compose down
```
