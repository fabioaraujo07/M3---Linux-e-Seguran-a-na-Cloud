\# Permissões aplicadas

644 Permissão de leitura e escrita para o utilizador, o grupo e os outros só leitura (publico.txt)

640 - Permissão de leitura e escrita para o utilizador, apenas leitura para o grupo (restrito.txt)

u+x - Utilizador tem a permissão de execução de um ficheiro (neste caso script.sh)



\## Ambiente utilizado

VM local



\## Utilizador e grupos

O output encontra-se devidamente identificados na pasta evidencias 



\## Ficheiros criados

\- publico.txt:

\- restrito.txt:

\- script.sh:





|Ficheiro|Permissão |Justificação|
|-|-|-|
|publico.txt|644|Permite que o proprietário leia e escreva no ficheiro, enquanto os restantes utilizadores apenas o podem ler. Adequado para informação pública.|
|restrito.txt|640|Permite que o proprietário leia e escreva, o grupo apenas leia e os restantes utilizadores não tenham qualquer acesso. Adequado para informação sensível ou interna.|
|script.sh|u+x|Adiciona permissão de execução apenas ao proprietário do ficheiro, permitindo que execute o script sem conceder essa permissão aos restantes utilizadores.|





\## Relação com o princípio do menor privilégio



O princípio do menor privilégio defende que cada utilizador ou processo deve ter apenas as permissões estritamente necessárias para realizar as suas tarefas, e nada mais do que isso.



Aplicar permissões totais a todos os utilizadores (777) permite a qualquer utilizador ler, modificar e executar ficheiros sem restrições. Isto aumenta significativamente o risco de:



alterações acidentais ou maliciosas em ficheiros importantes;

fuga ou exposição de informação sensível;

execução de scripts perigosos;

perda de controlo sobre a integridade do sistema.

