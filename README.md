# Bootcamp_Data_Engineer

### Construção de uma arquitetura de pipeline de dados usando a cloud AWS para extrair dados do site Coinmarketcap através da API.

<<<<<<< HEAD

=======
![Arquitetura](https://user-images.githubusercontent.com/45739569/218257772-852a45c8-2992-4e81-84e3-d01bfb7fc1c8.PNG)

> > > > > > > 78c9d38d4905fca67ab7fa554513c1a836352f10

##### Ingestão dos dados:

- Foi usado a key da API na função get_data(key) na aplicação app.py;
- Provisionado o RDS PostgreSQL na AWS;
- O arquivo model.py configurado com a tabela tb_coins;
- Configurar o endpoint do RDS na variável db_string;
- Aplicação executada consumindo API e persistido no banco de dados.


