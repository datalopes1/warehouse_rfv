
# 🏪Análise RFV (Recência Frequência Valor) - Retail Sales Data

Neste projeto será realizada uma análise do tipo RFV (Recência, Frequência e Valor) com dados que encontrei neste video no Youtube do canal [Jie Jenn](https://www.youtube.com/watch?v=9wxWrERZvss).

### 🛠️ Ferramentas utilizadas
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)

## 1.1. Os dados, o problema e os objetivos

A análise RFV é uma técnica de segmentação de clientes muito utilizada em marketing e gestão de relacionamento com clientes (CRM). Ele tem base em três métricas:

- Recência (Recency): O tempo decorrido entre a última compra ou interação de um cliente com a empresa. Clientes mais recentes tem tendência de fazer mais compras do que clientes que não interagem a muito tempo.
- Frequência (Frequency): É o número total de compras ou interações do cliente com a empresa. Clientes com maior frequência de compra, representam aqueles que são fiéis a empresa.
- Valor monetário (Monetary value): Refere-se ao gasto total ou a média de gastos do cliente em suas compras na empresa. Clientes que tem maior média de valores gastos na empresa contribuem de maneira significante com os lucros dela.

Combinando essas três métricas é possível de várias maneiras segmentar os clientes e partir disso criar campanhas de marketing, estratégias de relacionamento e campanhas focada em cada segmento de cliente especifico. 

### Estrutura do dataset
Os dados são de uma rede varejista fictícia que faz entregas internacionais de componentes. As colunas estão organizadas dessa forma:

| Coluna | Descrição|
|--------|----------|
|**OrderNumber**| ID do pedido|
|**Sales Channel**| Canal de vendas do pedido|
|**WarehouseCode**| ID do armazém do pedido|
|**ProcuredDate**|Data de reserva do pedido|
|**OrderDate**|Data da realizaçãod do pedido|
|**ShipDate**|Data de envio|
|**DeliveryDate**|Data de entrega|
|**CurrencyCode**|Moeda utilizada na transação|
|**_SalesTeamID**|ID do time de vendas|
|**_CustomerID**|ID do cliente|
|**_StoreID**|ID da loja|
|**_ProductID**|ID do produto|
|**Order Quantity**|Quantidade de itens no pedido|
|**Discount Applied**|Desconto aplicado na compra|
|**Unit Price**|Preço unitário do produto|
|**Unit Cost**|Custo unitário|

### Objetivos

Com este conjunto de dados em mãos meu objetivo será realizar a análise RFV, com uso do KMeans, e identificar uma segmentação de clientes para ser trabalhada pelo setor de marketing da empresa. 

## 1.2. Importação das bibliotecas e carregamento dos dados
A bibliotecas utilizadas foram o pandas, numpy, datetime, os, matplotlib, seaborn e warnings.

# 🧱2. Entendendo os dados 
##  2.1. Estrutura do dataframe
Aqui busquei através do métodos shape, head(), tail(), e info() para entender a estrutura dos dados. 
## 2.2. Breve conclusões antes de partir para os próximos passos 

- Vou usar somente algumas colunas, portando vou criar um novo dataframe somente com elas;
- Será necessário criar uma coluna para contabilizar o total de receita por pedido;
- Será necessário mudar a coluna "OrderDate" para o dtype datetime;
- O dataframe não possui dados nulos.

# 🧹3. Limpeza e manipulação dos dados
## 3.1. Verificação de nulos e duplicados
Verificação através dos métodos isna() e duplicated(). 
## 3.2. Manipulação dos dados e colunas
Foram feitos os processos de mudar o dtype de "OrderDate", criar um dataframe somente com as colunas que serão utilizadas, e a criação da coluna "Revenue".

# 🤖4. Aplicação do KMeans
## 4.1. Ajuste dos dados
Nessa etapa foram feitos ajustes para criar um dataframe com base no RFV antes de aplicar a clusterização com KMeans. Aqui foram feitas operações de agregação e de merge, para criar o dataframe com Colunas de "_CustomerID", "Recência", "Frequência" e "Valor".
## 4.2. Pré-processamento dos dados e definição do número de clusters
Aqui foi utilizado o StandardScaler() e definido o número de Clusters através do método do "cotovelo". O número de Clusters definido é 4. 
## 4.3. Aplicando a clusterização através do KMeans
Agora com os dados pré-processados e o número de Clusters definidos foi aplicado o algoritmo KMeans para segmentar os clientes. Fazendo uma classificação do comportamento dos Clusters através de seus Boxplots em: 
- Possível Churn; 
- Cliente Importante; 
- Cliente com Potencial; 
- Cliente Importante. 
Ao fim foi gerado um arquivo .csv com a segmentação dos clientes. 

# ✅5. Conclusões
![Warehouse](https://images.unsplash.com/photo-1590247813693-5541d1c609fd?q=80&w=2109&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)
Ao fim, conseguimos gerar um dataset com uma segmentação bastante útil para o time de marketing tornando possível criar dashboards e campanhas diretamente focadas a clientes como por exemplo:

- Uma campanha focada em reverter a possível situação de Churn dos clientes nesta segmentação. Propaganda negativa é muito mais efetiva que a positiva, especialmente em tempos de redes sociais, garantir um bom pós-venda e relacionamento com clientes é muito importante em qualquer sertor;
- Campanhas com descontos e outras formas de ativar os clientes com potencial, e fazer com que eles consumam mais produtos (é de entedimentos como este que você recebe aqueles e-mails de grandes lojas e varejistas online);
- Clientes que precisam de atenção, entram na mesmo caso de clientes em possível Churn, campanhas que ativem estes clientes e façam eles se sentirem "lembrados".
- Clientes importantes devem ter tratamento melhor, e acesso a desconto e métodos para aumentar sua fidelização junto a empresa. 