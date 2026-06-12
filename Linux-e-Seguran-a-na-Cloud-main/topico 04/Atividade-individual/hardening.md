# Hardening Inicial do Serviço Publicado

## 1. Identificação do serviço

O serviço publicado é uma instalação de **WordPress**, executada sobre o servidor web **Nginx**, com suporte a **PHP-FPM** e base de dados **MariaDB/MySQL**.

---

## 2. Riscos específicos do serviço

O WordPress é um sistema amplamente utilizado e, por isso, um alvo frequente de ataques. Os principais riscos identificados são:

- Ataques de força bruta ao painel de administração (/wp-admin)
- Vulnerabilidades em plugins e temas desatualizados
- Exposição de ficheiros sensíveis (ex: wp-config.php)
- Permissões incorretas em ficheiros e diretórios
- Acesso indevido à base de dados em caso de credenciais fracas
- Divulgação de versões do WordPress, PHP e Nginx (facilitando exploração de vulnerabilidades conhecidas)
- Possíveis ataques via SSH se não houver proteção adicional

---

## 3. Medidas iniciais de hardening

As seguintes medidas são recomendadas para aumentar a segurança do sistema:

- Atualizar regularmente o sistema operativo e pacotes instalados
- Remover ficheiros desnecessários e de teste (ex: info.php)
- Aplicar permissões corretas:
  - diretórios: 755
  - ficheiros: 644
- Garantir que a base de dados só aceita ligações locais (localhost)
- Utilizar passwords fortes no WordPress e na base de dados
- Ativar firewall (UFW) permitindo apenas portas necessárias (22, 80, 443)
- Ocultar ou minimizar exposição de versões do software
- Proteger o ficheiro wp-config.php contra acesso indevido

---

## 4. Medidas que podem ser aplicadas agora

Estas medidas podem ser aplicadas imediatamente no ambiente atual:

- Configuração e ativação do UFW (firewall)
- Correção de permissões dos ficheiros do WordPress
- Remoção de ficheiros de teste ou desnecessários
- Garantir que o serviço Nginx está ativo e atualizado
- Uso de credenciais fortes na base de dados e WordPress
- Verificação de portas abertas com `ss -tuln`

---

## 5. Medidas a implementar em tópicos seguintes

Algumas medidas mais avançadas serão aplicadas em fases posteriores do módulo:

- Implementação de HTTPS com certificado SSL (Let’s Encrypt)
- Instalação de Fail2ban para proteção contra ataques de força bruta
- Restrição de acesso ao /wp-admin por IP
- Configuração avançada de logs e monitorização
- Hardening avançado do PHP (desativação de funções perigosas)
- Configuração de backups automáticos
- Ocultação completa de versões do servidor web e PHP

---

## 6. Conclusão

Foram identificados os principais riscos associados ao WordPress e definidas medidas de hardening iniciais e futuras. As ações propostas aumentam a segurança do sistema sem comprometer o funcionamento do serviço web.
