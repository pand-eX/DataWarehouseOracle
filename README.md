
# Implementing a Data Warehouse !!!


[![NPM](https://img.shields.io/npm/l/react)](https://github.com/pand-eX/DataWarehouseOracle/blob/main/LICENSE) 

# About the project

Data Warehouse é um banco de dados, usado para armazenar informações relacionadas às atividades de uma organização de forma consolidada. Permite a análise de grandes volumes de dados, que são coletados de um sistema transacional OLTP (Online Transaction Processing). A DW está organizada para apoiar a tomada de decisão estratégica da empresa e usaremos a Virtual Machine com o Sistema Operacional Linux (Sistema Operacional) com a Oracle integrada para a implementação deste projeto.



## Why?

porque este projeto faz parte do meu portfólio pessoal, então ficarei feliz se você puder me fornecer qualquer feedback sobre o projeto, código, estrutura ou qualquer coisa que você possa relatar que possa me fazer um melhor engenheiro de dados!

Email-me: henricao_7@yahoo.com.br

Connect with me at [LinkedIn](https://www.linkedin.com/in/henrique-castro-484269203//).


## Entendendo a necessidade do cliente!


A XYZ Inc. com sede em São Paulo-SP é uma das maiores empresas do Brasil no segmento de vendas diretas ao consumidor de eletrônicos. A empresa possui diversas lojas em todo o estado de São Paulo, além do Rio de Janeiro, Minas Gerais, Pernambuco, Bahia, Goiás e Santa Catarina. Em seu sétimo ano de operação, a empresa conseguiu manter boas margens de lucro, com crescimento anual da receita em torno de 8,2%. O CEO decidiu que é hora de expandir as operações e precisa entender melhor o cenário atual da empresa. Após extensa pesquisa, o CEO e o conselho de administração decidiram que uma solução de Business Intelligence, com métricas e KPIs relacionados ao negócio da empresa, seria útil para entender erros/sucessos na gestão até agora e ajudar na definição da estratégia de crescimento para os próximos anos. O projeto BIAVANTE foi então criado, com o objetivo de fornecer uma solução corporativa de Business Intelligence. O departamento de TI da empresa já possui licenças de software de solução de BI para relatórios, um pacote de software comprado de um fornecedor. As licenças nunca haviam sido utilizadas e os diretores determinaram que o software fosse usado como forma de reduzir custos, uma vez que o pacote já havia sido pago. No entanto, a empresa não tem experiência em Data Warehouses e contratou você para oferecer os conselhos necessários na construção da solução. Você será responsável pela criação das interfaces Data Warehouse e ETL. A administração e o suporte de primeiro nível serão de responsabilidade da equipe de TI da empresa. Em sua primeira reunião, vários diretores explicaram em termos gerais como funciona a operação da empresa e registraram isso em ata. Abaixo está o resultado desta reunião 
A XYZ Inc. é uma empresa que vende eletrônicos, especialmente equipamentos de informática em geral. A empresa trabalha com margens agressivas e embora o investimento em Marketing seja pequeno, é constante. São diversas lojas em todo o Brasil e aproximadamente 930 funcionários. Cada loja possui um estoque de diversos produtos eletrônicos, como desktops, notebooks, tablets e smartphones, que são os principais produtos da empresa, mas vários outros produtos são vendidos, como TVs, sistemas de som, periféricos, entre outros. São aproximadamente 250 produtos, distribuídos em 15 categorias. Um armazém localizado em Barueri-SP, mantém produtos que chegam via importação ou de fábricas em São Paulo e Minas Gerais, onde são catalogados, recebem um selo RFID e depois são despachados para lojas de todo o Brasil. Cada produto possui um código SKU exclusivo, bem como detalhes que são armazenados no sistema de registro do produto, como nome do produto, marca, dimensões e outras especificações técnicas. Sempre que uma venda é registrada em um ponto de venda, uma das 23 lojas em todo o Brasil, os vendedores são instruídos a criar um cadastro sobre o cliente e solicitar uma autorização para que o cliente receba futuras promoções e campanhas de marketing. Nome, número de telefone, endereço e e-mail são obrigatórios no cadastro, mas outras informações podem ser solicitadas, especialmente no caso de venda de prazo, como emprego atual, renda, tempo de residência e número de filhos. A empresa também possui um cadastro de cada loja, que hoje está na planilha do Excel. Há o nome de cada loja (um tipo de apelido que ajuda a identificar cada loja), o endereço, a região, cidade e estado. Cada loja tem um código. Esta planilha atualiza periodicamente o sistema de vendas da empresa, uma vez que cada venda registrada está associada a uma loja. Todas as lojas vendem todos os produtos, mas as lojas mantêm diferentes estoques, como forma de reduzir custos logísticos, ou seja, não despachar muitos produtos para lojas que tenham um volume menor de vendas, o que poderia exigir possível maior movimentação de produtos para lojas com maior volume. Cada loja possui um CEP cuidadosamente registrado, pois a empresa frequentemente implementa algoritmos de otimização logística usando análise de gráficos. Eles compararam um novo sistema recentemente, depois que ouviram que o sistema, que é baseado em Inteligência Artificial, poderia reduzir os custos de combustível em até 25% otimizando as rotas de caminhões de entrega! Em cada loja, os funcionários atendem clientes no showroom, onde os produtos são exibidos e também no telefone. Cada loja tem alguns vendedores, funcionários de limpeza e supervisores, trabalhando em 2 turnos. A empresa pretende começar a vender online, mas ainda não há previsão. Todos os colaboradores estão cadastrados no sistema interno da empresa, com número de registro, dados pessoais e especialidade. Uma venda é sempre feita por um vendedor, pois a empresa paga comissão pelas vendas feitas e o registro do responsável pela venda está vinculado a cada venda feita. O valor e a quantidade de cada venda estão presentes nos relatórios diários da empresa, que são utilizados para diferentes decisões durante a semana. Mas esses relatórios são manuais, normalmente criados no Excel, e muitas vezes apresentam erros. Cada diretor regional precisa conhecer as vendas por região, acompanhar o desempenho da sua loja e comparar com as demais regiões. A empresa faz muitas vendas de produtos como um único pacote ou combo, mas que são produtos diferentes. Por exemplo, um desktop pode ser vendido junto com um monitor, teclado e mouse. Embora seja um pacote, os produtos possuem SKUs diferentes, valores diferentes, e contribuem de forma diferente quando um desconto é concedido. A empresa calcula a porcentagem de cada produto em uma venda de pacotes ou combos. Os diretores acreditam que algumas categorias de produtos podem não ser lucrativas e gostariam de confirmar essas informações com o novo sistema de BI. Essas informações também serão úteis para a definição de estratégias de expansão e quais novas categorias de produtos devem ser consideradas.

## Starting the Project!

- Então vamos implementar um processo que algumas empresas pagam milhares de dólares para implementar e assim vou tentar mostrar o passo a passo. 
Vou tomar como base que você já implementou Oracle no SISTEMA OPERACIONAL LINUX (Redhat), se eu fizesse esse processo o projeto seria gigantesco e assumiria o foco da criação do DW.
 Como estou fazendo um projeto pessoal, só terei um Banco de Dados que é o Oracle, mas ele servirá a 3 propósitos diferentes teremos um esquema para a fonte de dados, um esquema para Área de Encenação e um esquema para a própria DW. Vamos começar a executar o sistema para a fonte de dados. Lembrando que em um projeto DW você não precisa criar a fonte que será o sistema de banco de dados RCP, sistema DE CRM, uma planilha Excel, um arquivo txt ou qualquer outra fonte. O que estou fazendo aqui é apenas simular o ambiente para que você possa ver como todo o processo funciona do início ao fim.

- Todo o Script será para uma melhor compreensão do projeto. Aqui haverá mais a parte para entender o que está sendo feito e também a linha do tempo de criação da DW!!! Vamos!


- Agora que entendemos a necessidade do cliente de se manter focado nisso!!! Objetividade e Simplicidade são uma Arte, então vamos praticar!
Tentarei ser objetivo mantendo as coisas simples por não inventar coisas desnecessárias apenas para aumentar o design para tornar as coisas mais interessantes ou parecer mais sábias do que eu realmente sou, embora essa não seja a regra em muitas situações. Vou me concentrar no cliente.
Para iniciar o projeto precisamos estudar o processo de implementação de uma solução de Business Intelligence porque o Data Warehouse é um componente de uma solução de BI

![1](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/1.png)
 
##O processo de implementação de BI tem 5 principais: 

- Fase 1> Definição de problemas
- Fase 2> Extração e Integração de Dados
- Fase 3> Armazenamento em DW
- Fase 4> Analysis
- Fase 5> Tomada de decisão

 
![2](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/2.png)
 

![3](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/3.png)
![4](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/4.png)

Na parte de Compreensão das Necessidades do Cliente, você precisa ter uma reunião com Diretores e Gerentes nas sessões de Captura de Conhecimento onde listaremos:

Qual é o ponto?
- Quem se beneficia deste Projeto?
- Quais são os problemas atuais?
- Quem será o patrocinador do projeto?
- Que orçamento está disponível?
- Quais recursos estão disponíveis?
- Quais são os relatórios atuais 
e também nesta etapa reuniões internas com diferentes atores-chave. Análise documental. Consulte os processos e métodos utilizados na empresa. Mapeamento de processos.


Nos Requisitos Reunindo a reunião estão com analistas com algumas pessoas que são os líderes de equipe aqueles Profissionais que tem o conhecimento da própria área de negócios listamos algumas dessas tarefas:


- Reuniões com profissionais do funcionalismo.

- Lista dos principais requisitos.

- Aceitar e concordar entre as principais partes interessadas.

- Critérios de aceitação.

- Detalhes sobre o funcionamento final da solução

- Remascans finais do projeto.

- Os requerimentos devem ser Smart (específico, mensurável, alcançável, relevante e baseado em tempo)

- Sessões de feedback.




## Na Arquitetura é preciso pessoas da área de TI para construir a solução que é tecnicamente viável nela, vamos listar alguns passos:


- Reuniões internas com a equipe de TI.

- Identificar fontes de dados.

- Identificar recursos computacionais.

- Sistemas legados.

- Integrações e Interfaces

- Fornecedores que impactam o projeto.

- Como os dados são armazenados
 
- Projeto da solução de ETL(Extrato, Transformação e Carga)

- Modelagem (Lógica, Dimensional e Física)


-Objetivo do projeto:
Este projeto faz parte do projeto BIAVANTE da XYZ Inc, com o objetivo de implementar um Data WareHouse para apoiar soluções de BI, análise e tomada de decisão.

- O Projeto inclui a entrega de dois produtos:


 -Data Warehouse
 
 -Interfaces ETL para integração com fontes de dados.
 

## Atenção !!!

- Nesses requisitos de coleta de processos e Entregas de Projetos, como o Buusiness Case, a Especificação Funcional do Cliente não é responsabilidade do Engenheiro de Dados, mas queria mostrar o início do projeto para ter uma direção e compreensão de como um projeto para implementar um Data Warehouse começa a partir daqui vamos focar na parte que é de responsabilidade de um Engenheiro de Dados!!!



## Arquitetura do Data Warehouse


![5](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/5.png)

A Área de Preparação é uma área intermediária usada para processamento de dados durante o ETL antes de ir para DW. Basicamente, os dados que entram na DW já precisam ser integrados e validados para uma área separada para fazer isso.

## Modelo Lógico e Modelo Dimensional

![6](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/6.png)


O modelo lógico básico para cada projeto de implementação da DW é necessário para entender todo o segmento e a necessidade da empresa.

![7](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/7.png)

Uma dica> mais completo seu modelo dimensional será mais fácil de criar seu modelo físico, então preste muita atenção a esta etapa. 
- Star Squema é um modelo mais consolidado e um modelo um pouco mais padronizado 
- Primeiro lá no modelo lógico não tivemos o DIMENSION TIME a hora que registra a data de venda eventualmente o ano, mês a mês do dia, mas isso é uma informação de vendas aqui no modelo Dimensional eu preciso controlar o tempo de uma forma um pouco mais detalhada porque nas especificações do cliente ficou claro que ele quer o relatório por dia para que eu já saiba que o meu nível de Granularidade é até o dia então eu preciso extrair a partir da data as informações do ano, mês, semana e dia.
- Outra característica que chama a atenção e não ter os Funcionários da Dimensão é porque não temos? Uma dica valiosa!!! Inicie o pequeno Data Warehouse e, em seguida, você irá incrementar o seu DW. À medida que você a empresa e a equipe de projetos aprendem você pode incorporar cada vez mais dimensões você pode modificar as dimensões adicionando mais atributos modificando seu modelo Star Squema para Floco de Neve o Data Warehouse é uma estrutura viva porque reflete o negócio da empresa se o negócio mudar o negócio tem novos requisitos é normal que ele também cresça. Voltando à questão da dimensão Funcionários é porque não tem essa necessidade de criar isso agora eu preciso da Dimensão do Cliente porque a venda é feita pelo cliente, Dimensão do Produto porque a venda e feita a partir do produto, eu preciso da dimensão do Locale porque os gestores e diretores querem relatórios de vendas por regiões e eu preciso de um Tempo de Dimensão para registrar cada um dos momentos que a venda é feito.
Vamos entender a necessidade do projeto Keys e as diferenças entre Chave Substituta x Chave Natural conceito muito importante ao trabalhar com Data Warehouse. É fundamental porque as chaves que determinarão as principais relações nada mais são do que chaves primárias, chaves estrangeiras e chave de substituto é importante para você entender como essas chaves serão implementadas porque todas as relações que você faz em seu modelo tudo o que você extrai informações da DW é feita as relações entre essas chaves, portanto, se isso não for bem implementado, é claro que vai gerar problemas na frente
- Vamos começar ID_CLIENTE lá no Modelo Lógico criamos a Entidade cliente colocamos lá o ID_CLIENTE e chamamos com Chave Primária porque lá no banco de dados Transacional lá na fonte de dados minha tabela de registro de clientes ela tem uma coluna que identifica exclusivamente cada cliente nesta coluna e chamou a chave principal apenas quando você trabalha com Data Warehouse eu realmente quero criar outro campo que ajude com relacionamentos somente com o modelo Dimensional que outro campo é chamado de Chave de Substituto que também é chamado de chave artificial a chave substituta não existe nem mais ela só existe no Data Warehouse será uma coluna que irá incrementar automaticamente para que você digite o primeiro registro será o número 1 na chave de substituto o segundo número 2 e etc... Se você analisar uma tabela de dimensões, verá uma chave substituta e também uma chave que é a Chave Natural não é mais a Chave Primária e por que fazemos isso? Por que agora ajuda saber de onde vem o registro do que exatamente foi aquele registro lá na fonte de dados eu tenho algumas vantagens em manter essas informações, no entanto, para criar as relações entre as tabelas no meu modelo Dimensional criamos uma chave primária artificial que é chamada de Chave de Substituto /\ Nosso Projeto Chave diz que em nosso DW não usaremos a chave principal da fonte como a chave principal a chave principal da fonte de dados se transformará em uma chave natural ou chave de negócios e lá em nossa DW será criada uma chave de substituto uma chave artificial. 
- Outra questão importante é se você olha para a mesa Fato_VENDA olha quem vem para a mesa de fatos exatamente as colunas das Chaves de Substituto 
- Lembre-se e compreenda Dados Normalizados x Dados Desnormalizados > lembrando que você tem o propósito de DW que é consultar e você perde desempenho com dados Normalizados e por que você quer desnormalizar. O objetivo da DW é consultar
- Padrões de nomeação > nome da dimensão, nome da coluna, eventualmente a documentação é importante para que você tenha algum tipo de Padrão. Geralmente as empresas já têm um documento falando sobre esses Padrões que você como Consultor precisa verificar com o negócio se há algum tipo de padrão sendo adotado se não há você criar e usar seu próprio padrão, mas é importante que haja algum padrão. (Sk > Chave de Substituto /\ NK> Chave Natural /\ NM> nome /\ DESCRIÇÃO DESC> /\ BY>Binário /\ NR>Number /\ FLAG> Holiday)
- Uma das dimensões do seu modelo Dimensional é bastante especial que é a TIME e estará em qualquer DW que sempre estará lá para apoiar exatamente uma das principais perguntas que você faz para o Data Warehouse, ou seja, quando essa venda ocorreu, quando essa "situação" ocorreu queremos que nosso Data Warehouse responda a várias perguntas que uma delas está exatamente relacionada com o momento. A dimensão do tempo não é carregada junto com o processo de ETL, ou seja, você não precisa acompanhar constantemente a atualização da sua dimensão temporal porque, na verdade, é uma estrutura virtualmente estática é uma dimensão que raramente mudará. Algumas características quando você constrói essa dimensão, veja que no primeiro temos uma chave de substituto ou é um ID único para cada uma das entradas e uma Coluna com data tipo Data e que data é essa? Cada uma das datas que representam cada uma das datas do período de trabalho dessa DW que é o ano da DW quem responde é o cliente 1 ano? Dois anos? Três anos? 20 anos? O cliente vai definir que período de dados ele quer analisar então assumindo que ele quer quatro anos eu vou ter datas de entrada para esses 4 anos para que eu possa criar as cruzes. 
- Preencha toda a documentação de todas as colunas sempre que estiver criando seu modelo Dimensional.
- Modelo Físico entende a criação das Tabelas a definição de armazenamento se vou ou não usar ou particionamento, ou seja, se eu vou ter uma tabela distribuída em mais de um arquivo físico ainda no modelo físico também definimos como será a indexação que temos para criar algum projeto de índice e tudo isso ocorre na modelagem física  



 - Esse é o nosso objetivo que queremos criar um modelo dimensional lá no DW Eu tenho a fonte de dados incluindo já extrair esses dados para a Área de Encenação, mas os dados estão em formato bruto é impuro eles requerem um processo de transformação para manipular esses dados que é o processo ETL 
ETL é como Raul Seixas disse > é uma metamorfose ambulante está sempre em processo de mudança. Precisamos ter as habilidades necessárias para reconhecer tanto a análise técnica quanto as questões envolvidas nas regras do negócio.

- /\ A tabela 1 que vamos carregar é da dimensão Tempo porque os dados da dimensão do tempo não vêm no ETL ou geralmente não vêm. Criando uma operação específica para carregar a Dimensão do Tempo lembrando que dificilmente mudará ou mudará muito pouco na vida do seu DW não precisamos incluir isso no ETL mas eu REPITO dependendo do Projeto não há uma única regra não há apenas uma norma sempre dependerá do projeto na maioria dos casos a dimensão Tempo que varia muito pouco para que possamos gerar os dados que serão carregados dentro desta TABELA, quais são esses dados? Dados para data em um determinado período 

Então, na área de encenação, vamos preparar os dados e, em seguida, carregar em dw.
- Não usaremos o processo ETL para a dimensão de tempo que faremos manualmente no momento em que criaremos o DW.
Na Área de Preparação vamos trabalhar a dimensão Cliente, Locale e Produto vamos coletar os dados da fonte para verificar se precisamos de algum tipo de transformação se eu tiver que limpar os dados e já estou preparando os dados para carregamento posterior. Além disso, vamos preparar uma tabela de vendas eu não vou preparar o fato ok tabela eu vou preparar a tabela de vendas porque pelo que aprendemos com o nosso projeto os dados de vendas eles estão espalhados por mais de uma tabela então eu vou agrupar esses dados eu vou reorganizar colocar em uma única estrutura de tabela e também já preparar para carga posterior no FACT TABELA ,  basicamente vamos preparar dados 4 tabelas. 3 dimensões e para a tabela de fatos e a dimensão do tempo que faremos na DW.
 
 
 ## PROJECT END /\ Agora são melhorias contínuas!!! 


- Agora, com a DW pronta, precisamos fazer melhorias em nossa DW
- Propositalmente deixado lá na fonte de dados do banco de dados transacional no usuário de origem uma categoria de hierarquia que não foi bem implementada


![8](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/8.png)

Você pode ver repetindo as categorias e isso não pode acontecer no banco de dados transacional na fonte porque os dados precisam ser NORMALIZADOS.... Os dados não são normalizados lá na DW, mas na FONTE no banco de dados transacional precisa ser normalizado.

## Implementando hierarquia na fonte do banco de dados

Implementaremos corretamente a Hierarquia e teremos que alterar todo o processo de ETL até recarregarmos nossa TABELA DE FATOS
Primeiro vamos entender o nível de hierarquia

![9](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/9.png)

É categoria de acordo com o que a empresa vende ou fornece produto ou Serviço, abaixo desta categoria temos a categoria filha, pessoal e empresarial /\ notebooks para uso pessoal e para uso de empresa de serviços. E então terei cada produto associado ao nível mais baixo da minha Hierarquia o nome do produto Notebook MSI é um grão, ou seja, é o nível mais baixo de Granularidade que podemos ter níveis do tamanho que queremos depende do que a empresa implementa. 
As vendas não estão associadas à Categoria, o que você vende é o produto que temos aqui é a Hierarquia para que possamos categorizar esses produtos porque então eu quero emitir um relatório que foram as categorias que mais venderam. Quais categorias mais vendidas por região. Quais categorias mais vendidas pelo tipo de cliente e etc...
O produto não entra na tabela categoria porque temos uma tabela só para o produto depois que eu precisar entrar na tabela do produto e atualizar a categoria.
- Acabamos de implementar nossa Hierarquia de Categorias ver que temos 1 coluna com Todas as IDs 2 Coluna com todas as categorias sem repetição e os respectivos IDs da Categoria Pai

![10](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/10.png)

Agora, como eu disse o acima vamos atualizar a tabela do Produto. Mudamos o ID_CATEGORIA e isso não reflete mais na tabela do produto, só podemos fazer isso porque desativamos as restrições que são a restrição que mantém a integridade referencial para que desabilitemos restrições, comandamos > 
ALTERAR TB_PRODUTO ALTERAR A RESTRIÇÃO TB_PRODUTO_FK1 DESABILITAR; Usamos este comando antes de executar todo o processo. Assim, posso modificar a tabela Categoria, mas se agora eu não atualizar a tabela Do produto ficará tudo errado./\ MODIFICADO AGORA ATIVO PARA FAZER O comando QUERY >
ALTERAR TB_PRODUTO A RESTRIÇÃO DE MODIFICAÇÃO TB_PRODUTO_FK1 HABILITAR;
É IMPORTANTE LEMBRAR DE LIGAR E DESLIGAR AS RESTRIÇÕES ESTE É UM PROCESSO QUE FAZEMOS MUITO DURANTE O PROCESSO ETL ESPECIALMENTE ANTES DE CARREGAR OS DADOS NORMALMENTE VOCÊ DESATIVAR OS ÍNDICES E A RESTRIÇÃO À MEDIDA QUE LÁ DE SUA DW EXECUTA A CARGA APÓS ATIVO NOVAMENTE SE VOCÊ NÃO ATIVAR ELE TERÁ PROBLEMA DEPOIS EM INTEGRIDADE REFERENCIAL.

## Melhorando o desempenho do VIEW

- Podemos ter várias visualizações em nosso banco de dados, podemos criar uma visão, por exemplo, com uma regra de negócios ou seja, incluo uma cláusula WERE esta visão só poderia ter vendas a partir de 2018 /\ 2019 etc... Podemos criar uma Visão para cada mês do ano podemos criar uma exibição para categoria por exemplo e então eu vou criar as visualizações e então eu alimento lá, por exemplo, quando eu tenho o uso de uma ferramenta de BI em vez da ferramenta DE BI usando consulta faz uma consulta direta no VIEW é uma boa prática é muito mais seguro porque se eu precisar mudar a consulta eu altero a consulta dentro do ver, mas meu sistema de BI estará apontando para o VIEW Eu não preciso mudar nada no sistema eu apenas alterar a visão no banco de dados. 
- Há apenas um pequeno problema aqui quando usamos um VIEW na prática o que o banco de dados faz é executar o CONSULTA isso aqui é bom para o humano ele não precisa saber que a CONSULTA é simples para dar uma seleção na exibição, mas internamente o banco de dados sabe que este é um VIEW e executa a consulta é claro e isso tem um custo no banco de dados vamos visualizar qual é esse custo. (EXPLIQUE O PLANO DE CONSULTA PARA BAIXO)


![11](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/11.png)


Como o otimizador de banco de dados executou essa consulta? Como segue! Ele fez a Declaração Select /\ ORDER BY /\ usou o HASH para o grupo BY e se juntou e fez uma TABELA ACESS COMPLETA ou seja, ele nem sequer usou um índice.
- Claro que no meu exemplo isso não faz diferença porque temos poucas linhas, mas se em vez de 7 linhas eu tivesse 7 milhões de linhas isso faria toda a diferença a consulta ficaria muito lenta para criar um VIEW é uma boa alternativa, mas não resolve muito do problema de desempenho porque eu ainda estou executando a consulta da mesma maneira. Então, para resolver isso eu criei um VIEWs materializado onde eu vou armazenar no banco de dados o resultado de uma consulta em execução. O que eu quero é basicamente toda vez que eu executar o VIEW eu não quero executar consulta o que eu quero é olhar para os dados já armazenados no DW que CONSULTA que faz parte dessa VISÃO vamos executar lá e escrever os registros para um banco de dados quando eu chamar a visualização novamente eu vou estar com outro plano de execução muito mais rápido 
Observe que ele fez um ACESS COMPLETO apenas em uma tabela que foi o que criamos o View materializado se você ver a diferença do plano de execução lá da nossa Consulta ele fez o SCAN TABELA em 3 tabelas diferentes agora não eu varrer apenas uma única tabela de tempo de execução é infinitamente menor e eu posso otimizar consideravelmente o desempenho do banco de dados também é útil quando você quiser se conectar em banco de dados remoto, por exemplo, você tem um DW em um servidor na unidade de São Paulo e o analista está no Rio de Janeiro como você vai traficar os dados?  Posso criar uma Visão Materializada que ela vai consultar do Rio para São Paulo, ela vai para São Paulo consultar o banco de dados traz os dados é claro que isso vai demorar um pouco eu posso criar a Visão Materializada à noite e no dia seguinte os analistas do Rio de Janeiro vão trabalhar eles vão consultar os dados localmente do Rio de Janeiro porque nós criamos a materialização no rio não precisa para ficar gastando largura de banda para realizar consulta entre Rio e São Paulo Criei um Link base de dados entre os dois bancos Criei uma visão materializada no Rio apontando para os dados de São Paulo eu faço esse processo na noite seguinte os analistas ficam felizes com a vida trabalhando com Alto Desempenho. E se eu inserir mais dados na tabela de fatos? Com certeza o View materializado ficará desatualizado porque eu corri a Consulta apenas uma vez. Para isso, podemos fazer um refrash do comando Vista Materializada >
EXEC DBMS_MVIEW.refresh ('mv_vendas_2018');
-Domingo a DBA do Rio cria o View Materializado durante a segunda-feira para trabalhar normalmente, consultando os dados locais quando é na noite de segunda-feira o DBA do Rio agendar esta ATUALIZAÇÃO para que ele atualize a visão materializada da noite com os novos dados que foram carregados na tabela de fatos na manhã de terça-feira os analistas continuam trabalhando com a visão feliz materializada da vida com Alto Desempenho. Um ambiente profissional


![12](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/12.png)



## Uma coisa importante é definir a estratégia de atualização




![13](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/13.png)


Algumas empresas excluem todo o DW e atualizem com os novos dados que você atualiza o DW inteiro (depende de vários fatores, incluindo o tamanho do DW)
-Outras empresas atualizam o DW, ou seja, só aplica as alterações, uma vez que a última carga (dependendo do tamanho do DW é uma abordagem)
-E você pode encontrar uma maneira de detectar as alterações que ocorreram no sistema de origem entre uma carga e outra e aplicar apenas essas alterações isso reduzirá muito a sua janela de atualização.

![14](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/14.png)


![15](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/15.png)

Dependendo do banco de dados, podemos usar a tecnologia Golden Gate.
No meu caso de banco de dados oracle podemos usar os Registros de Arquivos que tem um conceito de Data Guard você pode criar uma espécie de banco de dados de cópias e todos os registros de banco de dados os logs (é que contém todos os comandos DML que são aplicados em todas as tabelas são os Logs do banco de dados que você pode pegar os arquivos que exatamente são os resultados desses Logs movê-lo para outro banco de dados e aplicar o arquivos que são basicamente aplicar os aplicativos DML, que outro banco de dados parece ser uma cópia) você pode aplicar uma solução semelhante no DW e temos o conceito golden gate que é trabalhar com dados de Streaming você pode configurar golden gate para olhar para sua fonte seja qual for outra não a captura do Banco Relacional apenas as alterações e aplicar ao seu sistema de Destino.

![16](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/16.png)


Aqui podemos fazer várias partições para cada mês e quando você atualizar os dados que você pode atualizar por partição não precisa atualizar todo o DW isso reduz consideravelmente o volume de dados e acelera o tempo de carga e você pode usar essa opção e, em seguida, se necessário poderia limpar os dados por partição assumindo que uma empresa queria, por exemplo, atualizar os dados de junho eu posso limpar apenas as partições dos dados de junho e carga apenas sobre essa partição. Se a partição que são arquivos físicos tiver no Disk diferente o fato de carregar uma partição não afetaria o desempenho de consulta dos dados em outra partição, ou seja, escolheria a melhor estratégia de acordo com o que a empresa tem à sua disposição lembrando que o Oracle Particion, que é a funcionalidade do Oracle para particionamento, tem uma licença separada.

![17](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/17.png)


No caso de uma empresa ter o nível de granularidade de 5 anos e passa 6 anos precisamos fazer uma estratégia para essa demanda. O que as empresas fazem é criar uma cópia da dimensão, mantendo apenas uma cópia daquele ano que não está no período de 5 anos então você tem no DW apenas os 5 anos, mas se necessário os dados históricos estão ali em mãos em disposição você cria uma cópia da Dimensão e pronto e inclusive você pode utilizar essa cópia em relatórios mesmo você pode criar os relatórios lá na ferramenta de BI apontando para essa dimensão de históricos. 

![18](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/18.png)




![19](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/19.png)


# 10 Erros comuns a serem evitados em Projetos de Data Warehouse.

![20](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/20.png)
