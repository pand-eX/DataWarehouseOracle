# Implementando um Data Warehouse
[![NPM](https://img.shields.io/npm/l/react)](https://github.com/pand-eX/DataWarehouseOracle/blob/main/LICENSE) 

# Sobre o projeto

Data Warehouse é um banco de dados, usado para armazenar informações relativas às atividades de uma organização de forma consolidada. Possibilita a análise de grandes Volumes de dados, que são coletados a partir de um sistema transacionais OLTP(Online Transaction Processing). O DW é organizado para dar suporte à tomada de decisões estratégicas da empresa e usaremos Virtual Machine com o SO(Sistema operacional) Linux com o Oracle integrado para a implementação desse projeto. 



## Why?

por que este projeto faz parte do meu portfólio pessoal, então, eu vou ficar feliz se você pudesse me fornecer qualquer feedback sobre o projeto, código, estrutura ou qualquer coisa que você possa relatar que poderia me fazer um engenheiro de dados melhor!

Email-me: henricao_7@yahoo.com.br

Connect with me at [LinkedIn](https://www.linkedin.com/in/henrique-castro-484269203//).


## Entendendo a necessidade do Cliente !


A XYZ Inc. com sede em São Paulo-SP, é uma das maiores empresas do Brasil no segmento de venda de eletrônicos direto ao consumidor. A empresa possui diversas lojas em todo estado de São Paulo, além de Rio de Janeiro, Minas Gerais, Pernambuco, Bahia, Goiás e Santa Catarina. Em seu sétimo ano de operação, a empresa tem conseguido manter boas margens de lucro, com um crescimento anual de faturamento na ordem de 8,2%. O CEO decidiu que é hora de expandir as operações e precisa compreender melhor o cenário atual da empresa. Depois de extensa pesquisa, o CEO e o board de diretores decidiram que uma solução de Business Intelligence, com métricas e KPIs referentes ao negócio da empresa seriam úteis para compreender erros/acertos na gestão até aqui e ajudar na definição da estratégia de crescimento para os próximos anos. Foi criado então o projeto BIAVANTE, com o objetivo de fornecer uma solução de Business Intelligence corporativa. A área de TI da companhia já possui licenças de software de solução de BI para geração de relatórios, de um pacote de software adquirido com um fornecedor. As licenças nunca haviam sido usadas e os diretores determinaram que o software fosse usado, como forma de reduzir custo, uma vez que o pacote já havia sido pago. Entretanto a empresa não possui experiência em Data Warehouses e contrataram você para oferecer a consultoria necessária na construção da solução. Você será responsável pela criação do Data Warehouse e das interfaces ETL. A administração e suporte de primeiro nível será de responsabilidade da equipe de TI da empresa. Em sua primeira reunião, diversos diretores explicaram em linhas gerais como funciona a operação da empresa e registraram isso em ata. Abaixo o resultado desta reunião 
A XYZ Inc. é uma empresa que vende eletrônicos, especialmente equipamentos de informática em geral. A empresa trabalha com margens agressivas e embora o investimento em Marketing seja pequeno, ele é constante. São diversas lojas em todo Brasil e aproximadamente 930 funcionários. Cada loja possui um estoque de diversos produtos eletrônicos, tais como desktops, notebooks, tablets e smartphones, que são os principais produtos da empresa, mas diversos outros produtos são vendidos, como TVs, sistemas de som, periféricos, entre outros. São aproximadamente 250 produtos, distribuídos em 15 categorias. Um armazém situado em Barueri-SP, mantém os produtos que chegam via importação ou de fábricas em São Paulo e Minas Gerais, onde eles são catalogados, recebem um selo RFID e então são despachados para as lojas em todo Brasil. Cada produto possui um código SKU único, além de detalhes que são armazenados no sistema de cadastro de produtos, tais como nome do produto, marca, dimensões e outras especificações técnicas. Sempre que uma venda é registrada em um ponto de venda, uma das 23 lojas em todo Brasil, os vendedores são orientados a criar um cadastro sobre o cliente e solicitar uma autorização para o cliente receber futuras promoções e campanhas de Marketing. Nome, telefone, endereço e e-mail são obrigatórios no cadastro, mas outras informações podem ser solicitadas, principalmente no caso de vendas a prazo, como emprego atual, renda, tempo de residência e número de filhos. A empresa possui também um cadastro de cada loja, que hoje está em planilha Excel. Lá estão o nome de cada loja (uma espécie de apelido que ajuda a identificar cada loja), o endereço, a região, cidade e estado. Cada loja tem um código. Essa planilha atualiza periodicamente o sistema de vendas da empresa, já que cada venda registrada é associada a uma loja. Todas as lojas vendem todos os produtos, mas as lojas mantêm estoques diferentes, como forma de reduzir custos com logística, ou seja, não despachar muitos produtos para as lojas que possuem um volume menor de vendas, o que poderia requerer possível movimentação posterior dos produtos para lojas com volume maior. Cada loja possui um CEP cadastrado cuidadosamente, pois a empresa implementa frequentemente algoritmos de otimização de logística usando análise em grafos. Eles compararam um novo sistema recentemente, depois que ouviram dizer que o sistema, que é baseado em Inteligência Artificial, poderia reduzir em até 25% os custos de combustível otimizando as rotas dos caminhões de entrega! Em cada loja, os funcionários atendem os clientes no showroom, onde os produtos são expostos e também no telefone. Cada loja conta com alguns vendedores, pessoal de limpeza e supervisor, trabalhando em 2 turnos. A empresa pretende começar a vender online, mas ainda não há previsão. Todos os funcionários são cadastrados no sistema interno da empresa, com número de matrícula, dados pessoais e especialidade. Uma venda é sempre feita por um vendedor, pois a empresa paga comissão pelas vendas efetuadas e a matrícula do responsável pela venda fica atrelada a cada venda realizada. O valor e a quantidade de cada venda estão presentes nos relatórios diários da empresa, que são usados para diferentes decisões durante a semana. Mas esses relatórios são manuais, criados normalmente no Excel, e frequentemente apresentam erros. Cada diretor regional precisa saber as vendas por região, para acompanhar o desempenho da sua loja e comparar com as demais regiões. A empresa faz muitas vendas de produtos como um único pacote ou combo, mas que são produtos diferentes. Por exemplo: um desktop pode ser vendido junto com um monitor, teclado e mouse. Embora seja um pacote, os produtos possuem SKUs diferentes, valores diferentes e contribuem de forma diferente quando um desconto é concedido. A empresa calcula o percentual de cada produto em uma venda de pacotes ou combos. Os diretores acreditam que algumas categorias de produtos podem não ser lucrativas e gostariam de confirmar esta informação com o novo sistema de BI. Essa informação também será útil para definir as estratégias de expansão e quais novas categorias de produtos devem ser consideradas.

## Iniciando o Projeto Passo a Passo!!!

- Então vamos implementar um processo que algumas empresas paga milhares de reais para implementar e por isso vou tentar mostrar o passo a passo. 
Vou tomar como base que você já implementou o Oracle no SO Linux(Redhat), se eu fizesse esse processo o projeto ficaria gigantesco e tiraria o foco da criação do DW.
 Como estou fazendo um processo pessoal só terei um Banco de dados que é o Oracle, mas ele vai servir para 3 propósito diferente nos teremos um esquema para fonte de dados, um esquema para Staging Area e um esquema para o DW em si.
vamos começar executando o sistema para fonte de dados. Lembrando que em um projeto de DW você não precisa cria a fonte isso será o sistema de banco de dados RCP, sistema CRM, uma planilha Excel, um arquivo txt ou de qualquer outra fonte. 
O que estou fazendo aqui é só para simular o ambiente para que vocês possam ver como funciona todo o processo do início ao fim.


- Agora que compreendemos a necessidade do cliente mantenha o foco nele!!! Objetividade e Simplicidade são uma Arte então vamos praticar!
Vou procurar ser objetivo, mantendo as coisas simples não inventando coisas desnecessária apenas para aumentar o projeto para deixar as coisas mais interessante ou parecer mais sábio do que eu sou realmente é embora essa não seja a regra em várias situações. Vou manter o foco no cliente.
Para iniciarmos o projeto precisamos estudar o processo de implementação de uma solução de Business Intelligence porque o Data Warehouse é um componente de uma solução de BI

![1](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/1.png)
 
 O processo de implementação do BI tem 5 fazes principais: 
![2](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/2.png)
 

![3](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/3.png)
![4](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/4.png)

Na parte de Compreensão das necessidades do cliente precisa fazer uma reunião com Diretores e Gestores nas sessões de Captura de conhecimento onde listaremos:

- Qual o objetivo?
- Quem se beneficia deste Projeto?
- Quais os problemas atuais?
- Quem será o sponsor do projeto?
- Qual o orçamento disponível?
- Quais os recursos disponíveis?
- Quais são os relatórios atuais 
e ainda nessa etapa reuniões internas com diferentes atores-chaves. Análise de documentos. Consulta a processos e métodos usados na empresa. Mapeamento de processos.
No Levantamento de Requisitos a reunião são com os analistas com algumas pessoas que são os líderes de equipe aqueles Profissional que tem o conhecimento da área de negócio em si listamos algumas dessas tarefas:
- Reuniões com profissionais funcionais.
-Lista de requisitos principais.
-Aceite e concordância entre os key stakeholders.
-Critérios de aceite.
-Detalhes sobre o funcionamento final da solução
-Entregáveis finais do projeto.
-Os requerimentos devem ser Smart(specific, Measurable, Attainable, Relevant e Time-Based)
-Sessões de Feedback.
Arquitetura é preciso de pessoas da área de TI para montar a solução que seja viável tecnicamente nela listaremos algumas etapas:
-Reuniões internas com equipe de TI.
-Identificar fontes de dados.
-Identificar Recursos computacionais.
-Sistemas legados.
-Integrações e Interfaces
-Fornecedores que impactam no projeto.
- Como os dados são armazenados
-Design da solução de ETL(Extract, Transform and Load)
-Modelagem (Lógica, dimensional e Física)
- Objetivo do Projeto 
Este projeto faz parte do projeto BIAVANTE da XYZ Inc, tendo como objetivo implementar um Data WareHouse para suportar as soluções de BI, análise e tomada de decisões.
- O Projeto inclui a entrega de dois produtos:
 Data Warehouse
Interfaces ETL para integração com as fontes de dados.

## Atenção !!!

- Nesses processos de levantamento de requisitos e necessidade do cliente não é responsabilidade do Engenheiro de dado mas quis mostrar o início do projeto para ter uma direção e entendimento de como se inicia um projeto de implementação de um Data Warehouse a partir daqui iremos focar na parte que é responsabilidade de um Engenheiro de dados!!!
Como não tenho um Banco de dados para usar de base irei criar um banco de dados no Oracle como fonte de dados do nosso DW.

- Todos os Script estará em ordem para o melhor entendimento do projeto. Aqui será mais a parte para compreender o que está sendo feito e também a linha do tempo de criação do DW!!! Let's go!

## Arquitetura do Data Warehouse 

![5](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/5.png)

A Staging Area é uma área intermediária usada para o processamento de dados durante o ETL antes de ir para o DW. Basicamente os dados que entra no DW já precisa estar tratos integrados e validados por isso uma área separada para fazer isso.

## Modelo Lógico e Modelo Dimensional 

![6](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/6.png)

O Modelo logico básico para todo projeto de implementação de um DW ele é necessário para entender todo o segmento e necessidade da empresa.


![7](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/7.png)

Uma dica> quanto mais completo estiver o seu modelo dimensional será mais fácil a criação do seu modelo físico então de bastante atenção a esta etapa. 
- Star Squema é um modelo mais consolidado e um modelo um pouco mais normalizado 
- Primeiro lá no modelo lógico não tínhamos a dimensão TEMPO o tempo ele registra a data da venda eventualmente o ano, mês a semana o dia, mas isso é uma informação da venda aqui no modelo Dimensional eu preciso controlar o tempo de uma maneira um pouco mais detalhada até porque nas especificações do cliente ficou claro que ele quer o relatório por dia então eu já sei que o meu nível de Granularidade é até dia então eu preciso extrair da data as informações de ano, mês, semana e dia.
- Outra característica que chama atenção e não ter a dimensão Funcionários é porque não temos? Uma Dica valioso!!! Comece o Data Warehouse pequeno e depois você vai incrementando seu DW. Enquanto você a empresa e a equipe do projeto vai aprendendo você pode incorporar mais e mais dimensões você pode modificando as dimensões adicionando mais atributos modificando seu modelo Star Squema para Snow Flake o Data Warehouse é uma estrutura viva porque ele reflete o negócio da empresa se o negócio muda o negócio tem novos requerimentos é normal que ele também cresça. Voltando a questão da dimensão Funcionários é porque não tem essa necessidade de criar isso agora eu preciso da Dimensão Cliente porque a venda é efetuada pelo cliente, Dimensão Produto pois a venda e feita a partir do produto, eu preciso da dimensão da Localidade pois os gerentes e diretores querem relatórios de vendas por regiões e eu preciso de uma Dimensão Tempo para registrar cada um dos momentos que a venda é efetuada.
Vamos compreender a necessidade do projeto de Chaves e as diferenças entre Surrogate Key x Natural Key conceito importantíssimo quando trabalhos com Data Warehouse. Ele é fundamental por que as chaves que vão determinar os relacionamentos a chaves nada mais são que chaves primarias, chaves estrangeiras e a Surrogate Key é importante você compreender como essas chaves vão ser implementadas porque todo os relacionamentos tudo que você fizer no seu modelo tudo que você extrair informações do DW é feita os relacionamentos entre essas chaves, portanto se isso não for bem implementado é claro que vai gerar problemas lá na frente
- Vamos começar pelo ID_CLIENTE lá no Modelo Lógico nós criamos a Entidade Cliente nós colocamos lá o ID_CLIENTE e chamei com Chave Primaria porque lá no banco Transacional lá na fonte de dados a minha tabela de Cadastro de cliente ela tem uma coluna que identifica cada cliente de forma única essa coluna e chamada de chave primaria só que quando você trabalha com Data Warehouse eu quero na verdade criar um outro campo que ajude com os relacionamentos apenas com o modelo Dimensional esse outro campo é chamado de Surrogate Key que também é chamada de chave artificial a Surrogate Key não existe em nem um outro lugar ela só existe no Data Warehouse será uma coluna que vai auto incrementar assim que você inserir o primeiro registro será o número 1 na Surrogate Key o segundo o número 2 e etc... Se você analisar uma tabela dimensão você verá uma Surrogate key e também uma chave que é Natural Key não é mais a Chave Primaria e porque fazemos isso? Por que agora ela ajuda a saber de onde vem o registro o que exatamente era esse registro lá na fonte de dados eu tenho algumas vantagens em manter essa informação, entretanto para criar os relacionamentos entre as tabelas no meu modelo Dimensional nós criamos uma chave primaria artificial que é chamada Surrogate Key /\ Nosso Projeto de chave diz que no nosso DW nós não vamos usar a chave primaria da fonte como chave primaria a chave primaria da fonte de dados vai se transformar em uma Natural key ou Business Key e lá no nosso DW será criada uma Surrogate Key uma chave artificial. 
- Outra questão importante é se você observa a tabela Fato_VENDA olha quem vem para tabela fato exatamente as colunas do Surrogate Keys 
- Lembrar e entender os Dados normalizados x Dados Desnormalizados > lembrando que você tem o objetivo do DW que é consulta e você perde performance com dados Normalizados e por isso que você quer desnormalizar. O objetivo do DW é fazer consulta
- Padrões de Nomenclatura > padrões de nome de dimensão, nome de coluna, eventualmente documentação é importante que tenha algum tipo de Padrão. Normalmente as empresas já tem um documento falando sobre esses Padrões você como um Consultor precisa verificar com a emprese se tem algum tipo de padrão sendo adotado caso não exista você cria e utiliza o seu próprio padrão, mas é importante que exista algum padrão. (SK > Surrogate Key /\ NK> Natural Key /\ NM> nome /\ DESC> descrição /\ BY>Binary /\ NR>Valor Númerico /\ FLAG> Feriado)
- Uma das dimensões do seu modelo Dimensional é bastante especial que é o TEMPO e estará em qualquer DW que sempre estará lá para suportar exatamente umas das perguntas principais que você faz para o Data Warehouse ou seja, quando ocorreu aquela venda, quando ocorreu aquela “situação” nós queremos que nosso Data Warehouse responda várias perguntas umas delas é exatamente relacionada ao tempo. A dimensão de tempo não é carregada junto com o processo ETL, ou seja, você não precisa ficar atualizando constantemente a sua dimensão de tempo porque na verdade ela é uma estrutura praticamente estática é uma dimensão que raramente vai mudar. Algumas características quando você construir essa dimensão, veja que nos primeiros temos uma Surrogate Key ou seja um ID único para cada umas das entradas e uma Coluna com a Data do tipo Date e que data é essa? É cada uma das datas que representa cada uma das datas do período de trabalho daquele DW qual é o ano do DW quem responde é o cliente 1 ano? 2 anos? 3 anos? 20 anos? O cliente vai definir qual o período de dados que ele quer analisar então supondo que ele queira quatro anos eu terei entrada de datas para esses 4 anos para que eu posso criar os cruzamentos. 
- Preencha toda a Documentação de todas as colunas sempre que você estiver criando seu modelo Dimensional.
- Modelo Físico ele compreende a criação das Tabelas a definição do armazenamento se eu vou ou não usar ou particionamento, ou seja, se eu terei uma tabela distribuída em mais de um arquivo físico ainda no modelo físico nós definimos também como será a indexação temos que criar algum projeto de índice e tudo isso ocorre na modelagem física  



 - Esse é o nosso objetivo nós queremos cria um modelo dimensional lá no DW eu tenho a fonte de dados inclusive já extrair esses dados para Staging Area mas os dados estão em formato bruto estão sem limpeza eles necessitam de um processo de transformação manipular esses dados esse é o processo ETL 
ETL é como Raul seixas dizia > é uma metamorfose ambulante está sempre em processo de mudança. Precisamos ter a aptidões necessárias para reconhecer tanto as analise técnicas e também as questões envolvidas nas regras de negócio.

- /\ A 1 tabela que vamos carregar é da dimensão Tempo porque os dados da dimensão tempo não vem no ETL ou normalmente não vem. Criando uma operação especifica para carregar a Dimensão Tempo lembrando que dificilmente ela vai mudar ou vai mudar muito pouco na vida útil do seu DW nós não precisamos incluir isso no ETL mas REPITO dependendo do Projeto não existe uma regra única não existe só um padrão vai sempre depender do projeto na maioria dos casos a dimensão Tempo ela varia muito pouco sendo assim, nós podemos gerar os dados que serão carregados dentro dessa TABELA, que dados são esses? Dados referente a data em um determinado período 

Então na Staging Area nós vamos prepara os dados para depois efetuar a carga no DW.
- Nós não usaremos o processo ETL para dimensão Tempo isso nós faremos manualmente no momento que iremos criar o DW.
Na Staging Area nós vamos trabalhar a dimensão Cliente, Localidade e Produto vamos coletar os dados da fonte verificar se precisamos de algum tipo de transformação se eu tenho que limpar os dados e já vou preparando os dados para posterior carga. Além disso, nós vamos preparar uma tabela de vendas não vou preparar a tabela fato ok eu vou prepara a tabela de Vendas porque pelo o que soubemos do nosso projeto os dados de vendas eles estão espalhados por mais de uma Tabela então eu vou agrupar esses dados vou reorganizar colocar em uma única estrutura única tabela e também já preparar para posterior carga na tabela FATO, basicamente vamos preparar dados 4 tabelas. 3 dimensões e para tabela fato e dimensão tempo faremos no DW.
 
 
 ## FIM do Projeto /\ Agora é melhorias continuas!!! 


- Agora com o DW pronto precisamos fazer melhorias no nosso DW
- Deixei de maneira proposital lá na fonte de dados do banco transacional no usuário source uma categoria de hierarquia que não foi bem implementada


![8](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/8.png)

Você pode ver repetição das categorias e isso não pode acontecer no banco de dados Transacional na fonte porque os dados precisam ser NORMALIZADOS .... O dados não é normalizados lá no DW mas na FONTE no banco de dados transacional precisa ser normalizado.

## Implementando Hierarquia na Fonte do banco de dados

Vamos implementar a Hierarquia de forma correta e teremos que alterar todo o processo ETL até carregar de novo nosso TABELA FATO
Primeiro vamos compreender o nível de Hierarquia

![9](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/9.png)

É categoria de acordo com aquilo que a empresa vende ou fornece produto ou Serviço, abaixo dessa categoria nós temos a categoria filha, pessoal e business /\ notebooks para uso pessoal e para uso de empresa serviço. E eu então vou ter cada produto associado ao menor nível da minha Hierarquia o nome do produto Notebook MSI é um grão, ou seja, é o menor nível de Granularidade nós podemos ter níveis do tamanho que quisermos depende daquilo que a empresa implementa. 
As vendas não são associadas a Categoria, o que você vende é o produto o que temos aqui é a Hierarquia para podemos categorizar esses produtos porque depois eu quero emitir um relatório quais foram as Categorias que mais venderam. Quais foram as categorias que mais venderam por região. Quais as categorias que mais venderam por tipo de cliente e etc...
Produto não entra na tabela Categoria porque temos uma tabela apenas para produto depois eu preciso entrar na tabela produto e atualizar a categoria.
- Acabamos de implementar nossa Hierarquia de Categoria veja que nós temos 1 coluna com Todos os Ids 2 Coluna com todas as categorias sem repetição e os respectivos Ids da Categoria Pai

![10](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/10.png)

Agora como disse a cima vamos atualizar a tabela de Produto. Nós mudamos o ID_CATEGORIA e isso não reflete mais na tabela produto, só conseguimos fazer isso pq nós desativamos a Constraints que é a restrição que mantém a integridade referencial então nós desativamos a Constraints, comando > 
ALTER TABLE TB_PRODUTO MODIFY CONSTRAINT TB_PRODUTO_FK1 DISABLE; Utilizamos esse comando antes de realizar todo o processo a cima. Por isso eu conseguir modificar a tabela Categoria mas se agora eu não atualizar a tabela de Produto ficara toda equivocada./\ MODIFICOU AGORA ATIVA PARA FAZER A QUERY comando >
ALTER TABLE TB_PRODUTO MODIFY CONSTRAINT TB_PRODUTO_FK1 ENABLE;
É IMPORTANTISSIMO LEMBRAR DE ATIVAR E DESATIVAR AS CONSTRAINTS ESSE É UM PROCESSO QUE FAZEMOS BASTANTE DURANTE O PROCESSO ETL PRINCIPALMENTE ANTES DE CARREGAR OS DADOS NORMALMENTE VOCÊ DESATIVA OS INDICES E AS CONSTRAINT LÁ DO SEU DW EFETUA A CARGA DEPOIS ATIVA DENOVO SE VOCÊ NÃO ATIVAR VAI TER PROBLEMA DEPOIS NA INTEGRIDADE REFERENCIAL.

## Melhorando a performance VIEW

- Nós podemos ter várias views no nosso banco de dados, podemos criar uma visão por exemplo com uma regra de negócio ou seja, incluo uma clausula WERE essa visão poderia ter vendas apenas de 2018 /\ 2019 etc... Podemos criar uma Visão para cada mês do ano podemos criar uma visão para categoria por exemplo e ai vou criando as visões e depois eu alimento lá por exemplo quando tiver utilizando uma ferramenta de BI ao invés da ferramenta de BI utilizar a QUERY faz uma consulta direta na VIEW é uma boa prática é bem mais seguro pq se eu depois precisar mudar a query eu mudo a query dentro da view mas o meu sistema de BI vai estar apontando para VIEW não preciso mudar nada no sistema eu mudo apenas a view no banco de dados. 
- Só tem uma pequena questão aqui quando nós usamos uma VIEW na prática o que o banco de dados faz é executar a QUERY isso aqui é bom para o ser humano ele não precisa saber da QUERY é simples dar um select na VIEW mas internamente o banco de dados sabe que isso é uma VIEW e executa a query é claro e isso tem um custo no banco de dados vamos visualizar o que é esse custo. (EXPLAIN PLAN FOR /\ EXPLIQUE O PLANO PARA QUERY A BAIXO) 


![11](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/11.png)
Como o otimizador do banco de dados executou essa query? Da seguinte forma! Ele fez o Select Statement /\ ORDER BY /\ utilizou o HASH para o grupo BY e o JOIN e fez um TABLE ACESS FULL ou seja ele não usou nem um índice.
- Claro que no meu exemplo isso não faz diferença porque temos poucas linhas mas se ao invés de 7 linhas eu tivesse 7 milhões de linhas isso aqui faria toda a diferença a query ia ficar muito lenta criar uma VIEW é uma boa alternativa mas não resolve muito o problema da performance porque ainda estou executando a query do mesmo jeito. Então para resolver isso criei uma Materialized VIEWs aonde eu vou armazenar no banco de dados o resultado da execução da QUERY. O que quero é basicamente cada vez que eu executar a VIEW eu não quero executar a QUERY o que quero é olhar para os dados já armazenado no DW aquela QUERY que faz parte dessa VIEW nós vamos executa lá e gravar os registro em um banco de dados quando eu chamar a view novamente eu vou estar com outro plano de execução muito mais veloz 
Repare que ele fez um ACESS FULL apenas em uma tabela que foi a que a gente criou a View materializada se você ver a diferença do plano de execução lá da nossa Query ele fez o TABLE SCAN em 3 tabelas diferentes agora não eu varro apenas uma única tabela tempo de execução é infinitamente menor e eu consigo otimizar de maneira considerável a performance do banco de dados ela também é útil quando você quer conectar em banco de dados remotos por exemplo você tem um DW em um Servidor na unidade de São Paulo e os analista estão no Rio de Janeiro como você vai trafegar os dados?  Eu posso criar uma View Materializada que ela vai consultar do Rio para São Paulo, ela vai em São Paulo consulta o banco de dados traz os dados é claro que isso vai demorar um pouco eu posso cria a View Materializada de noite e no dia seguinte os analista do Rio de Janeiro for trabalhar eles vão consultar os dados localmente do Rio de Janeiro porque criamos a materializad no rio não precisa ficar gastando largura de banda para executar consulta entre Rio e São Paulo eu crio um Data Base Link entre os dois bancos crio uma views materialized no Rio apontando para os dados de São Paulo faço esse processo anoite no dia seguinte os analista estão felizes da vida trabalhando com Alta Performance. E se eu por acaso inserir mais dados na tabela fato? Com certeza a View materialized vai ficar desatualizada porque eu executei a Query apenas uma vez. Para isso podemos fazer um Refrash da View Materializada comando >
EXEC DBMS_MVIEW.refresh(‘mv_vendas_2018’);
-Domingo o DBA do Rio cria a View Materializada durante segunda feira tão trabalhando normalmente, consultando os dados locais quando for na segunda a noite o DBA do Rio agenda esse REFRESH então ele vai atualizar a view materializada a noite com os novos dados que foram carregados na tabela fato na terça de manhã os analistas continuam trabalhando com a view materializada feliz da vida com Alta Performance. Um ambiente profissional

![12](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/12.png)



## Uma coisa importante é definir a estratégia de Refresh 




![13](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/13.png)
Algumas empresas deleta todo o DW e faz o Refresh com os novos dados você atualiza o DW INTEIRO (Depende de vários fatores inclusive o tamanho do DW)
-Outras empresas atualizam o DW, ou seja, apenas aplica as mudanças desde a última carga (dependendo do tamanho do DW é uma abordagem)
-E você pode encontrar forma de detectar as mudanças que ocorreram no sistema fonte entre uma carga e outra e aplicar apenas essas mudanças isso vai reduzir bastante a sua janela de atualização. 

![14](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/14.png)

![15](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/15.png)
Dependendo do banco de dados podemos usar a tecnologia Golden Gate.
No meu caso do banco de dados Oracle nós podemos utilizar o Arquive Logs ele tem um conceito de Data Guard você pode criar uma espécie de banco de dados cópia e todos os Logs do banco de dados os logs(é que contém todos os comandos DML que são aplicado em todas as tabelas são os Logs do banco de dados você pode pega os arquives que exatamente é o resultados desses Logs mover isso para outro banco de dados e aplicar os arquives que é basicamente aplicar as aplicações DML, aquele outro banco de dados fica como se fosse uma cópia) você pode aplicar uma solução semelhante no DW e temos o conceito Golden gate que é para trabalhar com Streaming de dados você pode configurar o Golden Gate para olhar para sua fonte seja ela qual for não apenas o Banco Relacional capturar apenas as mudanças e aplicar no seu sistema Destino. 

![16](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/16.png)
Aqui podemos fazer várias partições para cada mês e quando você atualiza os dados você pode atualizar por partição não preciso atualizar o DW inteiro isso reduz consideravelmente o volume de dados e acelera o tempo de carga e você pode utilizar essa opção e depois se necessário poderia limpar os dados por partição supondo que uma empresa queria por exemplo atualizar os dados de junho eu posso limpar apenas as partições dos dados de junho e carregar apenas nessa partição. Se a partição que são arquivos físicos tiverem em Disco diferente o fato de carregar uma partição não afetaria a performance de consulta dos dados em outra partição ou seja escolher a melhor estratégia de acordo com o que a empresa tem em sua disposição lembrando que o Oracle Particion que é a funcionalidade do oracle para particionamento tem uma licença a parte. 

![17](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/17.png)
No caso de uma empresa ter o nível de granularidade de 5 anos e passa 6 anos precisamos fazer uma estratégia para essa demanda. O que as empresas fazem é criar uma cópia da dimensão, mantendo apenas uma cópia daquele ano que não está no período de 5 anos então você tem no DW apenas os 5 anos, mas se necessário os dados históricos estão ali em mãos em disposição você cria uma cópia da Dimensão e pronto e inclusive você pode utilizar essa cópia em relatórios mesmo você pode criar os relatórios lá na ferramenta de BI apontando para essa dimensão de históricos. 

![18](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/18.png)
Parecido com o SLOWLY CHANGING DIMENSIONS Cada vez que você adicionar um registro você pode guardar o anterior bastaria eu mudar aquela FLAG de ATIVO PARA INATIVO coloca uma data que aquele arquivo foi descontinuado e insiro um novo registro com isso você mantém os históricos dos dados, mas ainda mantendo o versionamento dependendo do DW algumas empresas opta por sobrescrever os dados pega os dados novos e passo por cima do antigo e você perde a informação histórica não existe uma regra vai depende sempre da área de negócio dos objetivos dos recursos disponíveis mas é uma boa pratica ter pelo menos alguns pratica de versionamento. Cria 3 colunas, data de início, data fim e a FLAG que controla a atualização por esses campos  

![19](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/19.png)

# 10 Erros comuns a se evitar em Projetos de Data Warehouse.
![20](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/20.png)
