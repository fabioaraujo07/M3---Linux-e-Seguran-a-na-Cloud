# Plano de Continuidade Operacional

## Serviço crítico
- WordPress (site principal)
- Nginx (servidor web)
- PHP-FPM (processamento)
- MariaDB/MySQL (base de dados)

---

## Ficheiros e configurações críticas

- `/var/www/html`
- `/etc/nginx/sites-available/`
- `/etc/php/`
- Base de dados WordPress

---

## Logs importantes

- `/var/log/nginx/access.log`
- `/var/log/nginx/error.log`
- `journalctl`

---

## Periodicidade de backup

- WordPress: diário
- Base de dados: diário
- Configurações do sistema: semanal

---

## Procedimento de recuperação

1. Restaurar ficheiros do WordPress
2. Restaurar base de dados
3. Verificar configuração do Nginx
4. Reiniciar serviços (nginx, php, mysql)
5. Validar acesso ao site

---

## Critérios de validação

- Site acessível via browser
- wp-admin funcional
- Nginx ativo
- Base de dados ligada corretamente
- Sem erros nos logs

---

## Conclusão
O plano de continuidade garante que o serviço WordPress pode ser restaurado rapidamente em caso de falha, minimizando o tempo de indisponibilidade.
