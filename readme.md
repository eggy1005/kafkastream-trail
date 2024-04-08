docker exec -it broker2 kafka-topics --create \
    --bootstrap-server localhost:9092 \
    --topic word-count-input \
    --replication-factor 1 \
    --partitions 2 

With two partitions

docker exec -it broker2 kafka-topics --create \
    --bootstrap-server localhost:9092 \
    --topic word-count-output \
    --replication-factor 1 \
    --partitions 2 

./kafka-topics.sh — zookeeper localhost:2181 — delete — topic <topic_name>

tear down the docker image
docker-compose down -v


Create two partitions so the application can scale
