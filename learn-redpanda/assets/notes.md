ubuntu-os-cloud/ubuntu-2204-lts


 sudo apt-get update
 sudo apt-get install docker-compose-plugin


docker run --rm -it --entrypoint sh redpandadata/console

touch /tmp/config.yml

export CONFIG_FILEPATH=/tmp/config.yml

kafka:
  brokers:
  - redpanda-0:19092
  schemaRegistry:
    enabled: true
    urls:
    - http://redpanda-0:18081
redpanda:
  adminApi:
    enabled: true
    urls:
    - http://redpanda-0:9644

kafka:
  brokers: ["redpanda-0:9092"]
  schemaRegistry:
    enabled: true
    urls: ["http://redpanda-0:8081"]
redpanda:
  adminApi:
    enabled: true
    urls: ["http://redpanda-0:9644"]

kafka:
  brokers:
  - redpanda-0:9092
  schemaRegistry:
    enabled: true
    urls:
    - http://redpanda-0:8081
redpanda:
  adminApi:
    enabled: true
    urls:
    - http://redpanda-0:9644

export CONFIG_FILEPATH='/tmp/config.yml'
export KAFKA_BROKERS=redpanda-0:9092
export KAFKA_BROKERS_SCHEMAREGISTRY_ENABLED=true
export KAFKA_BROKERS_SCHEMAREGISTRY_URLS=http://redpanda-0:18081
export REDPANDA_ADMINAPI_ENABLED=true
export REDPANDA_ADMINAPI_URLS=http://redpanda-0:9644

