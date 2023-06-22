| Final OxCGRT dataset available, June 2023 |
| --- |
| *This repository contains old data*. The OxCGRT stopped publishing real-time updates at the end of 2022. A final version of the OxCGRT dataset is available at https://github.com/OxCGRT/covid-policy-dataset<br/>The final version of the dataset has more jurisdictions and more consistency in data format between files. We recommend people only continue to use this OxCGRT/Brazil-covid-policy repository if they need to access old or historical versions of the OxCGRT dataset. |

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

---

# Brazilian Sub-National Covid-19 Policy Responses
[_Versão em Português disponível abaixo_](#Políticas-Públicas-de-Resposta-à-Covid-19-no-Brasil)

This is a project from the [Blavatnik School of Government](www.bsg.ox.ac.uk), the [FGV EBAPE – Escola Brasileira de Administração Pública e de Empresas](https://ebape.fgv.br), and the [University of São Paulo](http://dcp.fflch.usp.br), contributing to the global [Oxford COVID-19 Government Response Tracker (OxCGRT)](https://www.bsg.ox.ac.uk/covidtracker) at the Blavatnik School.

More information is available on the project's website: [www.bsg.ox.ac.uk/pesquisa-covid19-brasil](http://bsg.ox.ac.uk/pesquisa-covid19-brasil).

---

__Cite this dataset as:__ Anna Petherick, Beatriz Kira, Lorena Barberia, Thomas Boby, Rafael Goldszmidt, and Maria Luciano. [ _Brazil’s Covid-19 Government Response Policies_](http://bsg.ox.ac.uk/pesquisa-covid19-brasil), Blavatnik School of Government, 2020.

---

### Dataset of Brazilian sub-national Covid-19 government response policies
Drawing on the Oxford COVID-19 Government Response Tracker (OxCGRT) [coding system](https://github.com/OxCGRT/Brazil-covid-policy/blob/master/documentation/codebook_subnational.md), we provide a systematic and objective account of the strength of Covid-19 response policies that have been instigated by Brazil’s federal government, state governments, and governments of all state capitals and the second city of each state.

Currently we provide coding for 12 indicators: C1 through C8, H1 through H3, and H6. These indicators allow the creation of two different [indices](https://github.com/OxCGRT/covid-policy-tracker/blob/master/documentation/index_methodology.md): the stringency index and the containment and health index. The dataset is updated continuously in real time.

The Brazilian state data has been incorporated into the primary [OxCGRT/covid-policy-tracker](https://github.com/OxCGRT/covid-policy-tracker) repository. This secondary repository contains a dataset that cannot be interpreted alongside our primary country data, but may be of interest nonetheless. The differences are described below.

#### Differences between the levels of policies

This repo contains data for three levels of policies, described using the suffixes of "GOV", “WIDE”, and “TOTAL”.
Policies described with the suffix "GOV" refers to policies issued only at a specific level of government, and can be used to compare government responses across different levels of government.

Policies described with the suffix “_WIDE” capture all government responses set by a given jurisdiction and its sub-components. “_WIDE” policies do not incorporate general policies from higher levels of government that may supersede local policies, but they do capture policies from higher-level governments if they are specifically targeted at that subnational jurisdiction. For example, if a national government orders events to close in a particular city experiencing an outbreak.
Policies described with the suffix “TOTAL” describe all government responses taken by a specific jurisdiction, those below it , and also includes inherited policies from higher levels that affect that jurisdiction. For example, if a country has an international travel restriction that applies country-wide, this would appear as a NAT_GOV policy and be inherited by STATE_TOTAL and CITY_TOTAL, but not by STATE_WIDE nor CITY_WIDE.

The BRA subnational repo contains eight descriptive labels:
-	NAT_GOV: Policies issued by the Brazilian federal government only.
-	NAT_TOTAL: Part of the OxCGRT international dataset, describes the overall policy environment that applies to residents of the country, including policies set by the subnational governments where those values are more stringent than country-wide action.
-	STATE_GOV: Policies issued by that particular state government only.
-	STATE_WIDE: Describes government responses set by a state and its sub-components. It does not include policies adopted at a higher level of government.
-	STATE_TOTAL:  Describes the overall policy environment that applies to residents of the state, including policies set by the national government where those values are more stringent than state-level action.
-	CITY_GOV: Policies issued by that particular municipal government only.
-	CITY_WIDE: Describes government responses set by a municipality and its sub-components. In Brazil, because the municipality is the lowest level of federation, city_policies policy corresponds to city_gov policies.
-	CITY_TOTAL: Describes the overall policy environment that applies to residents of the city, including policies set by the national government and state government where those values are more stringent than city-level action.


#### Further intepretation
Flags representing distinctions between targeted/general measures for subnational data products are consistent with those in the existing [OxCGRT codebook](https://github.com/OxCGRT/covid-policy-tracker/blob/master/documentation/codebook.md).

The Brazil subnational working paper describes the methodology, data collection protocols, and indicator descriptions.

#### Getting data
The [/data](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/data) folder in this repo contains recent exports from the Brazil sub-national database. You are welcome to build applications that draw directly from this repository. The data is a full export from the database presented in "jurisdiction-day" format, with a column of notes from our data collectors for each indicator. This is updated manually on a regular basis, and so the file name may change. Please note that some of the comments contain commas and other characters interpreted as a delimiter, and so may cause problems when parsing this CSV file.

### Survey data on citzens experiences and opinions relating to Covid-19 and government policies
We also present the original [results](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/data) of two rounds of a survey. The first round was conducted between 6 to 27 May and surveyed 1,654 citizens across eight state capitals. In the second round, 1,861 interviews were conducted between 27 July and 2 October 2020.

The surveys questionnaire was designed to ascertain the extent to which reality on the ground in these eight cities meets the World Health Organization’s (WHO) [list of recommendations](https://apps.who.int/iris/bitstream/handle/10665/331773/WHO-2019-nCoV-Adjusting_PH_measures-2020.1-eng.pdf) of the measures that should be put in place before Covid-19 response policies can be safely relaxed. Both rounds were conducted over the phone and used randomised stratified sampling by age, sex, income and education level.

### Risk of Openness Index (RoOI) derived from the Brazilian sub-national data
As Covid-19 has spread in Brazil, government responses across cities and states have waxed and waned. The dataset of Brazilian sub-national Covid-19 government response policies, combined with data from other sources, provides an overview of the risk and response of different states and cities as they tighten and relax physical distancing measures.

The [_Risk of Openness Index (RoOI)_](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/risk-of-openness-index) is based on the [recommendations](https://apps.who.int/iris/bitstream/handle/10665/331773/WHO-2019-nCoV-Adjusting_PH_measures-2020.1-eng.pdf) set out by the World Health Organisation (WHO) of the measures that should be put in place before Covid-19 response policies can be safely relaxed. As governments seek to calibrate policy to risk, the RoOI aims to inform decision-making on how and when it is safe to open up, and when new measures should be introduced instead.

The detailed calculations and logic behind the formulae are in the [Working Paper](http://bsg.ox.ac.uk/pesquisa-covid19-brasil), but the updated and version controlled source is the [methodology documentation](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/documentation).

### Analysis of specific regions

Detailed policy brief reporting the situation in nine capital cities in Brazil are available in the [/policy briefs](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/policy_briefs) folder.


### Acknowledgments
The authors thank they colleagues for commentary on the survey questions, especially Eduardo Andrade, Thomas Hale, Toby Phillips, Clare Leaver and Cesar Zucco. The survey was funded by the Global Challenges Research Fund, [The Alfred Landecker Foundation](https://www.bsg.ox.ac.uk/research/research-programmes/alfred-landecker-programme), and [Blavatnik School of Government](www.bsg.ox.ac.uk).

The OxCGRT Brazil subnational coders are: Aline Tognini, André Houang, Anna Paula Ferrari Matos, Bárbara Prado Simão, Beatriz Franco, Beatriz Kira, Bruna Maria da Silva Ruys, Camila Sacchetto, Carla Vila, Carlos Danquer Amaral, Carolina Martinelli, Carolina Scherer Beidacki,  Celso Antônio Coelho Júnior, Daniel Pereira Cabral, Danielle Stephanie Gomes Treider, Davi Mancebo Fernandes, Davi Romão, Dayane Ferreira, Déborah Palacio do Sacramento, Denilson Soares Gomes Junior, Elisa Codonho Premazzi, Elisangela Oliveira de Freitas, Fabiana da Silva Pereira, Felipe Natil Martins Moreira, Felipe Paiva Pinto, Gabriel de Azevedo Soyer, Guilherme Ramos, Henrique Oliveira da Motta, Hermann Fernandes Pais, Horácio Figueira de Moura Neto, Isabel Seelaender Costa Rosa, Isabela Blumm, João Ferreira Silva, João Gabriel de Paula Resende, João Pires Mattar, José Renato Venâncio Resende, Larissa Cristina Margarido, Laura Boeira, Letícia de Araújo Dias, Letícia Plaza, Liene Baptista, Luiz Eduardo Barbieri Bedendo, Luiz Guilherme Roth Cantarelli, Marcela Mello Zamudio, Maria Leticia Claro de Faria Oliveira, Maria Luciano, Marília Camargo Miyashiro, Marta Koch, Mateus Henrique Müller, Matheus Porto Lucena, Maurício Nardi Valle, Mayra Henrique de Melo, Natalia Brigagão, Natália Colvero Maraschin, Natália de Paula Moreira, Nicole Guedes Barros, Nicole Nanci, Pedro Arcain Riccetto, Pedro Ferreira Baccelli Reis, Pedro Santana Schmalz, Pollyana Lima, Ricardo Miranda Rocha Leitao, Rodrigo Furst, Tamoi Fujii, Teresa Soter Henriques, Thiago William Pereira Barcelos, Vinicius Tadeu Silvério dos Santos, Viviane de Assis Ignacio, and Walter Vinicius Ribeiro Cancelieri.


----


# Políticas Públicas de Resposta à Covid-19 no Brasil

Esse é um projeto da [Blavatnik School of Government](www.bsg.ox.ac.uk), da [FGV EBAPE – Escola Brasileira de Administração Pública e de Empresas](https://ebape.fgv.br), e da [Universidade de São Paulo](http://dcp.fflch.usp.br), uma expansão do [Blavatnik School of Government OxCGRT](https://www.bsg.ox.ac.uk/covidtracker).

Mais informações estão disponíveis no site do projeto: [www.bsg.ox.ac.uk/pesquisa-covid19-brasil](http://bsg.ox.ac.uk/pesquisa-covid19-brasil).

---

__Citação sugerida para a base de dados:__ Anna Petherick, Beatriz Kira, Lorena Barberia, Thomas Boby, Rafael Goldszmidt, e Maria Luciano.[ _Brazil’s Covid-19 Government Response Policies_](http://bsg.ox.ac.uk/pesquisa-covid19-brasil), Blavatnik School of Government, 2020.

---

### Base de dados de respostas governamentais à Covid-19 a nível subnacional no Brasil
Com base no [sistema de codificação](https://github.com/OxCGRT/Brazil-covid-policy/blob/master/documentation/codebook_subnational.md) do Oxford COVID-19 Government Response Tracker (OxCGRT), esta base de dados apresenta uma medida sistemática e objetivo da força das políticas de resposta ao Covid-19 que foram implementadas pelo governo federal, pelos governos estaduais, e pelos governos de todas as capitais estaduais e da segunda cidade de cada estado.

Atualmente a base de dados inclui 12 indicadores: C1 a C8, H1 a H3 e H6. Tais indicadores permitem a criação de dois [índices](https://github.com/OxCGRT/covid-policy-tracker/blob/master/documentation/index_methodology.md) distintos: o índice de rigidez e o índice de contenção e saúde. A base de dados é atualizada continuamente e em tempo real.

Os dados sobre políticas adotadas no nível estadual foram incoporados também ao [repositório principal do OxCGRT](https://github.com/OxCGRT/covid-policy-tracker). O presente repositório contém um banco de dados secundário distinto, que não deve ser interpretado da mesma forma que o banco de dados principal. As diferenças entre os dois são descritas abaixo.

#### Diferenças entre os níveis das medidas

Este repositório contém dados para três níveis de políticas públicas, descritos usando os sufixos "GOV", “WIDE”, e “TOTAL”. As medidas descritas com o sufixo "GOV" referem-se a políticas emitidas apenas em um nível específico de governo e podem ser usadas para comparar as medidas adotadas por diferentes níveis de governo.

As medidas descritas com o sufixo “_WIDE” capturam todas as respostas adotadas por uma determinada jurisdição e seus subcomponentes. Medidas “_WIDE” não incorporam políticas gerais de níveis mais altos de governo que podem substituir as políticas locais, mas capturam medidas adotadas por níveis mais altos se elas forem especificamente direcionadas para aquela jurisdição subnacional. Por exemplo, se um governo nacional ordenar o fechamento de eventos em uma determinada cidade que está passando por um surto. As políticas descritas com o sufixo “TOTAL” descrevem todas as respostas adotadas por uma jurisdição específica, aquelas abaixo dela, e também incluem políticas herdadas de níveis superiores que afetam essa jurisdição. Por exemplo, se um país tiver uma restrição de viagens internacionais que se aplique a todo o país, isso aparecerá como uma política NAT_GOV e será herdada por STATE_TOTAL e CITY_TOTAL, mas não por STATE_WIDE nem CITY_WIDE.

O repositório brasileiro contém oito rótulos descritivos:
- NAT_GOV: Políticas adotadas apenas pelo governo federal brasileiro.
- NAT_TOTAL: Parte do conjunto de dados internacional OxCGRT, descreve o ambiente de resposta geral do país, incluindo políticas definidas pelos governos subnacionais onde tais valores forem mais rigorosos do que a ação nacional.
- STATE_GOV: Políticas adotadas apenas por aquele governo estadual específico.
- STATE_WIDE: Descreve as respostas do governo adotadas por um estado e seus subcomponentes. Não inclui políticas adotadas em um nível superior de governo.
- STATE_TOTAL: Descreve o ambiente de resposta geral que se aplica aos residentes do estado, incluindo políticas definidas pelo governo nacional onde esses valores são mais rigorosos do que a ação em nível estadual.
- CITY_GOV: Políticas adotadas apenas por aquele governo municipal específico.
- CITY_WIDE: Descreve as medidas adotadas por um município e seus subcomponentes. No Brasil, como o município é o nível de federação mais baixo, a política city_policies corresponde às políticas city_gov.
- CITY_TOTAL: Descreve o ambiente de resposta geral que se aplica aos residentes do município, incluindo políticas definidas pelo governo nacional e pelo governo estadual, onde tais valores forem mais rigorosos do que a ação no nível municipal.

#### Intepretação adicional
Flags representando distinções entre medidas focalizadas ou gerais para níveis subnacionais são consistentes com a [documentação da base dados principal](https://github.com/OxCGRT/covid-policy-tracker/blob/master/documentation/codebook.md).

O relatório sobre os dados brasileiros descreve a metodologia, protocolos de coleta de dados, e uma descrição detalhadas dos indicadores.

#### Acesso aos dados
A pasta [/data](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/data) neste respositório contém arquivos atualizados periodicamente com os dados subnacionais, que estão disponíveis para a construção de aplicações. Os dados são apresentados no formato "jurisdição-dia", com uma coluna com notas escritas pela nossa equipe de codificadores para cada indicador. Os arquivos são autalizados manualmente em intervalos regulares, e o nome do arquivo pode mudar. Note que alguns dos comentários podem incluir vírgulas e outros caracteres como delimitadores, o que pode afetar análises automatizadas do arquivo CSV.


### Dados de pesquisa sobre as experiências e opiniões em relação às políticas de resposta à Covid-19
Nós também apresentamos os [resultados originais](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/data) de duas rodadas de uma pesquisa conduzida com indivíduos no Brasil. A primeira rodada ocorreu entre os dias 6 e 27 de maio com 1,654 indivíduos em oito capitais estaduais, enquanto a segunda rodada ocorreu entre 27 de julho e 2 de outubro, em nove capitais estaduais.

A pesquisa foi desenhada para identificar até que ponto a realidade nessas oito cidades correspondia à [lista de recommendações](https://apps.who.int/iris/bitstream/handle/10665/331773/WHO-2019-nCoV-Adjusting_PH_measures-2020.1-eng.pdf) da Organização Mundial da Saúde (OMS) quanto às medidas que deveriam ser adotadas para a flexibilização segura das políticas de resposta à Covid-19. Ambas as rodadas foram conduzidas pelo telefone e usaram amostras estratificada por idade, sexo, escolaridade e faixa de renda.


### Índice de Risco de Abertura (RoOI) derivado dos dados subnacionais brasileiros
À medida que a Covid-19 se espalhou pelo Brasil, a rigidez das respostas governamentais adotadas por cidades e estados aumentaram e diminuíram. A base de dados de políticas públicas adotadas por unidades subnacionais brasileiras, combinada com dados de outras fontes, fornece uma visão geral do risco e das respostas de diferentes unidades da federação ao longo do tempo.

O _Índice de Risco de Abertura (RoOI)_ é baseado nas [recomendações](https://apps.who.int/iris/bitstream/handle/10665/331773/WHO-2019-nCoV-Adjusting_PH_measures-2020.1-eng.pdf) publicadas pela OMS sobre as condições que devem ser observadas antes que as respostas à Covid-19 sejam relaxadas. O RoOI visa a informar a tomada de decisão acerca de quando é seguro reabrir a economia ou quando medidas mais restritas devem ser adotadas, à medida que governos buscam calibrar suas respostas.

O cálculo detalhado e a lógica por trás da fórmula estão no [relatório de pesquisa](http://bsg.ox.ac.uk/pesquisa-19-brasil), e a versão atualizada está disponível na [documentação deste repositório](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/documentation).

### Análise de regiões específicas

Relatórios individuais relatando a situação de nove capitais brasileiras (São Paulo/SP, Rio de Janeiro/RS, Porto Alegre/RS, Goiânia/GO, Salvador/BA, Recife/PE, Fortaleza/CE, Manaus/AM e Belém/PA) estão disponíveis na pasta [/policy briefs](https://github.com/OxCGRT/Brazil-covid-policy/tree/master/policy_briefs).


### Agradecimentos
Os autores agradecem seus colegas por comentários e sugestões sobre as perguntas de pesquisa, especialmente Eduardo Andrade, Thomas Hale, Toby Phillips, Clare Leaver e Cesar Zucco. A pesquisa foi financiada pelo Global Challenges Research Fund, [The Alfred Landecker Foundation](https://www.bsg.ox.ac.uk/research/research-programmes/alfred-landecker-programme), e pela [Blavatnik School of Government](www.bsg.ox.ac.uk).

O time de codificadores subnacionais do OxCGRT Brasil é composto por: Aline Tognini, André Houang, Anna Paula Ferrari Matos, Bárbara Prado Simão, Beatriz Franco, Beatriz Kira, Bruna Maria da Silva Ruys, Camila Sacchetto, Carla Vila, Carlos Danquer Amaral, Carolina Martinelli, Carolina Scherer Beidacki,  Celso Antônio Coelho Júnior, Daniel Pereira Cabral, Danielle Stephanie Gomes Treider, Davi Mancebo Fernandes, Davi Romão, Dayane Ferreira, Déborah Palacio do Sacramento, Denilson Soares Gomes Junior, Elisa Codonho Premazzi, Elisangela Oliveira de Freitas, Fabiana da Silva Pereira, Felipe Natil Martins Moreira, Felipe Paiva Pinto, Gabriel de Azevedo Soyer, Guilherme Ramos, Henrique Oliveira da Motta, Hermann Fernandes Pais, Horácio Figueira de Moura Neto, Isabel Seelaender Costa Rosa, Isabela Blumm, João Ferreira Silva, João Gabriel de Paula Resende, João Pires Mattar, José Renato Venâncio Resende, Larissa Cristina Margarido, Laura Boeira, Letícia de Araújo Dias, Letícia Plaza, Liene Baptista, Luiz Eduardo Barbieri Bedendo, Luiz Guilherme Roth Cantarelli, Marcela Mello Zamudio, Maria Leticia Claro de Faria Oliveira, Maria Luciano, Marília Camargo Miyashiro, Marta Koch, Mateus Henrique Müller, Matheus Porto Lucena, Maurício Nardi Valle, Mayra Henrique de Melo, Natalia Brigagão, Natália Colvero Maraschin, Natália de Paula Moreira, Nicole Guedes Barros, Nicole Nanci, Pedro Arcain Riccetto, Pedro Ferreira Baccelli Reis, Pedro Santana Schmalz, Pollyana Lima, Ricardo Miranda Rocha Leitao, Rodrigo Furst, Tamoi Fujii, Teresa Soter Henriques, Thiago William Pereira Barcelos, Vinicius Tadeu Silvério dos Santos, Viviane de Assis Ignacio, e Walter Vinicius Ribeiro Cancelieri.

