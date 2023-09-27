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

![Coleta1](https://github.com/maghinha/MVP/blob/main/Coleta%202%20(Storage).png?raw=true)

![Coleta2]()

![Fluxo de dados 1]()


*Dataflow1:*

![Dataflow2 (Primeirodtflow)](https://github.com/maghinha/MVP/blob/main/Dataflow%202%20(Primeiro%20Dataflow).png?raw=true)


*Select:*

![Dataflow3 (Primeir Dataflow SELECT)](https://github.com/maghinha/MVP/blob/main/Dataflow%203%20(Primeiro%20Dataflow%20SELECT).png?raw=true)


*Join:*

![Dataflow4 (Primeiro Dataflow Join)](https://github.com/maghinha/MVP/blob/main/Dataflow%204%20(Primeiro%20Dataflow%20JOIN).png?raw=true)


*Skin:*

![Dataflow5 (Primeiro Dataflow skin)](https://github.com/maghinha/MVP/blob/main/Dataflow%205%20(Primeiro%20Dataflow%20SKIN).png?raw=true)

*Dataflow2:*

![Dataflow6 (Segundo Dataflow)](https://github.com/maghinha/MVP/blob/main/Dataflow%206%20(SEGUNDO%20Dataflow).png?raw=true)

*Select:*

![Dataflow7 (Segundo Dataflow SELECT)](https://github.com/maghinha/MVP/blob/main/Dataflow%207%20(SEGUNDO%20Dataflow%20SELECT).png?raw=true)

![Dataflow8 (Segundo Dataflow SELECT2)](https://github.com/maghinha/MVP/blob/main/Dataflow%208%20(SEGUNDO%20Dataflow%20SELECT2).png?raw=true)

*Join:*

![Dataflow9 (Segundo Dataflow JOIN)](https://github.com/maghinha/MVP/blob/main/Dataflow%209%20(SEGUNDO%20Dataflow%20JOIN).png?raw=true)

*Skin:*

![Dataflow10 (Segundo Dataflow SKIN)](https://github.com/maghinha/MVP/blob/main/Dataflow%2010%20(SEGUNDO%20Dataflow%20skin).png?raw=true)

3.	Criação do pipeline para inserção dos dataflows

Inserção de Dataflows no pipeline

![PIPELINE 1 INSERÇÃO DATA FLOW](https://github.com/maghinha/MVP/blob/main/PIPELINE%201.png?raw=true)

![PIPELINE 2 INSERÇÃO DATA FLOW](https://github.com/maghinha/MVP/blob/main/PIPELINE%202%20(INSER%C3%87%C3%83O%20DATAFLOWS).png?raw=true)

Dados carregados para o Data Studio: 

![Dados carregados para Data Studio](https://github.com/maghinha/MVP/blob/main/Dados%20Carregados%20para%20Data%20Studio.png?raw=true)

Dados carregados para o Power BI, com conexão direta no banco:

![Dados carregados para o PBI ](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI.png?raw=true)

![Dados carregados para o PBI 2](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI%202.png?raw=true)

![Dados carregados para o PBI 3](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI%203.png?raw=true)

![Dados carregados para o PBI 4](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI%204.png?raw=true)

![Dados carregados para o PBI 5](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI%205%20(UNION%20ALL).png?
raw=true)

Dados Apple:

![Dados Apple](https://github.com/maghinha/MVP/blob/main/Dados%20Apple.png?raw=true)

Dados Amazon:

![Dados Amazon](https://github.com/maghinha/MVP/blob/main/Dados%20Amazon.png?raw=true)
