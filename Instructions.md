# INSTRUÇÕES DO PROJETO
Esse é um arquivo que contém as instruções para execução do projeto.
Neste arquivo, oriento como executar os containers com as ferramentas utilizadas.

## HADOOP

Depois de criado a imagem, execute os containers com o comando **docker run**, com os parâmetros desejados.
Pontos que podem ser mudados, são: hostname, nome da rede, volume e o nome do container.

**Recomendo que comece pelo nó principal e configure tudo, após, dê um commit e suba os**  
**containers com a imagem finalizada.**

_Cuidado ao modificar as portas, pode causar conflito com os serviços._

### Core e HDFS-SITE.

São os principais arquivos, cuidado ao configurar. Se quiser manter o arquivo, apenas cole as configurações no
HDFS e CORE.

_Se alterar o nome do cluster e os nomes dos nós, altere as configurações que utilizam._

