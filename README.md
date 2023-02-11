# Bootcamp_Data_Engineer

### Construção de uma arquitetura de pipeline de dados usando a cloud AWS para extrair dados do site Coinmarketcap através da API.

![1](C:\Users\WINDOWS\Documents\TRT%20MA%20Estrategia\Arquitetura.PNG)



##### Ingestão dos dados:

- Foi usado a key da API na função get_data(key) na aplicação app.py;
- Provisionado o RDS PostgreSQL na AWS;
- O arquivo model.py configurado com a tabela tb_coins;
- Configurar o endpoint do RDS na variável db_string;
- Aplicação executada consumindo API e persistido no banco de dados.
