# 🏬 Análise RFV - Warehouse Sales Data

Neste projeto será realizada uma análise do tipo RFV (Recência, Frequência e Valor) com dados que encontrei neste video no Youtube do canal [Jie Jenn](https://www.youtube.com/watch?v=9wxWrERZvss).

![img](https://images.unsplash.com/photo-1624927637280-f033784c1279?q=80&w=2074&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

### Objetivos e resultados
O objetivo do projeto é através do algorítmo KMeans encontrar uma segmentação dos clientes para campanhas de marketing. Ao fim foi entregue uma arquivo .csv com os clientes segmentos em:

- Potencialmente Leais;
- Frequentes de Valor;
- Retenção;
- Regulares.

### 🛠️ Ferramentas utilizadas
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
## Estrutura do Dataset
Os dados são de uma rede varejista fictícia, as colunas estão organizadas dessa forma:

|Coluna|Descrição|
|-----|----------|
|**OrderNumber**|ID do pedido|
|**Sales Channel**|Canal de vendas do pedido|
|**WarehouseCode**|ID do armazém do pedido|
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

## Bibliotecas Python utilizadas
#### Manipulação de dados
- Pandas, Numpy.
#### EDA
- Seaborn, Matplotlib.
#### Clusterização
- KMeans.

## Insights e conclusões
### Sobre os segmentos
Pensei nos segmentos da seguinte forma:

- Clientes potencialmente leais: podem estar explorando diferentes produtos dentro da empresa e têm potencial para se tornarem leais à nossa marca com o tempo. Ofertas personalizadas e outros meios de mantê-los engajados são importantes.
- Frequentes de valor: são aqueles regulares que constantemente consomem nossos serviços. Com estes, precisamos usar estratégias de fidelização, como programas de recompensas e descontos por recorrência.
- Clientes de retenção: possivelmente estão perdendo o interesse em nossa marca ou podem já ter encontrado outra opção. Para estes, precisamos buscar meios de reativação e incentivos para reacender a vontade de nos buscar.
- Clientes regulares: são fiéis à nossa marca e retornam com certa regularidade. Buscar recomendações baseadas em suas últimas compras pode ser uma forma de estimular mais compras.

### Sugestões para o time marketing
#### Para Clientes Potencialmente Leais

1. Campanhas de recomendações e descontos personalizados: Através de e-mail marketing, sugerir produtos relacionados ou que complementam as últimas compras, juntamente com cupons de desconto.
2. Programa de exclusividade: Oferecer acesso exclusivo a novos produtos no catálogo com certa antecedência.
#### Para Clientes Frequentes de Valor

1. Programa de fidelidade: Oferecer recompensas a partir de metas de consumo, como descontos especiais e brindes que remetam à nossa marca, assim como eventos para clientes dentro do programa, como dias com ofertas diferenciadas.
#### Para Clientes de Retenção

1. Campanhas de reativação: Envio de e-mails com descontos agressivos baseados nas últimas compras feitas ou oferecer descontos para as próximas compras.
2. Pesquisas de satisfação: Envio de e-mails com pesquisa de satisfação, para entender os motivos da inatividade, com desconto especial ao final do formulário.
#### Para Clientes Regulares

1. Promoções de recompensa por referência: Incentivar esses clientes a indicarem amigos ou familiares oferecendo recompensas especiais, como descontos ou brindes, para cada nova indicação bem-sucedida.


![img](https://images.unsplash.com/photo-1563986768609-322da13575f3?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)


### Conclusões

Ao concluir este projeto, podemos ver como, no caso do setor de marketing, a Análise RFV pode ser ponto chave para campanhas bem-sucedidas e bons resultados. Uma segmentação bem realizada permite a criação de campanhas de marketing com um direcionamento personalizado para cada tipo de cliente, dando um pouco de "alma" para cada campanha. A análise pode ser direcionada para diversos outros setores com fins diferentes, mas sempre entregando como resultado uma segmentação que permite trabalhar de forma ajustada e com menos espaços para erros causados por generalismos.