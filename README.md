# unifacef-kafka-categorizador
Projeto da Pós da Unifacef em desenvolvimento web para a disciplina de Mensageria/Streams

1. Entre na pasta do projeto e inicie no terminal o Kafka
```
docker-compose up -d
```

2. Inicie o projeto pelo comando abaixo
```
./mvnw spring-boot:run
```

3. Crie os eventos de Entrada para digitar algumas palavras
```
docker-compose exec kafka kafka-console-producer --bootstrap-server localhost:9092 --topic entrada
```

4. Digite algumas palavras de diversos tamanhos neste terminal
 
5. Abra um novo terminal para cada fila de tamanho de palavras: pequenas (até 3 caracteres), médias (até 6 caracteres), grandes (até 12 caracteres) e gigantes (maiores de 12 caracteres)
 
```
docker-compose exec kafka kafka-console-consumer --bootstrap-server localhost:9092 --topic pequenas --from-beginning
```
 
```
docker-compose exec kafka kafka-console-consumer --bootstrap-server localhost:9092 --topic medias --from-beginning
```
```
docker-compose exec kafka kafka-console-consumer --bootstrap-server localhost:9092 --topic grandes --from-beginning
```
```
docker-compose exec kafka kafka-console-consumer --bootstrap-server localhost:9092 --topic gigantes --from-beginning
``` 
 
 
 


