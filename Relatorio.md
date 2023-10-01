# **OBJETIVO**

  A partir de dados de duas das maiores empresas do mundo (APPLE e AMAZON), analisar os seguintes questionamentos: 

1. Qual o **preço de fechamento** de cada ação, ano a ano, desde o seu IPO? 
2. Qual a **máxima variação (percentual) positiva** diária da ação até o ano de 2022?
3. Qual a **máxima variação (percentual) negativa** diária da ação até o ano de 2022?
4. Qual a **valorização (percentual)** da ação desde o seu IPO (lançamento da ação na bolsa) até o fim de 2022?
5. Quantos dólares uma pessoa que investiu $1000 no IPO (lançamento da ação na bolsa), teria caso carregasse a ação até o fim de 2022?
6. Qual a **ocorrência (percentual) de dias** positivos, negativos e neutros das ações até o fim de 2022?
7. Qual a **maior valorização (percentual)** das ações durante o ano (1º dia até o último dia do ano)?

# **DETALHAMENTO**


*Busca pelos dados*

**AMAZON:**
https://www.kaggle.com/datasets/guillemservera/amzn-stock-data?select=amzn_split_adjusted.csv

**APPLE:**
https://www.kaggle.com/datasets/guillemservera/aapl-stock-data?select=aapl_split_adjusted.csv

# **COLETA**

Download de dados para o desktop e posteriormente upload para a o storage/container criado no Azure. 

# **MODELAGEM** 

#### *Amazon:*

![Dataflow3 (Primeir Dataflow SELECT)](https://github.com/maghinha/MVP/blob/main/Dataflow%203%20(Primeiro%20Dataflow%20SELECT).png?raw=true)

![Dataflow3 (Primeir Dataflow SELECT2)](https://github.com/maghinha/MVP/blob/main/DataFlow1%20(Select%202).png?raw=true)




#### *Apple:*

![Dataflow7 (Segundo Dataflow SELECT)](https://github.com/maghinha/MVP/blob/main/Dataflow%207%20(SEGUNDO%20Dataflow%20SELECT).png?raw=true)

![Dataflow8 (Segundo Dataflow SELECT2)](https://github.com/maghinha/MVP/blob/main/Dataflow%208%20(SEGUNDO%20Dataflow%20SELECT2).png?raw=true)

# **CARGA**

O ETL foi realizado pelo Data Factory, com as seguintes etapas percorridas: 

### 1.	Criação de datasets, realizando upload dos arquivos que se encontram no container.
![Carga1-DataSet](https://github.com/maghinha/MVP/blob/main/Carga%201%20(Dataset).png?raw=true)

![Carga2-DataSet1](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset1).png?raw=true)

![Carga2-DataSet2](https://github.com/maghinha/MVP/blob/main/Carga%202%20(Dataset2).png?raw=true)

![Coleta1](https://github.com/maghinha/MVP/blob/main/Coleta%202%20(Storage).png?raw=true)

### 2.	Criação dos dataflows (foi criado 1 para cada arquivo)

#### *Dataflow1:*

![Dataflow2 (Primeirodtflow)](https://github.com/maghinha/MVP/blob/main/Dataflow%202%20(Primeiro%20Dataflow).png?raw=true)


#### *Select:*

![Dataflow3 (Primeir Dataflow SELECT)](https://github.com/maghinha/MVP/blob/main/Dataflow%203%20(Primeiro%20Dataflow%20SELECT).png?raw=true)

![Dataflow3 (Primeir Dataflow SELECT2)](https://github.com/maghinha/MVP/blob/main/DataFlow1%20(Select%202).png?raw=true)


#### *Join:*

![Dataflow4 (Primeiro Dataflow Join)](https://github.com/maghinha/MVP/blob/main/Dataflow%204%20(Primeiro%20Dataflow%20JOIN).png?raw=true)


#### *Skin:*

![Dataflow5 (Primeiro Dataflow skin)](https://github.com/maghinha/MVP/blob/main/Dataflow%205%20(Primeiro%20Dataflow%20SKIN).png?raw=true)

#### *Dataflow2:*

![Dataflow6 (Segundo Dataflow)](https://github.com/maghinha/MVP/blob/main/Dataflow%206%20(SEGUNDO%20Dataflow).png?raw=true)

#### *Select:*

![Dataflow7 (Segundo Dataflow SELECT)](https://github.com/maghinha/MVP/blob/main/Dataflow%207%20(SEGUNDO%20Dataflow%20SELECT).png?raw=true)

![Dataflow8 (Segundo Dataflow SELECT2)](https://github.com/maghinha/MVP/blob/main/Dataflow%208%20(SEGUNDO%20Dataflow%20SELECT2).png?raw=true)

#### *Join:*

![Dataflow9 (Segundo Dataflow JOIN)](https://github.com/maghinha/MVP/blob/main/Dataflow%209%20(SEGUNDO%20Dataflow%20JOIN).png?raw=true)

#### *Skin:*

![Dataflow10 (Segundo Dataflow SKIN)](https://github.com/maghinha/MVP/blob/main/Dataflow%2010%20(SEGUNDO%20Dataflow%20skin).png?raw=true)

### 3.	Criação do pipeline para inserção dos dataflows 

![PIPELINE 1 INSERÇÃO DATA FLOW](https://github.com/maghinha/MVP/blob/main/PIPELINE%201.png?raw=true)

![PIPELINE 2 INSERÇÃO DATA FLOW](https://github.com/maghinha/MVP/blob/main/PIPELINE%202%20(INSER%C3%87%C3%83O%20DATAFLOWS).png?raw=true)

### 4. Utilização do Data Studio 

![Dados carregados para Data Studio](https://github.com/maghinha/MVP/blob/main/Dados%20Carregados%20para%20Data%20Studio.png?raw=true)

### 5. Dados carregados para o Power BI, com conexão direta no banco

![Dados carregados para o PBI ](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI.png?raw=true)



![Dados carregados para o PBI 2](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI%202.png?raw=true)



![Dados carregados para o PBI 3](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI%203.png?raw=true)



![Dados carregados para o PBI 4](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI%204.png?raw=true)

### Como os dados das tabelas possuem as mesmas colunas, foram "acrescentadas" as tabelas no power query, uma a outra para facilitar posteriormente a visualização interativa no dashboard. 
### *Essa ação equivale ao "UNION ALL" no SQL.*

![Dados carregados para o PBI 5](https://github.com/maghinha/MVP/blob/main/Dados%20carregados%20para%20o%20PBI%205%20(UNION%20ALL).png?raw=true)

# **ANÁLISE**

### (A). Qualidade de dados

Os dados já eram tratados, então não tive problemas significativos quanto a qualidade destes dados. Porém, não necessariamente existiam registro de todos os dias do ano para as ações (em ambas as tabelas), podendo ser inclusive uma possibilidade, o fato de o mercado não abrir em determinado dia. Como uma das perguntas a serem respondidas, eu precisaria do primeiro dia do ano de cada ano e do último dia também (para saber preço inicial da ação no ano e preço da ação no último dia do ano, por exemplo), foi necessário fazer um tratamento nas bases dentro do PowerBi para identificar quais foram os primeiros e últimos registros de data de cada ano durante o período em análise.
Seguindo com o tratamento desta forma, foi possível encontrar as respostas que gostaria para o MVP.  


O ano mínimo esperado para análise seria o ano de 1980, ano início da APPLE na bolsa, e o ano máximo 2022. Conforme texto descritivo no dashboard, os dados são considerados apenas até o ano de 2022.
Na coluna de "Date", conforme esperado, foram encontradas apenas informações de datas. 
Na coluna de valores que foram utilizados na estruturação dos dados (preço de abertura, preço de fechamento, preço máximo, preço mínimo) não foram encontrados valores nulos, apenas números. 

### (B). Solução do problema

*Todas as respostas se encontram no dashboard, conforme evidências. Nas perguntas, trarei a informação de forma mais objetiva.*

## 1. Qual o **preço de fechamento** de cada ação, ano a ano, desde o seu IPO?

![image](https://github.com/maghinha/MVP/blob/main/EvolucaoPreco_APPLE.png) 


![image](https://github.com/maghinha/MVP/blob/main/EvolucaoPreco_Amazon.png)  

 
## 2. Qual a **máxima variação (percentual) positiva** diária da ação até o ano de 2022?

### **AMAZON:** 

24,35%

### **APPLE:** 

20,57%


## 3. Qual a **máxima variação (percentual) negativa** diária da ação até o ano de 2022?

### **AMAZON:** 

-28,89%

### **APPLE:** 

-19,23%

## 4. Qual a **valorização (percentual)** da ação desde o seu IPO (lançamento da ação na bolsa) até o fim de 2022?

### **AMAZON:** 

68.908,9%

### **APPLE:** 

101.270,5%

## 5. Quantos dólares uma pessoa que investiu $1000 no IPO (lançamento da ação na bolsa), teria caso carregasse a ação até o fim de 2022?
**Ações da APPLE:**  Levando em consideração que $1.000,00 poderia comprar aproximadamente 7.794 ações, essa pessoa teria aproximadamente $1.012.704,00. 


**Ações da AMAZON:**  Levando em consideração que $1.000,00 poderia comprar aproximadamente 8.203 ações, essa pessoa teria aproximadamente $689.089,00. 



## 6. Qual a **ocorrência (percentual) de dias** positivos, negativos e neutros das ações até o fim de 2022?

Além da resposta no dashboard do PowerBi, com as medidas calculadas e transformações, também feito via SQL:

![image](https://github.com/maghinha/MVP/blob/main/C%C3%B3digoSQL1.png)

![image](https://github.com/maghinha/MVP/blob/main/C%C3%B3digoSQL2.png)



**AMAZON**



DIAS POSITIVOS: 49,62%



DIAS NEGATIVOS: 49,87%



DIAS NEUTROS: 0,51%




**APPLE**



DIAS POSITIVOS: 47,59%



DIAS NEGATIVOS: 45,55%



DIAS NEUTROS: 6,86%

## 7. Qual a **maior valorização (percentual)** das ações durante o ano (1º dia até o último dia do ano)?

**AMAZON:** 

970,8%

**APPLE:** 

200,3%




## DISCUSSÃO DE RESULTADOS

Nota-se que ambas as ações entregaram/entregam retornos consistentes e relevantes aos seus investidores de longo prazo, que não se desesperaram/desesperam em momentos de desvalorização da ação. Por outro lado, investidores impacientes podem não ter tido ganhos significantes, de modo que tenham vendido a ação em momentos de baixa do mercado.  Por mais que essas ações apresentem oscilações de preço, como demonstrado nos gráficos históricos, a valorização no longo prazo é uma realidade. 


Ambas possuem preços máximos históricos parecidos, sendo **APPLE: $182,63** vs **AMAZON $187,2**. 

Historicamente, a ocorrência de **dias sem oscilação de preço das ações** da APPLE foram maiores, com forte influência no indicador, dos anos anteriores a 2000 *(6,86% x 0,51%)*.
Desconsiderando anos anteriores a 2000 da análise, as ações da APPLE ficariam **0,28%** contra **0,40%** da AMAZON, de dias sem oscilação de preço, demonstrando que em um passado recente a ocorrência de dias neutros são mais parecidas.

Quando comparadas, não foi encontrada uma correlação forte de desvalorização das ações durante o ano. Em outras palavras, anos que a Apple teve uma desvalorização em suas ações (preço de abertura da ação no ano menor que o preço de fechamento da ação no ano), não necessariamente as ações da Amazon tiveram o mesmo comportamento e vice-versa.

*OBS: A análise de correlação dos preços, especificamente, foi feita a apenas partir do momento em que as duas ações estavam listadas simultaneamente na bolsa.*

Visualmente organizado em uma simples tabela: 

**Anos negativos APPLE:**


![image](https://github.com/maghinha/MVP/blob/main/AnosNegativosAPPLE.png)


**Anos negativos AMAZON:**


![image](https://github.com/maghinha/MVP/blob/main/AnosNegativosAMAZON.png)



*OBS: Não consegui subir um vídeo explicativo do Dashboard, portanto estarei anexando no envio do trabalho do portal, além do link abaixo.*
(https://github.com/maghinha/MVP/blob/main/Dash_explica.xspf)

### Dados Apple:

![Dados Apple](https://github.com/maghinha/MVP/blob/main/Dados%20Apple.png?raw=true)

### Dados Amazon:

![Dados Amazon](https://github.com/maghinha/MVP/blob/main/Dados%20Amazon.png?raw=true)

# AUTOAVALIAÇÃO

Foi um desafio grande para mim esse projeto, pois nunca anteriormente havia trabalhado com os dados na nuvem e tive a possibilidade de aprender, observando as aulas práticas do professor Vitor, como balizador. Entendo que consegui atingir o objetivo do trabalho, conforme eu esperava, respondendo todos os questionamentos que eu tive. Por ter mais facilidade e intimidade com o PowerBi (PowerQuery e Dax) eu optei por fazer alguns tratamentos dos dados pela ferramenta para poder ganhar tempo (já que não tive tanta facilidade assim com a nuvem e acabei demorando um pouco). Minha intenção era também fazer as respostas com a linguagem SQL, das perguntas, apenas para poder deixar ainda mais completo, mas por falta de tempo não prossegui com todas as soluções por lá, mas respondi o questionamento da ocorrência de dias positivos, negativos e neutros. Conforme citado anteriormente, encontrei inicialmente como um problema, a falta de inconsistência na base para os primeiros e últimos dias dos anos (o que afetaria diretamente nos questionamentos que eu estava buscando responder) mas consegui solucionar internamente pelo PowerQuery e cheguei no objetivo.  De forma geral, estou bem satisfeito com o  resultado, por ter conseguido responder as perguntas do objetivo do trabalho e principalmente por ter aprendido novas ferramentas e conseguido executar com sucesso o que foi passado nas aulas. Entendo que abriu um horizonte de ideias e possibildiades na minha cabeça para futuros trabalhos e sigo cada vez mais animado para novos aprendizados. 

