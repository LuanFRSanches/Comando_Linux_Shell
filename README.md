Atalhos mais usados:
Ctrl+l => Limpa a tela
Ctrl+r => Realiza busca no histórico de Comandos
Ctrl+u => Recorta a linha inteira
Ctrl+w => recorta a palavra á esquerda
Ctrl+k => recorta do cursor até o fim da linha
Ctrl+y => Cola o trecho recortado

Comandos básicos:
Shell e explorando o sistema de arquivos

cd => Ultiliza para navegar entre pasta
cd /var => Caminho absoluto 
cd log => Caminho relativo
.. => Volta diretorio
pwd => Ver o diretotio
ls -ltr => Mostra arquivos com data e horas
ls => Lista conteudos do diretorio

Pedindo ajuda e curingas do shell

man => Manual
--help => Manual mas resumido


Comando Importantes LINUX:

Mudar o hostname => hostnamectl set-hostname + nome
Mudar grupo => groupadd + nome
Mudar usuario => useradd + nome
Mudar a home => useradd + nome -d /home/+nome -g + nome -m -s "/bin/bash"
Mudar senha do user => passwd + nome
Usuario como root => nano /etc/sudoers
Ver usuario logado => whoami
