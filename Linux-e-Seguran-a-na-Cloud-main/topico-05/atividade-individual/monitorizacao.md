# Monitorização do Sistema

## Objetivo

Monitorizar o estado geral do servidor Linux, verificando tempo de atividade, utilização de memória, espaço em disco e estado do serviço web.

---

## Tempo de atividade do sistema

### Comando utilizado

```bash
uptime
```

### Resultado

```text
22:12:56 up 20 min, 2 users, load average: 0,00, 0,04, 0,11
```

### Análise

O servidor encontrava-se ativo há aproximadamente 20 minutos. A carga média do sistema (load average) apresentava valores muito reduzidos, demonstrando que o sistema não estava sobrecarregado e possuía recursos suficientes para executar os serviços instalados.

---

## Utilização de memória

### Comando utilizado

```bash
free -h
```

### Resultado

```text
               total        used        free      shared  buff/cache   available
Mem:           1,6Gi       578Mi       410Mi       3,7Mi       767Mi       1,0Gi
Swap:          1,7Gi          0B       1,7Gi
```

### Análise

O sistema possui 1,6 GiB de memória RAM. Apenas cerca de 578 MiB estavam em utilização, mantendo mais de 1 GiB disponível. A memória swap não estava a ser utilizada, indicando que a RAM disponível era suficiente para o funcionamento normal do sistema e dos serviços instalados.

---

## Espaço em disco

### Comando utilizado

```bash
df -h
```

### Resultado principal

```text
Filesystem                         Size  Used Avail Use% Mounted on
/dev/mapper/ubuntu--vg-ubuntu--lv  9,8G  5,6G  3,7G  61% /
```

### Análise

A partição principal do sistema possui uma capacidade total de 9,8 GB, dos quais 5,6 GB estão ocupados. Com 3,7 GB livres, existe espaço suficiente para o funcionamento do sistema, instalação de atualizações e armazenamento de cópias de segurança.

---

## Estado do serviço web

### Comando utilizado

```bash
sudo systemctl status nginx
```

### Resultado

O serviço Nginx encontrava-se ativo (active/running).

### Análise

O servidor web Nginx estava em execução e disponível para responder a pedidos HTTP. Este serviço é responsável pela publicação do WordPress instalado nos tópicos anteriores.

---

## Verificação da estrutura do serviço publicado

### Comando utilizado

```bash
ls /var/www/html
```

### Resultado

```text
index.nginx-debian.html
index.php
license.txt
readme.html
wp-admin
wp-blog-header.php
wp-comments-post.php
wp-config.php
wp-content
wp-cron.php
wp-includes
wp-load.php
wp-login.php
wp-settings.php
xmlrpc.php
```

### Análise

A presença dos diretórios e ficheiros do WordPress confirma que a aplicação continua instalada no diretório de publicação do servidor web.

---

## Conclusão

A monitorização realizada demonstra que o sistema se encontra estável e operacional. O servidor apresenta níveis reduzidos de utilização de recursos, espaço em disco disponível e o serviço Nginx encontra-se ativo. Além disso, a estrutura do WordPress permanece acessível no diretório de publicação, confirmando o correto funcionamento da aplicação web.
