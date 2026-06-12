# Backup e Recuperação

## Objetivo
Criar um backup do WordPress e testar a recuperação dos ficheiros.

---

## Diretório crítico identificado

- `/var/www/html`

---

## Criação do backup

### Comando utilizado
```bash
tar -czvf wordpress-backup.tar.gz /var/www/html/wordpress
```

### Resultado
Foi criado um ficheiro comprimido contendo o WordPress completo.

---

## Pasta de teste

### Comando utilizado
```bash
mkdir ~/teste-recuperacao
```

---

## Recuperação do backup

### Comando utilizado
```bash
tar -xzvf wordpress-backup.tar.gz -C ~/teste-recuperacao
```

---

## Validação da recuperação

### Comando utilizado
```bash
ls ~/teste-recuperacao
```

### Resultado
Os ficheiros do WordPress foram restaurados com sucesso na pasta de teste.

---

## Conclusão
O backup foi criado e restaurado com sucesso, comprovando que o processo de recuperação funciona corretamente.
