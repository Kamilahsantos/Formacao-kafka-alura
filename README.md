# 📢  Projeto do curso da Alura [Kafka: Produtores, Consumidores e streams ](https://cursos.alura.com.br/course/kafka-introducao-a-streams-em-microservicos)




## ⚙ Comandos Kafka:

### 📥 Instalando o kafka

Realizar o download nesse [site](https://www.apache.org/dyn/closer.cgi?path=/kafka/2.8.0/kafka_2.12-2.8.0.tgz) e extrair o arquivo

 ### 🖥 Iniciando zookeeper
 
 Dentro da pasta bin
 
 ```
./zookeeper-server-start.sh (caminho de onde foi extraido o kafka)/kafka_2.13-2.8.0/config/zookeeper.properties 
```

### 🖥 Iniciando o kafka

 Dentro da pasta bin

 ```
./kafka-server-start.sh  (caminho de onde foi extraido o kafka)/kafka_2.13-2.8.0/config/server.properties
 ```

### 🖥 Consultando as operações disponiveis com topicos

 Dentro da pasta bin

 ```
./kafka-topics.sh
```


### 🖥 Criando um novo topico

 Dentro da pasta bin

 ```
 ./kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic ECOMMERCE_NEW_ORDER
 ```
 
 ### 🖥 Verificando os tópicos criados

 Dentro da pasta bin

 ```
 ./kafka-topics.sh --list --bootstrap-server localhost:9092
 ```
 
 ### 🖥 Criando um producer para produzir mensagens

 Dentro da pasta bin

 ```
./kafka-console-producer.sh --broker-list localhost:9092 --topic ECOMMERCE_NEW_ORDER
 ```
 
  ### 🖥 Criando um consumer e consumindo as mensagens desde o começo do producer

 Dentro da pasta bin

 ```
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic ECOMMERCE_NEW_ORDER --from-beginning
```
 
  ### 🖥 Configurando o numero de partições
   
 Dentro da pasta config:
 
 Acesse o arquivo server.properties e troque a num.partitions para num.partitions=3
 
 
  ### 🖥  Alterando o numero de partições de um topico
  
 ```
 ./kafka-topics.sh --alter --zookeeper localhost:2181 --topic ECOMMERCE_NEW_ORDER --partitions 3
 ```
 
  ### 🖥  Descrevendo os consumers groups
  
 ```
 ./kafka-consumer-groups.sh --all-groups --bootstrap-server localhost:9092 --describe 
 ```
 

