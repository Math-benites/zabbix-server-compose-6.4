<h1 align="center">Zabbix - Compose </h1>

### Pré-requisitos

Antes de começar, você vai precisar ter instalado 
[Ubuntu 22.04 LTS ](https://releases.ubuntu.com/jammy/)

[Docker Compose version v2.3.3 igual ou superior]


[Docker Engine Version: 23.0.1 igual ou superior]


[Instale o Docker seguindo este guia](https://github.com/Math-benites/docker-install-script)



### 🎲 ( Rodando Compose )

Criando diretorios
```bash
mkdir -p /opt/app/
```

Acessando diretorio
```bash
cd /opt/app
```

 Fazendo Git do projeto
```bash
git clone https://github.com/Math-benites/zabbix-server-compose-6.4.git . 
```

Rodando compose
```bash
docker compose up -d
```

O servidor Zabbix(http) inciará na porta:8880 - acesse <http://MYIP:8880/>

O servidor Zabbix(https) inciará na porta:8443 - acesse <https://MYIP:8443/>

(Necessario importacao de certificado em "/zbx_env/etc/ssl/apache2")

O servidor Grafana inciará na porta:3000 - acesse <http://MYIP:3000>

### 🔧 ( Alterando Configuracoes - Opicional )

Zabbix server.config
```bash
nano ./env_vars/.env_srv
```

Zabbix web.config
```bash
nano ./env_vars/.env_web
```

Zabbix mysql.config
```bash
nano ./env_vars/.env_db_mysql
```


