### Informações da máquina
>Host: winnin-ec2-statsd (54.243.226.38)

>SSH Key: WinninWeb.pem

>SSH port: 22

>SSH user: ubuntu

>Docker container owner: root

>WORKDIR: /opt

>BACKUP_DIR: /backups/

>S3_BACKUP_DIR: s3://winnin-bkp/grafana/

>Crontab de backup: 00 01 * * * /opt/docker-grafana-graphite/scripts/backup

### Procedimentos para restaurar um backup:

>logar na máquina winnin-ec2-statsd com ssh

>trocar para o usuário root (sudo su)

>entrar no diretório /opt/docker-grafana-graphite/

>fazer um git pull (descartar qualquer alteração existente)

>pegar o backup a ser restaurado em s3://winnin-bkp/grafana/

>extrair o backup no diretório /opt/

>entrar no diretório /opt/docker-grafana-graphite/scripts

>executar o script "start" (./start)
