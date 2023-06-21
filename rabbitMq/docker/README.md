# RabbitMQ Docker

- Install Docker and Docker-compose
- run the following command

```bash
sudo docker-compose --env-file .env -f docker-compose.yml up --build
```

## change these fields by your specified config in env file:

- RABBITMQ_VERSION
- RABBITMQ_PORT
- RABBITMQ_USERNAME
- RABBITMQ_PASSWORD
