# Keycloak Docker

- Install Docker and Docker-compose
- run the following command

```bash
sudo docker-compose --env-file .env -f docker-compose.yml up --build
```

## change these fields by your specified config in env file:

- KEYCLOAK_ADMIN_USER
- KEYCLOAK_ADMIN_PASSWORD
- KEYCLOAK_MANAGEMENT_USER
- KEYCLOAK_MANAGEMENT_PASSWORD
- KEYCLOAK_PORT
- POSTGRES_HOST
- POSTGRES_PORT
- POSTGRES_DB_NAME
- POSTGRES_USER
- POSTGRES_PASSWORD
