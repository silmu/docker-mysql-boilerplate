# Docker MySQL boilerplate 🐳

If you don't feel like setting up MySQL on your system, using MySQL in a system agnostic Docker container is a great option.

## Steps to follow

1. Install [Docker](https://docs.docker.com/desktop/setup/install/mac-install/)
2. Copy repository `git clone https://github.com/silmu/docker-mysql-boilerplate.git`
3. Run `docker-compose up -d`

### Troubleshooting 🛠️

If you encounter error logging in for the first time run:

1. `docker exec -it mysql-8-container mysql -u root -p` to login into MySQL in the container
2. Set the authentication plugin to `caching_sha2_password`:

   ```sql
   ALTER USER 'root'@'localhost' IDENTIFIED BY 'root';
   FLUSH PRIVILEGES;
   ```
