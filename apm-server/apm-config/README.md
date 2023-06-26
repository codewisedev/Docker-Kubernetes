create ElkStack passwords:

```bash
sudo docker exec -it elasticsearchcontainer bash
cd bin
elasticsearch-setup-passwords auto
```

example:

```text
Changed password for user apm_system
PASSWORD apm_system = 9jwIxolfOWaH4k5jngel

Changed password for user kibana_system
PASSWORD kibana_system = LnvaBy6RsE5hZIbhRvmE

Changed password for user kibana
PASSWORD kibana = LnvaBy6RsE5hZIbhRvmE

Changed password for user logstash_system
PASSWORD logstash_system = bbCjx1BvQ9yMTD8g0qJI

Changed password for user beats_system
PASSWORD beats_system = eETbY8FYlmNwXvEx7ZLt

Changed password for user remote_monitoring_user
PASSWORD remote_monitoring_user = 60anaqr03jpkSV0ejkab

Changed password for user elastic
PASSWORD elastic = Fd8PEAWeDqzdntbeoUqc
```

add kibana password:

```bash
sudo docker exec -it kibanacontainer bash
cd bin
kibana-keystore create
kibana-keystore add elasticsearch.password --> kibana pass
```

copy kibana and apm config files:

```bash
sudo docker cp kibana.yml kibanacontainer:/usr/share/kibana/config/
sudo docker cp apm-server.yml apmcontainer:usr/share/apm-server/
```

write this code in kibana dev-tool:

```bash
PUT /log

POST kbn:/api/fleet/epm/packages/apm/8.5.3
{
    "force": true
}
```
