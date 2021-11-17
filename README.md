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
ls -la => Lista verbosa

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

alias vi="vim" => Cria alias 
unalias vi => Remove alias

Gerenciando arquivos e diretorio

mkdir + nome => Cria uma diretorio
mkdir -p ~/backup/2021/{01..12}
tree ~/backup => visualiza todo a árvore
touch ~/backup/2021/app01.conf => Cria um arquivo vazio
cp ~/backup/2021/01/app02.conf ~/backup/2021/02 => Copia arquivos
cp -R pasta/pasta => Copia pastas


Parâmetros:
-i => interativo, pede uma configuração antes de sobrescrever
-r => cópia recursivar
-p => preserva atributos(data de modificação, permissões etc.)
-a => cópia recursiva e preserva permissões do arquivo

Move e/ou renomeia arquivos:
mv ~/backup/2021/01/app01.conf ~/backup/2021/02
mv ~/backup/2021/01/app01.conf ~/backup/2021/03/app03.conf
mv ~/backup/2021/01/app03.conf ~/backup/2021/03/app03_novo.conf

Parâmetros:
-i => interativo, pede uma confirmação antes de sobrescrever um arquivo 
-f => força sobrescrevero arquivo de destino

Remover arquivos e diretorios:
rm~/backup/2021/03/app03._novo.conf

Parâmetros:
-i => interativo, pede uma confirmação antes de remover
-f => força remoção do arquivo
-r => remove diretorio de forma recursiva

rm -rf/* => O que acontece?

Remove diretório vazio:
rmdir ~/backup/2021/04e


Leitor de texto:

Lê um arquivo de texxto de forma paginada:
less + diretorio 

Opção de busca:
/ => realiza busca dentro do arquivo
n => mostra a próxima busca encontradas 
N => retorna busca anterior encontrada
q => para sair

Mostra quantidade de linhas, palavras e bytes de um arquivo:
wc + direto e arquivo 

Parâmetros:
-l => quantidade de linhas
-w => quantidade de palavras
-c => quantidade de bytes

Shell Avançado:

curl + site => Vê o site no terminal
cat + nome => ler o arquivo de texto
for i in `cat cep.txt`; do echo  CEP:$i; done => Loop
for i in `cat cep.txt`; do curl https://viacep.com.br/ws/$i/json/; done
for i in `cat cep.txt`; do curl https://viacep.com.br/ws/$i/json/ >> cepsConsultados.txt ; done 
cat cepsConsultados.txt |grep localidade

 

