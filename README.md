# Pipeline-de-Dados-do-Telegram

* Introdução
  * O projeto visa automatizar a captação de dados de um bot e conversas de um grupo de chat na plataforma Telegram, utilizando ferramentas da AWS para ingestão, processamento e análise desses dados.

* Descrição do Projeto
  * Ingestão de Dados: Os dados brutos do Telegram são capturados por uma função AWS Lambda, que é acionada via API Gateway, e subsequentemente armazenados em um bucket S3 no formato JSON.
  * ETL e Armazenamento: Uma arquitetura orientada a eventos, orquestrada pelo AWS EventBridge, aciona outra função Lambda para processar e ordenar os dados brutos. Os dados transformados são então salvos em um bucket S3 no formato Parquet, otimizado para consumo.

* Conclusão
  * A fase final do pipeline envolve a apresentação dos dados, onde consultas SQL são realizadas e visualizações são criadas utilizando o Amazon Athena, permitindo a análise e o storytelling dos insights obtidos.
