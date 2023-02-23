Esse projeto trata-se de contruir um Data Lake usando MinIO e Spark em um servidor local. O objetivo é processar Big Data no formato CSV e converte-lo em Parquet para posteriores analises.


Dataset: https://www.kaggle.com/datasets/nhs/general-practice-prescribing-data?resource=download

Haverá três zonas de trabalho:
    1) Landing
    2) Processing
    3) Curated


Algumas anotações (prints):

Lambda vs. Kappa
<![Lamba-vs-Kappa](/img/lambda-vs-kappa.png)>

Apache Parquet
<![Parquet](/img/apache-parquet.png)>

Apache Parquet
<![Parquet-Sample](/img/parquet-sample.png)>


Instalação do Spark Standalone
1 - Faça download do Spark.
    https://spark.apache.org/downloads.html
2 - Descompacte o arquivo para uma localização que deseja ter os binários do spark
    exemplo: /home/spark
3 - Edite o arquivo .bash_profile com os valores abaixo:
    export SPARK_HOME="/home/spark"
    export PATH="$PATH:$SPARK_HOME/bin"
    export PYTHONPATH=$PYTHONPATH:$SPARK_HOME/python:$SPARK_HOME/python/lib
4 - Feche e abra novamente o terminal para verificar se as variáveis foram definidas
com o comando:
    echo $SPARK_HOME
5 - Abrindo o Shell do Spark:
    spark-shell
6 - Abre o Shell pyspark
    pyspark


Bibliotecas faltantes s3a:
https://mvnrepository.com/artifact/org.apache.hadoop/hadoop-aws

Baixar conforme versão instalada do Spark e deixar disponível no local onde foi feita a build do Spark (ex. /home/spark/jars/)
ex. 
    1)  hadoop-aws-3.3.2.jar
    2)  aws-java-sdk-bundle-1.11.1026.jar 