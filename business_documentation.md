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

No organograma devem ser representadas todas as **pessoas** e **áreas** importantes para o projeto. O requisito mínimo para este item é que sejam identificados os ***sponsors***  e o **cliente / usuário final**. É importante que o nome e o email destas pessoas também sejam registrados.

Exemplos:
  Sponsor 
  Brewtech Integration, 
    Gerente: ([Bruna Carla Santos Silveira]) ([99816467@ambev.com.br])
    PO: [Filippo Simoes Ferrari] ([99808568@ambev.com.br])
    Estag: ([Matheus Ferreira Silva]) ([99826089@ambev.com.br])
  
  CENG
    Diretor: [nome] ([email])
    Especialista de negócio: [nome] ([email])

  ITF cervejaria UB
    Diretor: [nome] ([email])

  Cliente:
    Operador: [nome] ([email])
    Técnico de automação: [nome] ([email])
    Especialista CENG: [nome] ([email])

### Motivação

A motivação deve ser a descrição das **dores** relatadas pelo cliente, tendo como foco o problema e as variáveis envolvidas. 

  "Não temos uma base consistente dos copackers no Brasil, assim perdemos muitas horas pprocurando copackers seja via internet ou rede de contatos."

### Descrição do problema

A descrição do problema deve ser feita em termos gerais, utilizando a linguagem do negócio. Não há necessidade de interpretá-lo como um problema de dados neste momento. 

"Perda de tempo procurando copackers."

### Solução corrente

A solução corrente é a forma como o negócio resolve o problema atualmente ou algum outro *benchmark* que pode ser usado como referência. Esta etapa é importante para ser utilizada como *baseline* para a nova solução que será proposta.

"Atualmente temos uma empresa contratada para fazer a prospecção de copackers."

### Objetivo principal

O objetivo principal pode ser entendido também como objetivo final e estar atrelado a algum KPI conhecido. 

- Diminuir tempo procurando copackers
- Ter base de copackers consolidada. 
****


Exemplos:
  - Diminuir rotina operacional;
  - Aumentar eficiência;
  - Medir a qualidade percebida pelos clientes através das redes sociais.

Métrica de sucesso

Exemplos: 
  - quantidade de lotes fora de especificação;
  - LEF;
  - OAE.

### Objetivos secundários

Quando o objetivo principal é muito complexo, é interessante determinar objetivos secundários para dar um direcionamento de como o objetivo principal pode ser atingido.

-Ter a lista de empresas fabricantes de bebidas no Brasil consolidada. 
-Ter todas as opções de empresas que podem ser copackers. 



Exemplos:
  - Identificar comentários relacionados aos produtos da ambev;
  - Definir qual é a parametrização ideal da lavadora para que a quantidade de garrafas rejeitadas seja a menor possível;
  - Fornecer dados para o operador tomar a decisão;


### Hipóteses

É a tradução do objetivo de negócio definido acima em problemas de dados, ou seja, uma descrição de como o problema poderia ser resolvido através do uso de dados. As hipóteses descritas nesta seção serão o objeto de investigação do Cientista de Dados nas próximas etapas. Para melhores descrições, verifique o item 1.3 do CRISP-DM (*Determine data mining goals*).

- É possível aumentar a base de copackers em 15% através da base de dados?

Exemplos:
- É possível identificar os pallets através da imagem? 
- É possível realizar a contagem de pallets identificados em um vídeo?

### Riscos e contingências

Aqui é importante listar todos os riscos do projeto, sejam eles de negócio (surgiu uma nova solução de mercado), financeiros (o custo da solução pode aumentar se for necessário utilizar abordagens mais complexas), técnicos (a infraestrutura atual não suporta a solução proposta), da dados (os dados não tem qualidade suficiente para atingir o objetivo), etc


- É possível que a base de dados não seja assertiva para encontrarmos os copackers. 

Exemplos:
- É possível que a solução proposta não seja suficiente e abodagens mais sofisticadas sejam ser necessárias;
- É possível que os dados não tenham qualidade suficiente para o desenvolvimento da solução;
- É possível que a base de dados não tenha o volume necessário para o treinamento do modelo.

### Requisitos

Aqui devem ser listados as condições necessárias para que a solução funcione conforme o esperado para atingir o objetivo de negócio.

- A solução precisa entregar as empresas de fabricação de bebida em nível Brasil. 
- 

Exemplos:
- a solução precisa funcionar em tempo real;
- a solução precisa se conectar com o sistema X;
- o modelo precisa estar disponível para consulta conforme a requisição do usuário;
- é necessário disponibilizar a explicação do output feito pelo modelo;


### Fontes de dados

Nesta seção precisam estar listadas todas as fontes de dados necessárias para o desenvolvimento da solução bem como toda informação necessária para seu uso. 

- IRIS
- 

Informações desejáveis:
- Nome da fonte: Ceres, MES ATHENA, LMS, SAP transação MZ01, vídeo de cameras, sistema supervisório, PLC;
- Acesso: Disponível na Iris, Através do SODA, requer ingestão de dados, etc;
- Revisão de LGPD: pendente;
- Periodicidade da consulta: mensal, semanal, diária, real-time;
- Formato: tabular, NoSQL, arquivo;
- Requer serviços adicionais: anotação do label, anotação POS tagging, segmentação de objetos, etc;
- Outras informações relevantes: é preciso comprar usuário para acessar o sistema, os dados devem ser comprados por um serviço X, os dados são de fonte pública, é necessário coletar dados através de scrapping, etc;


### Valuation

Descrever qual é o retorno esperado caso o objetivo seja atingido por completo ou de maneira parcial. É importante que este retorno seja traduzido em valor monetário, mas caso isto não seja possível deve-se descrever como este retorno será medido. 

Caso a memória de cálculo seja muito complexa, deixe um resumo registrado neste documento e o link para o arquivo onde o cálculo foi feito.

Além da descrição acima, é importante registrar o nome das pessoas de negócio que participaram da criação da estimativa, referência para emails trocados ou alguma outra comprovação da concordância entre as partes.


--------------------------------------------------------

# Fase L1

A fase L1 deve acabar com a avaliação técnica e uma análise exploratória dos dados indicando se é possível iniciar a etapa de modelagem. Os itens desejáveis na análise exploratória são:

- levantamento das tabelas de interesse;
- validação da suficiência das variáves para o teste das hipóteses;
- validação da suficiência do histórico / volumetrica para o teste das hipóteses;
- especificação do critério de seleção das variáveis (quais variáveis serão usadas);
- descrição dos dados que serão utilizados (distribuição, tipo do dado, etc);
- registro do relacionamento entre as tabelas, caso isto tenha sido descoberto durante a EDA;
- registro do significado de cada campo, caso isto tenha sido descoberto durante a EDA;
- notas de eventuais reuniões feitas com o dono dos dados;
- análise da qualidade dos dados;
- outas análises relevantes pode ser encontradas na etapa 2 do CRISP-DM (*Data understanding*)


## Avaliação técnica


### Hipóteses

Refinamento das hipóteses definidas na etapa anterior com base na análise exploratóra e descrição das estratégias de modelagem para cada hipóteses. 

Exemplos:

- Problema de negócio: Quero reduzir o tempo de linha parada por problemas de válvula; 
    - hipótese 1: construção de um modelo de regressão para previsão da vida útil da válvula; 
    - hipótese 2: construção de um modelo de classificação para previsão de quebra ou não quebra dentro dos próximos 30 dias; 
    - hipóteses 3: construção de um modelo de clustering, agrupando as válvulas diariamente em 2 grupos, análise posterior das características dos grupos para validar que 1 grupo é suscetível a falha e outro não)

### Métricas

As métricas a serem utilizadas podem ser métricas convencionais utilizadas em problemas de regressão, classificação, agrupamento, etc (MAE, MSE, R2, F1-score, AUC, etc), ou métricas de negócio que são geradas a partir de resultados do modelo, porém é necessário ter um objetivo "técnico" bem desenhado para podermos comparar resultados).

Além da definição das métricas é importante, ainda nesta etapa, avaliar a métrica do estado atual ou do benchmark escolhido como referência, pois este valor será um norte para a avaliação do sucesso da POC. Caso mais de uma métrica tenha sido listada para avaliar a solução é interessante destacar qual delas será utilizar como critério de sucesso.


### Próximos passos

Os próximos passos pode ser um plano de execussão da próxima etapa ou uma revisão dos requisitos para que a iniciativa possa se tornar viável.

Exemplo de plano de execussão:

- ingestão de dados
    - contratação do serviço da empresa que irá fornecer os dados;
    - validação da LGPD;
    - criação de usuários para acesso ao sistema;
    - implementação da ingestão;
        - requer a disponibilidade de um engenheiro de dados;
    - validação da ingestão pelo responsável técnico;
    - validação da ingestão pelo negócio;
        - coletar evidências da validação;
    - deploy da ingestão;
- implementação do modelo (requer a disponibilidade de um cientista de dados);
    - refatoração do código da POC;
    - treinamento do modelo com os dados do MVP;
    - validação do modelo;
    - deploy do modelo;



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
