# Zabbix Server with MySQL, Grafana and Traefik in a Docker Compose

## 🗒️ Describe
Images Used:
* [mysql](https://hub.docker.com/_/mysql/)
* [zabbix-server-mysql](https://hub.docker.com/r/zabbix/zabbix-server-mysql/)
* [zabbix-web-apache-mysql](https://hub.docker.com/r/zabbix/zabbix-web-apache-mysql/)
* [zabbix-web-service](https://hub.docker.com/r/zabbix/zabbix-web-service/)
* [grafana](https://hub.docker.com/r/grafana/grafana/)
* [traefik](https://hub.docker.com/_/traefik/)

## ◼️ Install
Install Docker Engine and Docker Compose by following my guide.

NOTE: If necessary, you can change the docker-compose version at the URL below (v2.17.3). To check the latest version, access the [URL](https://github.com/docker/compose/releases).

```shell
cd /tmp
curl -fsSL https://get.docker.com/ | sh
curl -L "https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

Clone the repository to your system and start the deployment using docker-compose.

NOTE: Before, change MySQL user password and Zabbix/Grafana URL and ACME Email by editing env/db.env and .env files.

```shell
cd /opt
git clone https://github.com/alfredotavio/zabbix-grafana-docker.git
cd /opt/zabbix-grafana-docker
mkdir letsencrypt/
touch letsencrypt/acme.json
chmod 600 letsencrypt/acme.json
docker-compose up -d
```

## 📂 Structure
```shell
.
├── env
│   ├── db.env
│   ├── grafana.env
│   ├── traefik.env
│   ├── zbx-rpt.env
│   ├── zbx-srv.env
│   └── zbx-web.env
├── .env
└── docker-compose.yml
```

## 👨‍💻 Author
<table>
  <tr>
    <td align="center">
      <a href="#">
        <a href="https://www.linkedin.com/in/alfredotavio/"><img src="https://avatars.githubusercontent.com/u/22720865?v=4" width="100px;" alt="Foto do Alfredo Castro"/><br>
        <sub>
          <b>Alfredo Castro</b>
        </sub>
      </a>
    </td>
  </tr>
</table>
