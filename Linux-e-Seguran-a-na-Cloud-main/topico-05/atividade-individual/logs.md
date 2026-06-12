# Análise de Logs do Sistema

## Objetivo
Analisar registos do sistema e do servidor web para identificar eventos relevantes.

---

## Logs do sistema

### Comando utilizado
```bash
journalctl -n 30
```

### Resultado
Foram listadas as últimas 30 entradas do sistema, incluindo inicialização de serviços e atividades normais do sistema.

### Evento relevante
Foi identificado o funcionamento normal dos serviços do sistema, sem erros críticos registados.

---

## Logs do Nginx (acessos)

### Comando utilizado
```bash
sudo tail -n 20 /var/log/nginx/access.log
```

### Análise
Foram registados acessos ao servidor web através de pedidos HTTP normais, indicando utilização ativa do WordPress.

---

## Logs do Nginx (erros)

### Comando utilizado
```bash
sudo tail -n 20 /var/log/nginx/error.log
```

### Análise
Não foram identificados erros críticos no servidor web, indicando funcionamento estável.

---

## Conclusão
A análise dos logs indica que o sistema e o servidor web estão a funcionar corretamente, sem falhas ou eventos críticos relevantes.
