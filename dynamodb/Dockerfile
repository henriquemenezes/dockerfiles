FROM openjdk:8
LABEL maintainer "Henrique Menezes <hamsalmeida@gmail.com>"

WORKDIR /usr/local/dynamodb

RUN curl -L https://s3-us-west-2.amazonaws.com/dynamodb-local/dynamodb_local_latest.tar.gz | tar xz && \
    mkdir -p /var/lib/dynamodb/data

EXPOSE 8000
ENTRYPOINT ["/usr/bin/java", "-Djava.library.path=./DynamoDBLocal_lib", "-jar", "DynamoDBLocal.jar", "-dbPath", "/var/lib/dynamodb/data"]

VOLUME ["/var/lib/dynamodb/data"]
