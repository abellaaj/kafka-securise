# kafka-securise
- dans ce projet j'ai configuré de kafka:

1- kafka avec ssl et SASL (MD5)

2-kafka avec ssl et SASL (SCRAM-SHA-512)

- Pour lancer le serveur kafka:

1) lancer en premier lieu zookeper: ./zookeper-server-start.sh ../config/zookeper.properties

2) lancer kafka : ./kafka-server-start.sh ../config.server.properties

- Pour le cas de SCRAM il faut lancer la commande suivnte pour créer le user admin ainsi que son mot de passe:

./kafka-configs.sh --zookeeper localhost:2181 --alter --add-config 'SCRAM-SHA-256=[password=admin-secret],SCRAM-SHA-512=[password=admin-secret]' --entity-type users --entity-name "admin"
