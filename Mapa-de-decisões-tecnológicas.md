---
published: true
permalink: /Mapa-de-decisões-tecnológicas/
layout: slate
filename: Mapa-de-decisões-tecnológicas.md
title: Mapa de decisões - Kit de Dados Abertos
desc: Neste mapa são apresentadas diversas formas de publicação de dados abertos, dando ao gestor parâmetros de apoio à decisão.
---

## Mapa de decisões tecnológicas

A tabela abaixo mostra as soluções mais comuns para publicar dados abertos, ordenadas por complexidade e prazo de implementação.

<!---
Abaixo o código HTML da tabela, markdown não suporta colspan.
--->

<table class="tabela-decisoes-tecnologicas">
    <!--<colgroup>
      <col width="118" />
      <col width="424" />
      <col width="302" />
      <col width="200" />
    </colgroup>-->

    <tr>

      <th>
        Solu&ccedil;&atilde;o
      </th>

      <th>
        Pr&eacute;-requisitos
      </th>

      <th>
        Prazo
      </th>

    </tr>

    <tr>

      <td rowspan="2">
        <a href="#publicar-dump-da-base-de-dados">Publicar dump da base de dados</a>
      </td>

      <td class="celula-meio">
        Acesso &agrave; base de dados
      </td>

      <td rowspan="2">
        Curto<br />
      </td>

    </tr>

    <tr>
      <td>
        Servidor web para arquivos
      </td>

    </tr>

    <tr>

      <td rowspan="2">
        <a href="#publicar-dados-em-arquivos-csv">Publicar dados em arquivos CSV</a>
      </td>

      <td class="celula-meio">
        Mecanismo de ETL (caso esteja em banco relacional)
      </td>

      <td rowspan="2">
        Curto<br />
      </td>

    </tr>

    <tr>
      <td>
        Servidor web para arquivos
      </td>

    </tr>

    <tr>

      <td rowspan="3">
        <a href="#publicar-dados-em-arquivos-json--xml">Publicar dados em arquivos JSON / XML</a>
      </td>

      <td class="celula-meio">
        Mecanismo de ETL (caso esteja em banco relacional)
      </td>

      <td rowspan="3">
        M&eacute;dio
      </td>

    </tr>

    <tr>
      <td class="celula-meio">
        Servi&ccedil;o de desenvolvimento
      </td>

    </tr>

    <tr>
      <td>
        Servidor web para arquivos
      </td>

    </tr>

    <tr>

      <td rowspan="2">
        <a href="#desenvolver-mdulo-de-dados-abertos-em-sistema-existente">Desenvolver m&oacute;dulo de dados abertos em sistema existente</a>
      </td>

      <td class="celula-meio">
        Servi&ccedil;o de desenvolvimento
      </td>

      <td rowspan="2">
        Longo
      </td>

    </tr>

    <tr>
      <td>
        Servidor web para deploy da nova solu&ccedil;&atilde;o
      </td>

    </tr>

    <tr>

      <td rowspan="3">
        <a href="#desenvolver-api-restful-de-dados-abertos-desacoplada-da-soluo">Desenvolver API RESTful de dados abertos desacoplada da
        solu&ccedil;&atilde;o</a>
      </td>

      <td class="celula-meio">
        Mecanismo de ETL
      </td>

      <td rowspan="3">
        Longo
      </td>

    </tr>

    <tr>
      <td class="celula-meio">
        Servi&ccedil;o de desenvolvimento
      </td>

    </tr>

    <tr>
      <td>
        Servidor web para deploy da nova solu&ccedil;&atilde;o
      </td>

    </tr>

    <tr>

      <td rowspan="3">
        <a href="#novo-sistema-com-a-gesto-de-dados-incorporados-em-sua-arquitetura">Novo Sistema, com a gest&atilde;o de dados incorporados em sua arquitetura</a>
      </td>

      <td class="celula-meio">
        Mecanismo de ETL
      </td>

      <td rowspan="3">
        Longo
      </td>

    </tr>

    <tr>
      <td class="celula-meio">
        Servi&ccedil;o de desenvolvimento
      </td>

    </tr>

    <tr>
      <td>
        Servidor web para deploy da nova solu&ccedil;&atilde;o
      </td>

    </tr>

    <tr>

      <td rowspan="3">
        <a href="#publicar-dados-em-arquivos-rdf">Publicar dados em arquivos RDF</a>
      </td>

      <td class="celula-meio">
        Ontologia da &aacute;rea do conhecimento do sistema
      </td>

      <td rowspan="3">
        Longo
      </td>

    </tr>

    <tr>
      <td class="celula-meio">
        Mecanismo de ETL
      </td>

    </tr>

    <tr>
      <td>
        Servidor web para arquivos
      </td>

    </tr>

    <tr>

      <td rowspan="3">
        <a href="#disponibilizar-dados-por-endpoint-sparql">Disponibilizar dados por Endpoint SPARQL</a>
      </td>

      <td class="celula-meio">
        Ontologia da &aacute;rea do conhecimento do sistema
      </td>

      <td rowspan="3">
        Mais Longo
      </td>

    </tr>

    <tr>
      <td class="celula-meio">
        Mecanismo de ETL
      </td>

    </tr>

    <tr>
      <td>
        Banco de dados de triplas
      </td>

    </tr>

    <tr>

      <td rowspan="5">
        <a href="#publicar-dados-em-api-de-dados-ligados-linked-data">Publicar dados em API de dados ligados (Linked Data)</a>
      </td>

      <td class="celula-meio">
        Ontologia da &aacute;rea do conhecimento do sistema
      </td>

      <td rowspan="5">
        Mais Longo
      </td>

    </tr>

    <tr>
      <td class="celula-meio">
        Banco de dados de triplas
      </td>

    </tr>

    <tr>
      <td class="celula-meio">
        Servi&ccedil;o de desenvolvimento
      </td>

    </tr>

    <tr>
      <td class="celula-meio">
        Mecanismo de ETL
      </td>

    </tr>

    <tr>
      <td>
        Servidor web para deploy da nova solu&ccedil;&atilde;o
      </td>

    </tr>
  </table>

<!---
### Lista de Soluções

#### Publicar dump da base de dados

Essa é a forma mais simples de publicação, caso a base de dados não esteja em ambiente próprio, basta pedir extração ao prestador de serviços, disponibilizar no servidor web e providenciar domínio + URL persistente.

**Vantagens e Desvantagens:** curto prazo de implementação, difícil visualização dos dados.

#### Publicar dados em arquivos CSV

Para essa publicação é necessário um mecanismo mínimo de ETL, para poder transformar as tabelas do SGBD em 'tabelas' CSV.

**Vantagens e Desvantagens:** curto prazo, fácil visualização através de ferramentas conhecidas.

#### Publicar dados em arquivos JSON / XML

No caso do CSV bastaria transformar e normalizar uma tabela em outra tabela (SGBD -> SQL). Para essa publicação, será necessária uma transformação mais customizada, respeitando as estruturas dos formatos JSON e XML.

**Vantagens e Desvantagens:** mais trabalhoso de implementar, facilidade de se trabalhar com esses formatos nas linguagens de programação e apis de visualização.

#### Desenvolver módulo de dados abertos em sistema existente

Essa opção só é viável caso o sistema tenha uma arquitetura modular.

**Vantagens e Desvantagens:** coesão da solução; interface única para usuários; maior custo de desenvolvimento.

#### Desenvolver API RESTful de dados abertos desacoplada da solução

Uma decisão importante para essa opção é a separação ou não do banco de dados da API do de produção, que possui várias implicações (performance, atualidade dos dados etc)

**Vantagens e Desvantagens:** possibilidade de consultas mais específicas; Custo de desenvolvimento.

#### Novo Sistema, com a gestão de dados incorporados em sua arquitetura

**Vantagens e Desvantagens:** Sistema desenhado prevendo atendimento da Lei de Acesso à informação, automatização da extração de dados

#### Publicar dados em arquivos RDF


#### Disponibilizar dados por Endpoint SPARQL


#### Publicar dados em API de dados ligados (Linked Data)
-->

### Glossário de Formatos

#### Formatos básicos

##### Dump SQL

De forma genérica, um "_[dump](https://pt.wikipedia.org/wiki/Dump_de_banco_de_dados)_"
é uma descarga de todo o conteúdo de uma base de dados, estruturada de uma
forma que possa ser novamente carregada em um sistema gerenciador de banco de
dados (SGBD) idêntico ou compatível, produzindo-se por esse processo uma base
de dados que é uma cópia fidedigna da original.

Há vários tipos de _dump_. Os formatos textuais podem ser inspecionados em um
editor de textos e geralmente usam a sintaxe SQL no dialeto particular do SGBD
utilizado. Há também os formatos binários que produzem arquivos menores que os
textuais, mas a compatibilidade com versões diferentes do SGBD tende a ser
ainda mais restritiva que a compatibilidade dos formatos textuais.

Os SGBD em geral possuem processos definidos e documentação objetiva de como se
gerar e carregar um _dump_.

`++++++`:
 
* Forma menos trabalhosa de se publicar os dados
* Curto prazo para produção
* Preserva a estrutura dos dados como o são em produção

`------`:

* Provável necessidade de remoção prévia de dados pessoais
* Necessidade de realizar carga dos dados em SGBD para acessá-los
* Não há padronização entre formatos de dumps de SGBSs diferentes: em geral
  necessita-se do mesmo software e versão que gerou o dump

##### CSV

Pode significar [Comma-Separated Values](https://pt.wikipedia.org/wiki/Comma-separated_values)
(valores separados por vírgula), ou
ainda, Character-Separated Values (valores separados por caractere). É um
formato para armazenamento de dados tabulares em texto. A codificação é
muito simples: cada linha do arquivo representa uma linha na tabela, e as
colunas são separadas por vírgula. Campos que podem conter vírgula devem ser
delimitados por aspas. CSV é recomendado para representação de estrutura de
dados mais simples, de natureza tabular, onde não existem subpropriedades ou
listas, gerando um arquivo menor e mais leve para processamento. Arquivos CSV
são processáveis diretamente por editores de planilhas, como o OpenOffice e o
MS Excel. (do [Glossário](/Gloss%C3%A1rio/#csv))

`++++++`:

* Simplicidade. Registros em estrutura tabular.
* Facilidade de geração (qualquer banco de dados exporta)
* Facilidade de consumo (qualquer editor de planilhas manipula)
* Sucinto (os arquivos gerados são menores)

`------`:

* Falta de padronização do formato
* Não suporta tipagem de valores
* Dificuldade em se representar ligações entre os dados

###### Exemplo

 
    Quantidade do item,Valor estimado do item,Decreto 7174,Margem preferencial,Unidade de fornecimento,Situação do item,Valor melhor lance
    6,"R$ 1,590.33",Não,Não,SV,encerrado,R$ 360.00
    8,"R$ 1,480.67",Não,Não,SV,encerrado,R$ 314.98
    6,"R$ 1,700.00",Não,Não,SV,encerrado,R$ 989.00


Fonte: [http://compras.dados.gov.br/pregoes/doc/pregao/1600850000132014/itens.csv](http://compras.dados.gov.br/pregoes/doc/pregao/1600850000132014/itens.csv)

##### JSON

É um acrônimo para
[_JavaScript Object Notation_](https://pt.wikipedia.org/wiki/JSON).
É um padrão aberto de estruturação de dados baseado em texto e legível por
humano. A especificação é a [RFC 7159](https://tools.ietf.org/html/rfc7159).
JSON ganhou maior utilização com a utilização de carga dinâmica de conteúdo
em páginas web com Javascript (técnica denominada "Ajax"). A serialização em
JSON é muito simples e resulta em uma
estrutura pouco verbosa o que se mostra uma ótima alternativa para o XML.
JSON possibilita serialização de estrutura de objetos complexos, como listas e
subpropriedades. JSON está se tornando o padrão mais utilizado para integração
de dados entre repositórios e frameworks, também está se tornando o padrão
nativo de armazenamento em alguns bancos de dados modernos.
(do [Glossário](/Gloss%C3%A1rio/#json))

`++++++`:

* Facilidade para representar hierarquias
* Suporta tipagem de valores
* Facilidade de consumo (qualquer linguagem de programação lê com facilidade)
* Utilizável diretamente em navegadores (leitura por javascript)
* Formato padronizado ([RFC 7159 do IETF](https://tools.ietf.org/html/rfc7159),
  [ECMA-404](http://www.ecma-international.org/publications/files/ECMA-ST/ECMA-404.pdf))
* Possibilidade de definir esquema de validação
* Mais leve para processar que o XML

`------`:

###### Exemplo

    {

        "uasg": ​160085,
        "modalidade": ​5,
        "numero_aviso": ​132014,
        "identificador": "16008505000132014",
        "tipo_pregao": "Eletrônico",
        "situacao_aviso": "Publicado",
        "numero_processo": "64535.029433/2014",
        "tipo_recurso": "Nacional",
        "nome_responsavel": "ELIAS ANTONIO MARCOS CARNEIRO DE ALBUQUERQUE",
        "funcao_responsavel": "Ordenador de Despesas",
        "data_entrega_edital": "2015-04-08T09:00:00",
        "endereco_entrega_edital": "Qg Ex Bl.a 1. Pavimento  - Setor Militar Urbano - Smu/DF",
        "data_abertura_proposta": "2015-04-22T09:00:00",
        "data_entrega_proposta": "2015-04-08T09:00:00"
    }

Fonte: [http://compras.dados.gov.br/licitacoes/doc/licitacao/16008505000132014.json](http://compras.dados.gov.br/licitacoes/doc/licitacao/16008505000132014.json)

##### XML

XML significa [Extensible Markup Language](http://pt.wikipedia.org/wiki/XML),
e é uma sintaxe para codificar documentos em um formato legível por máquina.
É baseado em texto e tem como alguns de seus
[objetivos](http://www.w3.org/TR/REC-xml/#sec-origin-goals) a facilidade de
uso e legibilidade.
XML é largamente utilizado como formato de troca de dados nos clássicos Web
Services SOAP. Apesar da larga utilização, é cada vez menos encorajada a
utilização desse formato para integração de aplicações. Em substituição,
recomenda-se utilizar JSON, por economizar banda e ser de processamento mais
leve. (do [Glossário](/Gloss%C3%A1rio/#xml)).

`++++++`:

* Facilidade para representar hierarquias
* Suporta tipagem de valores
* Amplo suporte de ferramentas
* Formato padronizado ([W3C](http://www.w3.org/TR/2006/REC-xml11-20060816/))
* Possilidade de definir esquema de validação

`------`:

* Prolixo (os arquivos gerados são maiores)
* Maior gasto de processamento para geração e consumo em relação ao JSON.

###### Exemplo

    <resource>
        <_links>
            <link href="/fornecedores/id/linha_fornecimento/308" rel="self" title="Linha de Fornecimento 308: EQUIPAMENTOS PARA PURIFICAÇÃO DE ÁGUA"/>
            <link href="/fornecedores/v1/fornecedores?id_linha_fornecimento=308" rel="fornecedores" title="Fornecedores associados a esta Linha de Fornecimento"/>
            <link href="/materiais/id/material/4610" rel="material" title="Material 4610: EQUIPAMENTOS PARA PURIFICAÇÃO DE ÁGUA"/>
        </_links>
        <id>308</id>
        <codigo_material>4610</codigo_material>
        <tipo>Material</tipo>
        <ativo>true</ativo>
    </resource>

Fonte: [http://compras.dados.gov.br/fornecedores/doc/linha_fornecimento/308.xml](http://compras.dados.gov.br/fornecedores/doc/linha_fornecimento/308.xml)

#### Formatos geo

Alguns formatos de arquivo servem especificamente para representar dados
geográficos. A seguir, são relacionados os principais padrões abertos para
dados geo, juntamente com as vantagens e desvantagens de cada um.

##### GeoJSON

É um formato aberto baseado em [JSON](/Gloss%C3%A1rio/#json) para representar
informações geográficas. Possibilita representar formas como pontos, linhas e
polígonos com coordenadas geográficas, juntamente com seus atributos
não-espaciais.
O GeoJSON não é mantido por um órgão formal de padronização, como alguns
outros formatos para informações geográficas. Em vez disso, ele é
[especificado](http://geojson.org/geojson-spec.html)
por um grupo de trabalho de desenvolvedores.
(do [Glossário](/Gloss%C3%A1rio/#geojson)).

`++++++`:

* Todos os benefícios do JSON
* Bom suporte de ferramentas
* Leve para processamento

`------`:

* Falta padronização (embora a especificação seja aberta)

###### Exemplo

    {
       "type":"FeatureCollection",
       "features":[
          {
             "type":"Feature",
             "id":"ubs.fid--4ce37384_151a5912be6_34da",
             "geometry":{
                "type":"MultiPoint",
                "coordinates":[
                   [
                      -43.023,
                      -6.767
                   ]
                ]
             },
             "geometry_name":"geometria",
             "properties":{
                "codigo":"9724",
                "empreendimento":"Floriano - PI - UBS I",
                "subeixo":"Comunidade Cidadã",
                "tipo":"UBS",
                "orgao_responsavel":"Ministério da Saúde",
                "executor":"Municí­pio",
                "unidade_federativa":"PI",
                "municipio":"FLORIANO",
                "investimento_previsto":"--",
                "observacao":"",
                "estagio":"Concluí­do",
                "data_de_referencia":"31 de Outubro de 2014",
                "count":0
             }
          },
          {
             "type":"Feature",
             "id":"ubs.fid--4ce37384_151a5912be6_34db",
             "geometry":{
                "type":"MultiPoint",
                "coordinates":[
                   [
                      -40.616,
                      -7.088
                   ]
                ]
             },
             "geometry_name":"geometria",
             "properties":{
                "codigo":"9725",
                "empreendimento":"Fronteiras - PI - UBS I",
                "subeixo":"Comunidade Cidadã",
                "tipo":"UBS",
                "orgao_responsavel":"Ministério da Saúde",
                "executor":"Municí­pio",
                "unidade_federativa":"PI",
                "municipio":"FRONTEIRAS",
                "investimento_previsto":"--",
                "observacao":"",
                "estagio":"Em obras",
                "data_de_referencia":"31 de Outubro de 2014",
                "count":0
             }
          }
       ]
    }

Fonte: [http://189.9.137.169:8080/geoserver/pac/wms?service=WFS&version=1.0.0&request=GetFeature&typeName=pac:ubs&outputFormat=JSON](http://189.9.137.169:8080/geoserver/pac/wms?service=WFS&version=1.0.0&request=GetFeature&typeName=pac:ubs&outputFormat=JSON)

##### KML

Acrônimo para
_[Keyhole Markup Language](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)_.
É um formato baseado em XML, desenvolvido originalmente pelo Google e depois
[padronizado](http://www.opengeospatial.org/standards/kml) pelo Open Geospatial
Consortium. Pode representar informações geográficas, tais como
marcadores de local, imagens, polígonos, modelos tridimensionais ou descrições
textuais, usando coordenadas de latitude, longitude e elevação conforme o
sistema [WGS84](https://en.wikipedia.org/wiki/World_Geodetic_System).
(do [Glossário](/Gloss%C3%A1rio/#kml)).

`++++++`:

* Formato padronizado
* Bom suporte de ferramentas

`------`:

* Mais pesado para processamento que o GeoJSON

##### Shapefile ESRI

Formato aberto para dados geoespaciais, desenvolvido pela empresa Esri, que
produz soluções de software para sistemas de informações geográficas (GIS).
Apesar de ser mantido por uma empresa, a sua
[especificação](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf)
é aberta e é implementada por praticamente todas as ferramentas de GIS.
(do [Glossário](/Gloss%C3%A1rio/#shapefile)).

`++++++`:

* Amplo suporte de ferramentas

`------`:

* Falta padronização (embora a especificação seja aberta)
* Necessita múltiplos arquivos para um único mapa
* Possui limitações no armazenamento de atributos

#### Formatos baseados em RDF

A família de formatos
[RDF](https://pt.wikipedia.org/wiki/Resource_Description_Framework)
baseia-se em um metamodelo de grafos para indicar os relacionamentos entre
os nós, onde cada nó pode ser qualquer coisa sobre a qual queira se afirmar
algo. Esse metamodelo possibilita estabelecer relações semânticas entre os
dados, ao descrevê-los conforme um modelo (vocabulário ou ontologia)
preestabelecido para aquele domínio da informação.

Dados conforme esse metamodelo de grafos podem ser armazenados em bancos de
dados especializados, chamados _triple stores_, ou bancos de triplas, numa
referência à forma de descrever o grafo listando cada tripla nó-aresta-nó,
representando sujeito, predicado e objeto.

Ao gravar dados RDF em um arquivo, no entanto, é necessário escolher uma entre
as múltiplas sintaxes possíveis para representar o grafo como uma sequência de
caracteres: XML, N-Triples, Turtle, JSON-LD, RDFa, etc.
(do [Glossário](/Gloss%C3%A1rio/#rdf)).

A seguir, algumas vantagens e desvantagens de se usar RDF em geral para a
publicação de dados. Em seguida, apresentam-se uma breve descrição e as
vantagens e desvantagens de cada um dos formatos de arquivo (sintaxes)
específicos para dados em RDF.

`++++++`:

* possibilidade de utilizar semântica para descrever os dados
* facilita o cruzamento e ligação de dados entre fontes diversas
* potencializa a reutilização de ferramentas especializadas em dados de determinado domínio da informação
* facilita a descoberta de conhecimento ao possibilitar queries mais complexas usando dados de diversos domínios

`------`:

* necessita desenvolver
  [ontologia](https://pt.wikipedia.org/wiki/Ontologia_(ci%C3%AAncia_da_computa%C3%A7%C3%A3o))
  que descreve os conceitos relacionados aos dados
* maior complexidade do metamodelo (grafos)
* maior heterogeneidade nas estrutura dos dados

##### Turtle

Turtle significa _"[Terse RDF Triple Language](https://en.wikipedia.org/wiki/Turtle_(syntax))"_,
ou linguagem sucinta de triplas RDF. Foi criada como uma sintaxe simplificada
para leitura tanto por humanos quanto por máquinas e
[padronizada](http://www.w3.org/TR/turtle/) em 2014.
A indentação e o uso de prefixos são
elementos que facilitam a leitura, assim como o agrupamento de triplas que
possuem o mesmo sujeito ou que possuem o mesmo sujeito e mesmo predicado.

`++++++`:

* Sucinto (os arquivos gerados são menores)
* Simplicidade de leitura por humanos
* Formato padronizado
* Bom suporte de ferramentas
* Leve para processamento

`------`:

###### Exemplo

    <http://orcamento.dados.gov.br/id/2015/Acao/0011>
          a       loa:OperacaoEspecial , loa:Acao ;
          rdfs:label "Contribuição ao Fundo Global para o Meio Ambiente - GEF (MP)" ;
          loa:codigo "0011" .

    <http://orcamento.dados.gov.br/id/2015/ItemDespesa/322014>
          loa:temAcao <http://orcamento.dados.gov.br/id/2015/Acao/0005> .

    <http://orcamento.dados.gov.br/id/2015/ItemDespesa/357389>
          loa:temAcao <http://orcamento.dados.gov.br/id/2015/Acao/0005> .

Fonte: [http://orcamento.dados.gov.br/doc/2015/Acao.ttl](http://orcamento.dados.gov.br/doc/2015/Acao.ttl)

##### RDF/XML

A sintaxe original, quando o padrão RDF foi inicialmente estabelecido, foi a
baseada em XML. Por ser a primeira sintaxe para RDF, o seu suporte em
ferramentas é excelente. Por outro lado, pela verbosidade do XML e pela
sua estrutura hierárquica, os arquivos gerados são geralmente complexos e de
difícil leitura.

`++++++`:

* Formato padronizado
* Amplo suporte de ferramentas

`------`:

* Dificuldade de leitura por humanos
* Utiliza estrutura hierárquica para representar um modelo de grafos
* Prolixo (os arquivos gerados são maiores)
* Mais pesado para processamento

##### JSON-LD

É um formato baseado em
[JSON para Linked Data](https://en.wikipedia.org/wiki/JSON-LD), também
[padronizado](http://www.w3.org/TR/json-ld/) em 2014.
Traz todas as vantagens do formato JSON. A estrutura de mapeamento para IRIs
pode opcionalmente ser separada em um documento JSON de contexto, o que deixa
o JSON principal, onde estão os dados, essencialmente com a mesma estrutura que
um documento JSON comum.

`++++++`:

* Formato padronizado
* Leve para processamento
* Utilizável diretamente em navegadores (leitura por javascript)

`------`:

* Menor suporte de ferramentas por ser um padrão mais recente

