---
title: Template Documentação de Negócio
slug: doc_template_business_documentation.aspx
draft: false

metadata:
  Tag: "guide"
  Project: "template"
  Status: "prod"
---

# Projeto

Este template foi construído através de uma adaptação do CRISP-DM na metodologia adotada pelo Global para avaliar o nível de maturidade das soluções de dados. Os itens levantados neste documento são os mais importantes de serem documentados, entretanto outros pontos podem ser adicionados caso haja necessidade.

Sumário:

- [Fase L0](#Fase-L0)
- [Fase L1](#Fase-L1)
- [Fase L2](#Fase-L2)
- [Fase L3](#Fase-L3)
- [Fase L4](#Fase-L4)
- [Fase L5](#Fase-L5)

--------------------------------------------------------

# Fase L0

## Entendimento do negócio

### Organograma


  Sponsor 
  Brewtech Integration, 
    Gerente: ([Bruna Carla Santos Silveira]) ([99816467@ambev.com.br])
    PO: [Filippo Simoes Ferrari] ([99808568@ambev.com.br])
    Estag: ([Matheus Ferreira Silva]) ([99826089@ambev.com.br])
  

### Motivação


  "Não temos uma base consistente dos copackers no Brasil, assim perdemos muitas horas pprocurando copackers seja via internet ou rede de contatos."

### Descrição do problema


"Dificuldade de encontrar copackers, inviabilizando produções que a ambev não é capaz de atender."

### Solução corrente


"Atualmente temos uma empresa contratada para fazer a prospecção de copackers."

### Objetivo principal


- Diminuir tempo procurando copackers
- Ter base de copackers consolidada. 


Métricas de sucesso

-Aumentar em 15% a base de copackers.



### Objetivos secundários


-Ter a lista de empresas fabricantes de bebidas no Brasil consolidada. 
-Ter todas as opções de empresas que podem ser copackers. 



### Hipóteses


- É possível aumentar a base de copackers em 15% através da base de dados?



### Riscos e contingências



- É possível que a base de dados não seja assertiva para encontrarmos os copackers. 


### Requisitos


- A solução precisa entregar as empresas de fabricação de bebida em nível Brasil. 
- 



### Fontes de dados


- IRIS
- 



### Valuation

Se objetivo for atendido, provavelmente eliminariamos um custo mensal de aproximadamente 11k/mês, com a empresa terceira que faz a prospecção para nós. 

![image](https://user-images.githubusercontent.com/110915069/185122196-4c224dc7-eda2-4b8c-adf7-7c3e16785b37.png)

![image](https://user-images.githubusercontent.com/110915069/185125149-368437ee-cc2e-4a5e-a337-2bce5132add2.png)


E-mail de negociação com a empresa terceira. 


--------------------------------------------------------

# Fase L1



## Avaliação técnica


### Hipóteses

- Problema de negócio: Queremos aumentar a base de copackers para ter melhores opções no mercado. 
    - hipótese 1: coleta de dados através da consulta de cnpj vai melhorar nossa visibilidade. 
    - hipótese 2: Encontrar empresas com CNAE de envase e cruzar informações com CNAE de bebidas, pode nos mostrar alguns copackers já preparados. 
    - hipótese 3: Visualizar em mapa a localização de um copacker x uma filial ambev, pode facilitar a tomada de decisão.  

### Métricas

Aumentar em 15% a capacidade de copackers provenientes do nordeste.  



### Próximos passos




- Análise dos dados
  - Refinamento da coleta de dados
  - validações se podemos entregar para empresa terceira
  - Passar para empresa terceira ir atrás dos copackers e indústrias de bebidas. 
  - Verificar se os dados foram utilizados 


--------------------------------------------------------

# Fase L2

A fase L2 é uma prova de conceito ou a execução do projeto em uma escala reduzida a fim de validar rapidamente se a hipótese é viável. Espera-se que esta etapa finalize com um modelo publicado e validado.

A publicação do modelo nesta etapa tem a finalidade de registrar a aceitação ou a rejeição da hipótese inicial, portanto não precisa necessariamente seguir o rigor de publicação de um projeto que será colocado em produção.

Sugestões do que deveria ser documentado nesta etapa podem ser encontradas na etapa 4 do CRISP-DM (*Modeling*), mas único documento esperado é a documentação técnica no repositório da Iris.

Os entregáveis esperados para esta etapa são: 
- repositório criado no github;
- documentação técnica proposta pela Iris descrevendo se o critério de sucesso foi atingido;
- publicação do modelo no MLFlow ou equivalente;




--------------------------------------------------------
# Fase L3

A fase L3 é equivalente ao MVP. É onde a solução será implementada em pequena escala, portanto é esperado que o projeto seja colocado em produção durante esta etapa, e funcionará como um experimento. A estimativa de retorno também será reavaliada, mas agora na prática.

## Definição do experimento

A primeira etapa da fase L3 corresponde ao final da etapa 4 do CRISP-DM (*Modeling*). Aqui o modelo será refatorado, os conjuntos de treino e teste serão revistos e o projeto deve ser colocado em produção.

### Escopo

Descrição do que será realizado. Uma vez que se trata de uma solução reduzida, é importante delimitar como isto será feito. Por exemplo, a cervejaria que será escolhida para o teste, a linha de produção, a marca, etc.

#### Grupos de controle e de tratamento

Exemplos: 
- mês anterior ao início do piloto; 
- sala de brassagem vizinha sem piloto; 
- média da performance da zona no mesmo período.

#### Duração / quantidade de experimentações

Exemplos:
- 60 lotes; 
- 1 mês;
- 1000 novos exemplos.

#### Critério de sucesso

Idealmente deve ser igual construído com base na métrica definida na etapa L1; 

Exemplos: 
- redução do número de não conformidades deste PTP; 
- redução do volume de paradas por válvula; 
- aumento do número de lotes ou volume produzido por dia.

#### Retorno financeiro estimado

Idealmente o retorno financeiro deve ser construído em função da métrica de sucesso. Caso o retorno avaliado não seja financeiro, espcificar como o retorno foi medido.

Exemplos: 
- redução no número de não conformidades do PTP reduz o custo de não conformidade; 
- aumento no volume produzido por dia dilui o custo de produção;

#### Usabilidade esperada

Exemplos:
- a solução deverá ser utilizada no mínimo 1x ao dia; 
- a solução será utilizada de maneira on-line pelo equipamento, portanto deverá ser utilizado em todo lote;

#### Riscos mapeados do ambiente
Exemplos:
- não temos controle de todas as variáveis conhecidas;
- há sobreposição de variáveis para atingimento da métrica de sucesso; 
- não há situação As Is para ter um cenário comparativo;

### Arquitetura

Overview da arquitetura usada na validação. É importante que a representação contenha as fontes e as tabelas que foram geradas ao longo do processo, os sistemas utilizados (ex: MES Athena, Iris, PowerBI) e os códigos que compõem a solução. Caso necessário, utilize um ou mais documentos a parte para fazer esta representação.
Exemplo:
 - as informações virão pelo MES Athena, feature engineer e inferência feitas em batch pela manhã na Iris e disponibilização das informações em dash PBI via beerlake para usuário consumir informação; Inputs vem via SODA, feature engineer e inferência serão locais em servidor disponível na unidade, tendo a escrita da variável predita direto no PLC; Usuário passará informações via whatsApp todo inicio de semana e inferência será rodada localmente de forma manual pelo time SDC, as predições serão passadas de volta ao usuário em planilha excel;


--------------------------------------------------------

## Resultados experimentação

Equivalente a etapa 5 do CRISP-DM (*Evaluation*) e parte da etapa 6 (*Deployment*), com a diferença que esta será uma segunda avaliação a ser feita pelo negócio e aqui ainda não será tratado do monitoramento da solução.

### Descrição

Descrever se o exeperimento ocorreu como o esperado: 
- revisar os objetivos de negócio e o critério de sucesso definidos no início;
- os grupos de controle e tratamento foram respeitados?
- a duração foi respeitada?
- o critério de sucesso foi atingido?
- a usabilidade foi suficiente?


### Dificuldades enfrentadas

Descrever quais foram as dificuldades enfrentadas.

Exemplos:
- dificuldade de encaixar na rotina do usuário; 
- modelo preditivo não é assertivo o suficiente para esta aplicação;

### Conclusão

Descrever qual foi a conclusão feita com o negócio.

Exemplos:
- o experimento ocorreru conforme o esperado e seguiremos para a fase L4;
- o experimento foi inconclusivo e devemos testar em novas grupos de teste;
- o experimento não ocorreu conforme o esperado e o projeto será cancelado;

------------------------------------------------------
# Fase L4 

Na fase L4 o projeto já foi validado e será colocado em produção em grande escala. O ideal é que isto aconteça de maneira gradual e as expectativas em relação ao projeto continuem sendo atualizadas.

## Produtização

### Revisão da Arquitetura

A documentação da arquitetura pode ser a mesma apresentada na etapa L3, mas deve ser atualizada caso tenha ocorrido alguma mudança.

Exemplo:
- 100% Iris e inferências disponibilizadas como API e acessadas pelo Ceres; 
- o treino dos modelos será feito na Iris, porém o artefato do modelo preditivo será usado localmente com aplicação desenvolvida pelo time de automação da cervejaria; 
- tudo será feito dentro do SORBA;


### Riscos e dificuldades

Exemplos:
- solução em real-time, ainda não temos uma arquitetura standard pra isso; 
- necessidade de uma engenharia de dados grande, ainda pendente, para desenvolver o ETL dos dados para inferência)
- desenvolvimento de front-end e back-end do Ceres; 
- desenvolvimento de front-end no supervisório para disponibilização da informação; 
- desenvolvimento do dash;

### Plano de execução

Elaboração de um planejamento para produtizar o projeto em larga escala com a descrição das etapas de desenvolvimento, pessoas envolvidas e estimativas de tempo para cada etapa.

-------------------------------------------------------

# Fase L5

## Monitoramento

### Cadeia de suporte

Exemplos:
- Quem são os responsávies - time/nome - pelo suporte L1, L2 e L3;

### Monitoramento de funcionamento

Como será feito o monitoramento para garantir que a solução esteja funcionando.

Exemplos:
- verificar alertas de erro em pipelines do databricks; N/A pois é uma modelo via API;

### Monitoramento de performance

Exemplos: 
 - modelos serão reavaliados em D-1 com uma pipeline específica de monitoramento e informações serão disponibilizadas em dash gerencial do time de analytics;
