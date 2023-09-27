# **OBJETIVO**

  A partir de dados de duas das maiores empresas do mundo, analisar os seguintes questionamentos: 

1. Qual o **preço máximo** de cada ação, ano a ano, desde o seu IPO? 
2. Qual a **máxima variação (percentual) positiva** diária da ação até o ano de 2022?
3. Qual a **máxima variação (percentual) negativa** diária da ação até o ano de 2022?
4. Qual a **valorização (percentual)** da ação desde o seu IPO na bolsa até o fim de 2022?
5. Quantos dólares uma pessoa que investiu $1000 na época, teria caso carregasse a ação até o fim de 2022?
6. Qual a **ocorrência (percentual) de dias** positivos, negativos e neutros das ações até o fim de 2022?
7. Qual a **maior valorização (percentual)** das ações durante o ano (1º dia até o último dia do ano)?

# **DETALHAMENTO**


*Busca pelos dados*

AMAZON:
https://www.kaggle.com/datasets/guillemservera/amzn-stock-data?select=amzn_split_adjusted.csv

APPLE:
https://www.kaggle.com/datasets/guillemservera/aapl-stock-data?select=aapl_split_adjusted.csv

# **COLETA**

Download de dados para o desktop e posteriormente upload para a o storage/container criado no Azure, conforme indicações abaixo.  

# **MODELAGEM** 

# **CARGA**

O ETL foi realizado pelo Data Factory, com as seguintes etapas percorridas: 

1.	Criação de datasets, realizando upload dos arquivos que se encontram no container.
![Carga1-DataSet](https://github.com/maghinha/MVP/blob/main/Carga%201%20(Dataset).png?raw=true)

![Carga2-DataSet1](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset1).png?raw=true)

![Carga2-DataSet2](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset2).png?raw=true)

![Coleta1](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset2).png?raw=true)

![Coleta2](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset2).png?raw=true)

![Dados Amazon](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset2).png?raw=true)

![Dados Apple](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset2).png?raw=true)

![Dados carregados para Data Studio](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset2).png?raw=true)


*Dataflow1:*


*Select:*


*Join:*


*Skin:*


*Dataflow2:*


*Dataflow1:*


*Select:*


*Join:*


*Skin:*


3.	Criação do pipeline para inserção dos dataflows

Inserção de Dataflows no pipeline


Dados carregados para o Data Studio: 


Dados carregados para o Power BI, com conexão direta no banco:


Dados Apple:


Dados Amazon:



TESTE12323132:  ![TESTE 123 ](https://github.com/maghinha/MVP/blob/main/x.png?raw=true)https://github.com/maghinha/MVP/blob/main/x.png?raw=true)
