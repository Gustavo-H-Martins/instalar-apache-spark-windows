# Configurando o Apache Spark no Windows 11:

## 1. Instalação do Java:

O **`Spark`** requer o `Java Development Kit` (JDK). Baixe e instale o JDK mais recente em seu sistema. Você pode usar o [`Oracle JDK`](https://www.oracle.com/java/technologies/downloads/#jdk21-windows) ou o [`OpenJDK`](https://learn.microsoft.com/pt-br/java/openjdk/download).

## 2. Download do Spark:

Acesse o [site oficial do **Apache Spark**](https://spark.apache.org/downloads.html) e faça o download da versão mais recente do Spark pré-construída para o Hadoop.

1. Extraia os Arquivos:
    Extraia o arquivo que você baixou para uma pasta no seu sistema. Certifique-se de que o caminho da pasta não contenha espaços em branco, pois isso pode causar problemas.

## 3. Download do hadoop:

Acesse o link da distribuição para windows do [**Apache Hadoop** no github](https://github.com/cdarlint/winutils) e baixe a versão compatível com a do Spark

## 4. Variáveis de Ambiente:

Adicione as variáveis de ambiente para o Spark, Hadoop e o Java:
Crie uma nova variável de sistema chamada SPARK_HOME e defina o caminho para a pasta onde o Spark foi extraído.
Adicione %SPARK_HOME%\bin ao seu PATH de sistema.

```bash
    setx SPARK_HOME C:\spark\spark_vX.X.X_bin_hadoop_vX.X
    sext PATH "%PATH%;%SPARK_HOME%\bin"
    # ÊXITO: o valor especificado foi salvo.
```

Crie uma nova variável de sistema chamada HADOOP_HOME e defina o caminho para a pasta onde o Hadoop foi salvo.
Adicione %HADOOP_HOME%\bin ao seu PATH de sistema.
```bash
    setx HADOOP_HOME C:\hadoop
    sext PATH "%PATH%;%SPARK_HOME%\bin"
    # ÊXITO: o valor especificado foi salvo.
```
Crie uma variável de sistema chamada JAVA_HOME e defina o caminho para a pasta onde o JDK está instalado.
Adicione %JAVA_HOME%\bin ao seu PATH de sistema.
```bash
    setx JAVA_HOME C:\java
    sext PATH "%PATH%;%JAVA_HOME%\bin"
    # ÊXITO: o valor especificado foi salvo.
```
## 5. Teste a Instalação:

Abra um prompt de comando e digite `spark-shell`. 
```bash 
    spark-shell
    # Setting default log level to "WARN".
    # To adjust logging level use sc.setLogLevel(newLevel). For SparkR, use setLogLevel(newLevel).
    # Spark context Web UI available at http://localhost:4040/jobs/
    # Spark context available as 'sc' (master = local[*], app id = local-1697213488762).
    # Spark session available as 'spark'.
    # Welcome to
    #      ____              __
    #     / __/__  ___ _____/ /__
    #    _\ \/ _ \/ _ `/ __/  '_/
    #   /___/ .__/\_,_/_/ /_/\_\   version 3.5.0
    #      /_/
    # 
    # Using Scala version 2.12.18 (Java HotSpot(TM) 64-Bit Server VM, Java 21)
    # Type in expressions to have them evaluated.
    # Type :help for more information.

    # scala>
```
Isso iniciará o shell do Spark. 
Você deve ver a interface do [Spark disponível no seu navegador.]()

[![Gustavo-H-Martins](https://github-readme-stats.vercel.app/api?username=Gustavo-H-Martins&show_icons=true&theme=radical)](https://github.com/Gustavo-H-Martins)

## 🧾 Licença
Este projeto é free. 
Consulte o arquivo [LICENSE](./LICENCE) para mais detalhes.

## 🧑🏽 Colaboradores
Este projeto foi criado por:

- Gustavo H Martins ([GitHub](https://github.com/Gustavo-H-Martins) | [LinkedIn](https://www.linkedin.com/in/gustavo-henrique-lopes-martins-361789192/))


## 🔋👩🏽‍💻 Status do Projeto
Este projeto está em andamento e recebe atualizações frequentes.
