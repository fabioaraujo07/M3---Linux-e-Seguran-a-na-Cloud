# Publicação WordPress

## Nível escolhido
Nível 3 - Avançado

## Rota escolhida
Nginx

## Componentes usados
- Servidor web: Nginx
- PHP: versão 8.5.4 
- Base de dados: MariaDB/MySQL
- WordPress: versão 7.0

## Pasta de publicação
/var/www/html

## URL de acesso
http://192.168.150.133/

## Estado da instalação
Instalação concluída e funcional

## Comandos principais utilizados
- systemctl status nginx
- systemctl status php-fpm
- mysql -u root -p
- cp -r wordpress /var/www/html/
- chown -R www-data:www-data /var/www/html

## Limitações encontradas
dificuldades na configuração de permissões / PHP-FPM, bastante troubleshooting na configuração do fichiero config do nginx por causa da versão antiga do php, tive de instalar a versão mais recente e atualizar o field server no ficheiro de config do nginx
 
