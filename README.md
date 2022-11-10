# Desafio_Boas_Praticas_com_DynamoDB

## Nesse deafio foi realizado os comandos para criar tabela no aws dynamodb

### O arquivo pode ser observado na figura:

![TabelaAWSDDB](https://github.com/gillrosas/Desafio_Boas_Praticas_com_DynamoDB/blob/main/Capturar.PNG)

### Foi realizado o dowloading do link LCI na AWS [AWS_CLI](https://aws.amazon.com/pt/cli/)

### Os comandos para a criação: 

```
  aws dynamodb create-table \
    --table-name Music \
    --attribute-definitions \
        AttributeName=Artist,AttributeType=S \
        AttributeName=SongTitle,AttributeType=S \
    --key-schema \
        AttributeName=Artist,KeyType=HASH \
        AttributeName=SongTitle,KeyType=RANGE \
    --provisioned-throughput \
        ReadCapacityUnits=10,WriteCapacityUnits=5

```

### Para add itens na tabela 
```
aws dynamodb put-item \
    --table-name Music \
    --item file://itemmusic.json \

```
