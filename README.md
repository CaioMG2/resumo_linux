Resumo de estudos sobre o sistema operacional Linux.

Linux

Kernel:
- Core do sistema, gerencia CPU, memória, etc.
- Liga usuário ao hardware.

Comandos no Terminal:
Sintaxe: COMANDO -OPÇÕES ARQUIVOS/DIRETÓRIOS

1. **cd**:
   - Mudar de diretório.
   - Mudança direta: cd /etc/
   - Mudança relativa: cd ssh (dentro de /etc/)
   - Voltar: cd --
   - Pai do diretório atual: cd ..
   - Mover dois diretórios acima: cd ../../
   - Último diretório antes do atual: cd -
   - Home do usuário: cd ~
   - Avançar em outro diretório: cd ../var/
   - Completar diretório: usar TAB
   - Mudar e executar: cd ../ && ls

2. **ls**:
   - Listar arquivos/diretórios.
   - Detalhes: ls -l
   - Arquivos ocultos: ls -a
   - Tamanho legível: ls -lh
   - Data modificação: ls -ltr
   - Sub-diretórios: ls -R
   - Ordem reversa: ls -r
   - Ordenar por tamanho: ls -lS ou ls -lSh

3. **clear**:
   - Limpar tela.

4. **cat**:
   - Mostrar conteúdo de arquivo.
   - Mostrar vários arquivos: cat file1 file2
   - Criar arquivo: cat > file.txt
   - Mostrar linhas numeradas: cat -n file
   - Final de linha: cat -e file
   - Criar e adicionar: cat file1 > file2
   - Adicionar conteúdo: cat file1 >> file2

5. **mkdir**:
   - Criar diretórios.
   - Verbose: mkdir -v

6. **rm**:
   - Remover arquivos/diretórios.
   - Interativo: rm -i
   - Diretório vazio: rm -dv
   - Forçar: rm -rfv
   - Remover diretório: rmdir

7. **cp**:
   - Copiar arquivos/diretórios.
   - cp arquivo_origem destino
   - cp -r diretorio_origem destino

8. **mv**:
   - Mover/renomar arquivos/diretórios.
   - mv arquivo diretorio
   - mv arquivo novo_nome

9. **pwd**:
   - Mostrar diretório atual.

10. Atualizar Bibliotecas:
    - sudo apt-get update

11. Instalar Programa:
    - sudo apt-get install <programa>

12. Remover Programa:
    - sudo apt remove <programa>

13. Gerenciar Usuários:
    - Adicionar: sudo adduser <nome>
    - Deletar: sudo userdel --remove <nome>
    - Alterar: sudo usermod -c 'novonome' <nome>

14. Grupos:
    - Ver grupos: getent group
    - Criar: sudo groupadd -g <id> <nome>
    - Deletar: sudo groupdel <nome>
    - Mover: sudo usermod -a -G <grupo> <usuário>
    - Superusuário: sudo su

15. Permissões:
    - Leitura (R), Escrita (W), Execução (X).
    - Permissão simbólica: chmod <permissões> arquivo/diretório

16. Alterar Proprietário:
    - chown <usuário> <arquivo>

17. Alterar Grupo:
    - sudo chgrp <grupo> <arquivo>

18. Histórico de Comandos:
    - HISTORY

19. Compactação/Descompactação:
    - Tar: compactar: tar -cvf <arquivo>.tar <diretório>
           descompactar: tar -xvf <arquivo>.tar
    - Zip: compactar: zip -r <arquivo>.zip <diretório>
           descompactar: unzip <arquivo.zip>

Permissões no Linux:

Permissões em um sistema Linux permitem controlar quem pode acessar, modificar ou executar arquivos e diretórios. Elas são divididas em três grupos: owner (dono), group (grupo) e others (outros). Cada grupo tem permissões para leitura, escrita e execução, representadas pelas letras R, W e X, respectivamente.

Sintaxe: chmod <permissões> arquivo/diretório

Permissões podem ser definidas numericamente, usando valores de 0 a 7:
- 0: Nenhuma permissão
- 1: Execução
- 2: Escrita
- 3: Escrita e execução
- 4: Leitura
- 5: Leitura e execução
- 6: Leitura e escrita
- 7: Leitura, escrita e execução

Também é possível usar notação simbólica, que inclui o uso de + (adicionar), - (remover) e = (definir).

Essas permissões são essenciais para garantir a segurança e a integridade dos dados em um sistema Linux.
