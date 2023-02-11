# Bootcamp_Data_Engineer

### Construção de uma arquitetura de pipeline de dados usando a cloud AWS para extrair dados do site Coinmarketcap através da API.

![Arquitetura](https://user-images.githubusercontent.com/45739569/218258669-fafad37f-4416-4b45-8217-4bf72c13f801.PNG)

##### Ingestão dos dados:

- Foi usado a key da API na função get_data(key) na aplicação app.py;
- Provisionado o RDS PostgreSQL na AWS;


![RDS](https://user-images.githubusercontent.com/45739569/218258389-71d38d08-dd2e-46c0-8ac1-7054ec677cb6.PNG)




- O arquivo model.py configurado com a tabela tb_coins;
- Configurar o endpoint do RDS na variável db_string;
- Aplicação executada consumindo API e persistido no banco de dados;
- Criação de um Data Lake no formato Delta no AWS S3 com buckets Raw, Processed e Curated.

![Delta_Lake](https://user-images.githubusercontent.com/45739569/218259255-96b34f51-3ad4-4c3c-ad30-39f08fff505c.PNG)


![S3](https://user-images.githubusercontent.com/45739569/218259611-3b0b5c30-0af4-45ce-8c41-91fd98fb1733.PNG)
