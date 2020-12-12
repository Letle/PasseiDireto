# Passei Direto

A ideia da manipulação da Base A foi utilizar PySpark para visualização dos DataSet e assim conseguir construir a modelagem.

Não montei as cargas para focar na construção do pipeline da Base B, que mesmo assim não foi conclído por falta de prática. =/


Utilizei o Jupyter Notebook para leitura dos DataSet, para executar é só baixar via pip, bem como os pacotes pertinentes.
Deve-se alterar a variável path nos dois notebooks para o caminho do seu repositório.


***    Reposta da pergunta   ***
Definir um pipeline dos dados. Estamos fornecendo uma base estática como exemplo,
mas no mundo real esses dados são populados constantemente. Como você
estruturaria a solução para que a base analítica seja mantida atualizada?

R: Utilizaria infraestrutura AWS para criação de um pipeline que pudesse entregar os dados modelados analiticamente, contendo S3 Buckets, SQS , Spark, DataBricks e Redshift. Onde a aplicação geraria eventos armazenados em um S3 bucket monitoriado periodicamente pelo SQS e por sua vez armazenaria esses eventos em uma fila. À partir da fila gerada no SQS é possível iniciar periodicamente o Databricks contendo notebooks utilizando Spark para ETL e auxiliando na carga em banco de dados Redshift disponibilizando dados para relatórios e análises.


