# MySQL and phpMyAdmin with Docker Compose

This repository contains a Docker Compose configuration to set up MySQL and phpMyAdmin containers. It allows you to easily manage your MySQL database using phpMyAdmin.

## Prerequisites

- Docker: Make sure you have Docker installed on your system. You can download and install Docker from [here](https://www.docker.com/get-started).

## Usage

1. Clone this repository to your local machine.

    ```bash
    git clone https://github.com/ckmusngi/mysql-phpmyadmin-docker.git
    ```

2. Navigate into the cloned directory.

    ```bash
    cd mysql-phpmyadmin-docker
    ```

3. Modify the `.env` file to customize MySQL root password, database name, username, and password. Replace `MYSQL_ROOT_PASSWORD`, `MYSQL_DATABASE`, `MYSQL_USER`, and `MYSQL_PASSWORD` with your desired credentials.

4. Execute the following command to start the containers.

    ```bash
    docker compose up -d
    ```

    This command will start both MySQL and phpMyAdmin containers in detached mode, meaning they will run in the background.

5. Access phpMyAdmin in your web browser by navigating to `http://localhost:8080`. You can log in using the MySQL root credentials you provided.

6. After you're done, you can stop and remove the containers by executing:

    ```bash
    docker compose down
    ```

    This will stop and remove both containers.

## Customization

- You can customize the MySQL root password, database name, username, password and ports by modifying the environment variables in the `.env` file.

## Important Notes

- The MySQL data volume is mounted at `./db-data` on the host machine. This ensures that MySQL data is persisted even if the container is stopped or removed.

- Ensure that the necessary ports (3306 for MySQL and 8080 for phpMyAdmin) are not being used by other applications on your system before running the containers.