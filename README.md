# Projeto-ICD


## Nome dos integrantes:
- Élia Dutra Sena
- Luis Fernando de Araujo Oliveira
- Maria Eloisa Silva de Sousa
- Maria Clara Caldas Fernandes


## Tema:
- Jogos Olímpicos e Paralímpicos de Verão: Análise Comparativa e Socioeconômica do Desempenho Global

## Abordagem de coleta de dados:
- Dados socioeconômicos (Web Scraping)
- Dados dos jogos Olímpicos e Paralímpicos (Web Scraping e CSV Kaggle)


## Sobre conjunto de dados:
Com o intuito de observar mais a fundo o desempenho das nações em competições esportivas, no caso os Jogos Olímpicos e Paralímpicos, foi analisado no âmbito esportivo edições das Olimpíadas e Paralimpíadas (1960-2024), e no âmbito socioeconômico usando o PIB. Com esses dados é previsto observar um reflexo não apenas do talento individual, mas o impacto que o investimento e infraestrutura pode causar no desempenho de uma nação. Compreender como fatores socioeconômicos influenciam esse desempenho é essencial para entender as disparidades globais no esporte e na inclusão social, visto que tambem analisamos as Paralimpíadas, que denuncia fortemente a relação de um pais com os investimentos esportivos e sociais.


## Processo de coleta de dados:
- Extração via Web Scraping:
  
  Dados econômicos (PIB) - Extraído através de dados do portal Worldmeters.
  
  Dados de medalhas - Países e suas respectivas medalhas nas Olimpíadas e Paralimpiadas através de dados da Wikipédia (tabela geral e tabelas por ano).

- Arquivos estruturados (csv):
  
  Dataset Kaggle: Utilização do arquivo estruturado athlete_events.csv proveniente do repositório "120 years of Olympic history: athletes and results". Este arquivo fornece a base histórica detalhada de atletas e resultados de 1896 a 2016.


## Base de Dados:
- *Dados esportivos:*
  
  Histórico de medalhas por ano: país e suas respectivas medalhas recebidas da olimpíada do ano.

  - Paralimpíadas

  | Coluna             | Descrição                                                                                  |
  |--------------------|--------------------------------------------------------------------------------------------|
  | **'Ordem'**        | Ordem de colocação no ranking de medalhas daquela edição                                   |
  | **'País'**         | Nome dos países no formato (NOC nome, ex: BRA Brasil)                                      |
  | **'Ouro'**         | Soma do total de medalhas de ouro que cada país possui                                     |
  | **'Prata'**        | Soma do total de medalhas de prata que cada país possui                                    |
  | **'Bronze'**       | Soma do total de medalhas de bronze que cada país possui                                   |
  | **'Total'**        | Total da somas das medalhas de cada tipo                                                   |

  - Olimpíadas

  | Coluna             | Descrição                                                                                  |
  |--------------------|--------------------------------------------------------------------------------------------|
  | **'Ordem'**        | Ordem de colocação no ranking de medalhas daquela edição                                   |
  | **'País'**         | Nome dos países no formato (NOC nome, ex: BRA Brasil)                                      |
  | **'Ouro'**         | Soma do total de medalhas de ouro que cada país possui                                     |
  | **'Prata'**        | Soma do total de medalhas de prata que cada país possui                                    |
  | **'Bronze'**       | Soma do total de medalhas de bronze que cada país possui                                   |
  | **'Total'**        | Total da somas das medalhas de cada tipo                                                   |

  
  Histórico de medalhas geral: país e a quantidade total de medalhas adquiridas em todas as olimpíadas.

  - Paralimpíadas

  | Coluna             | Descrição                                                                                  |
  |--------------------|--------------------------------------------------------------------------------------------|
  | **'País**          | Nome dos países no formato (nome NOC, ex: Brasil Bra)                                      |
  | **'№'**            | Número de participações no evento                                                          |
  | **'Ouro'**         | Soma do total de medalhas de ouro que cada país possui                                     |
  | **'Prata'**        | Soma do total de medalhas de prata que cada país possui                                    |
  | **'Bronze'**       | Soma do total de medalhas de bronze que cada país possui                                   |
  | **Total**          | Total da soma das medalhas de cada tipo                                                    |

  - Olimpíadas

  | Coluna             | Descrição                                                                                  |
  |--------------------|--------------------------------------------------------------------------------------------|
  | **'No.'**          | Identificação única de cada país                                                           |
  | **'País'**         | Nome dos países no formato (NOC nome, ex: BRA Brasil)                                      |
  | **'Jogos'**        | Número de participações no evento                                                          |
  | **'Ouro'**         | Soma do total de medalhas de ouro que cada país possui                                     |
  | **'Prata'**        | Soma do total de medalhas de prata que cada país possui                                    |
  | **'Bronze'**       | Soma do total de medalhas de bronze que cada país possui                                   |
  | **'Total'**        | Total da somas das medalhas de cada tipo                                                   |

  
  Atletas (Kaggle): dados gerais (nome, gênero, idade, peso, altura, time, esporte, cidade, medalha) sobre todos os atletas que participaram das olimpíadas entre 1896-2016.

  | Coluna             | Descrição                                                                                  |
  |--------------------|--------------------------------------------------------------------------------------------|
  | **'ID'**           | Código individual de cada atleta                                                           |
  | **'Name'**         | Nome completo do atleta                                                                    |
  | **'Sex'**          | Sexo do atleta (M ou F)                                                                    |
  | **'Age'**          | Idade do atleta                                                                            |
  | **'Height'**       | Altura do atleta em metros                                                                 |
  | **'Weight'**       | Peso do atleta em kilogramas                                                               |
  | **'Team'**         | País que o atleta representa                                                               |
  | **'NOC'**          | Comitê Olimpíco Nacional do país                                                           |
  | **'Games'**        | Ano e temporada (verão/inverno) que ocorreu o evento                                       |
  | **'Year'**         | Ano que a olímpiada ocorreu                                                                |
  | **'Season'**       | Temporada do evento (verão ou inverno)                                                     |
  | **'City'**         | Cidades sedes dos jogos                                                                    |
  | **'Sport**         | Esporte que o atleta concorreu                                                             |
  | **'Event'**        | Modalidade expecífica que o atleta competiu                                                |
  | **'Medal'**        | Se o atleta conseguiu medalhas e qual o tipo                                               |

  
- *Dados socioeconômicos:*
  
  PIB mundial.

  | Coluna                  | Descrição                                                                                  |
  |-------------------------|--------------------------------------------------------------------------------------------|
  | **'#'**                 | Ordem de colocação no ranking de países com maior PIB                                      |
  | **'País'**              | Nome dos países                                                                            |
  | **'PIB'**               | O valor do PIB em formato $00,0 trilhões                                                   |
  | **'IB (Valor Total)'**  | O valor do PIB em formato $29.298.025.000.000	                                             |
  | **'Crescimento do PIB'**| Porcentagem de crecimento que o PIB sofreu                                                 |
  | **'PIB per Capita'**    | O valor do PIB total dividido pela população total                                         |


- Pasta do Drive contendo os arquivos CSV:

  https://drive.google.com/drive/folders/1Z0YrWUmL9wC_m_FT78TxeK-zKKCVF80p?hl=pt-br

