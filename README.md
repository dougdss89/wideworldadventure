# PROJETO WIDEWORLD ADVENTURE
___________________________________________________

### BEM VINDO AO PROJETO DE ETL/ELT WIDEWORLD ADVENTURE

Este é o projeto de integração das bases de dados do SQL Server
1. AventureWorks
2. WideWorldImporters

O objetivo do projeto é limpar as duas bases de dados, integrá-las em um único Data Warehouse, e então, apresentá-las na camada de visualização.

Na pasta **datamodel** estão as modelagens de dados que serão utilizadas após o processo de ETL.

A pasta **hadoop** contém os arquivos necessários para criação dos Data/Delta Lakes.

# HADOOP
___________________________________________________
Depois de criado a imagem, execute os containers com o comando docker run, com os parâmetros desejados. Pontos que podem ser mudados, são: hostname, nome da rede, volume e o nome do container.

Recomendo que comece pelo nó principal e configure tudo, após, dê um commit e suba os
containers com a imagem finalizada.

Cuidado ao modificar as portas, pode causar conflito com os serviços.

### Core e HDFS-SITE.
São os principais arquivos, cuidado ao configurar. Se quiser manter o arquivo, apenas cole as configurações no HDFS e CORE.

Se alterar o nome do cluster e os nomes dos nós, altere as configurações que utilizam.

No HDFS-SITE, as configurações que você precisa alterar, caso deseje, são as do namenodes e do cluster.

# DATASOURCE
___________________________________________________

As bases de dados utilizadas para o projeto.
Faça o restore no SQL Server para utilizá-las como fonte de dados.

[Adventureworks](https://github.com/Microsoft/sql-server-samples/releases/download/wide-world-importers-v1.0/WideWorldImporters-Full.bak)
e [WideWorldImporters](https://github.com/Microsoft/sql-server-samples/releases/download/wide-world-importers-v1.0/WideWorldImporters-Full.bak)

### SQL Server
____________________________________________________
Se desejar a base RAW, porém, com as tabelas que julguei necessárias para o projeto, pode baixar daqui
A base HML, não tem tratamento nem nada. Já a PRD, os dados estão tratados. Ambas são originadas do banco de dados Adventureworks da Microsoft.

dwadvworks_prd
dwadvworks_hml

**[Faça o download das fontes de dados aqui.](https://drive.google.com/drive/u/0/folders/1dw7fwB9hsgc0sjUspzBVMcetywIdfRNf)**

### PostGreSQL
_____________________________________________________
Os arquivos dw_wideworld e wideworld_hml, são originados da WideWorldImporters, também da Microsoft.
Eles seguem a mesma linha do exemplo anterior, sendo HML a base sem tratamento e o dw_wideworld tratado.

Esses arquivos são para restaurar no banco PostgreSQL.

Para migrar para o SGBD, utilizei o Airbyte, ferramenta de ELT.

Para subir as bases no PostgreSQL use os arquivos:

wideworld_hml
dw_wideworld

**[Faça o download das fontes de dados aqui.](https://drive.google.com/drive/u/0/folders/1dw7fwB9hsgc0sjUspzBVMcetywIdfRNf)**

