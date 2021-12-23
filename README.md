# Near Node monitring
Node monitoring and alerts tools packed in docker-compose.

Main goal of this tooling, is to create easy to use monitoring for Near node and netwrok, out of the box.



This a brief node setup:
- Prometheus 
- NodeExporter
- Alertmanager 
- Telegram Bot


# Guide on how to setup monitoring tool

1) You will need **Telegram bot token** to interact with a bot and your **Telegram id number**:
- to create a token for Telegram bot - message `@BotFather`. Enter command `/newbot` and follow instructions;
- to obtain Telegram id number - message `@userinfobot`. Enter command `/start`.

2) You will need `docker` & `docker-compose` installed on your OS. Check if docker & docker-compose installed:

```
docker -v
```
```
docker-compose -v
```

Install `docker` & `docker-compose` if not installed:

```
apt install docker-compose
```
```
apt install docker
```

3) Clone github repository:
```
git clone https://github.com/doma2k/Near-network-monitoring-tool.git
```

4) Update files:

- `alert_rules.yml` , `prometheus.yml` located in `prometheus` directory;

- `config.yml` located in `alertmanager` directory.

Input your near node ip number instead of `<AAA.AAA.AAA.AAA>`

5) Update `docker-compose.yml` file with the IP address of your near node, **Telegram id** and **bot token**:

Input your near node ip number instead of `<AAA.AAA.AAA.AAA>`

Input your **Telegram id** obtained in step 1 instead of `<telegram_id_number>`

Input your **bot token** obtained in step 1 instead of `<telegram_bot_token>`

6) Run monitoring tool with the following command:

```
docker-compose up
```

To stop docker-compose - use 
```
docker-compose down
```
