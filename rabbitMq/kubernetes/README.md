# RabbitMQ Kubernetes

- Install kubectl

## Convert your username and password to base64 with this code:

```
echo -n 'username' | base64
echo -n 'password' | base64
```

## After start rabbitmq pod, then run this commands:

Enter to rabbitmq container:

```
kubectl exec -it <rabbitmq_pod_name> -- bash
```

Run management plugin with this command:

```
rabbitmq-plugins enable rabbitmq_management
```

## Change these fields by your specified config:

- `username` lines: 6
- `password` lines: 7
- `rabbitmq_version` lines: 25
- `rabbitmq_port` lines: 38, 57, 58
- `rabbitmq_management_port` lines: 39, 60, 61
