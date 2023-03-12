# Bootcamp_Data_Engineer

## Construção de uma arquitetura de pipeline de dados usando a cloud AWS para extrair dados do site Coinmarketcap através da API extraindo os dados .JSON.

![Arquitetura](https://user-images.githubusercontent.com/45739569/218258669-fafad37f-4416-4b45-8217-4bf72c13f801.PNG)

### Ingestão dos dados para o RDS usando o SGBD PostgreSQL:

- Foi usado a key da API na função get_data(key) na aplicação app.py;
- Provisionado o RDS PostgreSQL na AWS;


![RDS](https://user-images.githubusercontent.com/45739569/218258389-71d38d08-dd2e-46c0-8ac1-7054ec677cb6.PNG)




- O arquivo model.py configurado com a tabela tb_coins;
- Configurar o endpoint do RDS na variável db_string;
- Aplicação executada consumindo API e persistido no banco de dados.

### Criação de um Data Lake no formato Delta no AWS S3 com buckets Raw, Processed e Curated:

![Delta_Lake](https://user-images.githubusercontent.com/45739569/218259255-96b34f51-3ad4-4c3c-ad30-39f08fff505c.PNG)


![S3](https://user-images.githubusercontent.com/45739569/218259611-3b0b5c30-0af4-45ce-8c41-91fd98fb1733.PNG)



### Migração de dados do RDS para o bucket Raw através do DMS, sendo criados arquivos .CSV:


![DMS](https://user-images.githubusercontent.com/45739569/224553617-b626215b-4f74-4e95-83f0-2a6d3107fe71.png)


### Processamento de dados entre os Buckets do S3:

- Foi criado o cluster Amazon EMR para fazer a leitura dos dados em .CSV do bucket Raw para escrever em formato Delta para os Buckets Processing e Curated através do PySpark.


![Data Lake Buckets](https://user-images.githubusercontent.com/45739569/224554457-89eea6a9-3a7c-48ac-b6ae-9ce659cc67f6.png)


### Criação de Crawlers e Consultas com Athena:

- Foi criado Crawler através do Glue para acesso as dados do Bucket Processing e Curated para fazer consultas SQL usando AWS Athena que é um serviço Serverless não precisando de nenhuma instância.

![Crawler](https://user-images.githubusercontent.com/45739569/224555564-2b741c10-909c-4ea6-8886-f0c5147fc1de.png)


![Athena](https://user-images.githubusercontent.com/45739569/224555727-76d0f8d5-78c3-42ee-871e-d768c6a43057.png)


### Subindo o Data Warehouse com Redshift para armazenar os dados.


![Redshift4](https://user-images.githubusercontent.com/45739569/224556620-dc2368f7-8350-4e3d-b46f-7dac2c1055d8.png)






