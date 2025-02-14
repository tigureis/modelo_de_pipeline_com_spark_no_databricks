# Simulação de Streaming de Dados com Spark Structured Streaming e Delta Lake

## Descrição

Este projeto foi desenvolvido como um exercício durante meus estudos e serve como referência futura para a implementação de pipelines de streaming de dados. O objetivo é simular um streaming de dados utilizando dados fornecidos por meio de comandos SQL. O projeto demonstra como usar Spark Structured Streaming e Delta Lake para processar dados em tempo real.


## Funcionalidades

O projeto inclui as seguintes funcionalidades:

- Criação de tabelas Bronze, Silver e Gold para representar diferentes estágios do pipeline de dados.
- Ingestão de dados na camada Bronze usando comandos SQL.
- Processamento de dados na camada Silver usando Spark Structured Streaming, adicionando um timestamp e escrevendo os dados em um único batch.
- Escrita em múltiplas tabelas na camada Silver usando o método `foreachBatch` para garantir a escrita idempotente.
- Agregação de dados na camada Silver usando funções de agregação do Spark SQL.
- Processamento de mudanças nos dados (CDC) usando o comando `MERGE` para aplicar as atualizações.
- Junção incremental de tabelas usando streams de dados.
- Introdução de novos dados na camada Bronze.
- Comando para encerrar todos os processos de streaming.


## Pré-requisitos

- Databricks Runtime (Recomendado Databricks Runtime 12.2 LTS ML ou superior).
- Spark 3.3.x ou superior.
- Delta Lake 2.x ou superior.
