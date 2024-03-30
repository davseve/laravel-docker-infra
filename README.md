This repository contains a Docker setup for running a Laravel application locally using the LEMP stack (Linux, Nginx, MySQL, PHP), along with phpMyAdmin for database management.

## Prerequisites

Before getting started, ensure that you have Docker and Docker Compose installed on your machine.

- [Docker Installation Guide](https://docs.docker.com/get-docker/)
- [Docker Compose Installation Guide](https://docs.docker.com/compose/install/)

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/davseve/laravel-docker-infra.git
2. Navigate to the project directory:

   ```bash
   cd laravel-docker-infra
   ```

3. Copy the `.env.example` file to `.env`:

   ```bash
   cp .env.example .env
   ```

4. Update the `.env` file with your Laravel application configurations, including database credentials:

   ```dotenv
   DB_CONNECTION=mysql
   DB_HOST=db
   DB_PORT=3306
   DB_DATABASE=laravel
   DB_USERNAME=root
   DB_PASSWORD=password
   ```

## Building and Starting Docker Containers

To set up the Docker image, execute the following command:

```bash
docker-compose build
```

To start the Docker containers in detached mode (background):

```bash
docker-compose up -d
```

## Stopping Docker Containers

To stop the Docker containers, execute:

```bash
docker-compose stop
```

## Accessing Laravel Application and phpMyAdmin

- Access your Laravel application in a web browser at `http://localhost`.
- Access phpMyAdmin at `http://localhost:8080` in your web browser. Use the MySQL database credentials specified in your `.env` file to log in.

## Docker Commands

- Start containers: `docker-compose up -d`
- Stop containers: `docker-compose stop`
- View container logs: `docker-compose logs`

## Directory Structure

- `app/`: Laravel application files
- `nginx/`: Nginx server configuration
- `mysql/`: MySQL database storage
- `phpmyadmin/`: phpMyAdmin configuration files

## Customizations

- Adjust Nginx configuration in `nginx/default.conf` if needed.
- Customize Docker container names, ports, and volumes in `docker-compose.yml`.

## Notes

- Make sure ports `80` and `8080` are not in use by other services on your machine before running Docker.
- This setup is intended for local development purposes. Ensure proper security measures in production environments.

## License

This project is licensed under the [MIT License](LICENSE).

```

You can directly copy and paste this entire block into your README.md file or any other Markdown file.
```
