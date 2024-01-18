# Clickhouse

## Deploy

Clone the repository and change the directory to the cloned one.

```sh
docker-compose up -d
```

## Migration

### Install clickhouse cli

```sh
curl https://clickhouse.com/ | sh
```

### Connecting server

```sh
./clickhouse server
```

### Connecting client

```sh
./clickhouse client
```

### Export Data

```sh
 ./clickhouse client --host 127.0.0.1 --secure --password 123456 --port 9000 --query "SELECT * from table" --format FormatName > result.txt
```

### Import Data

```sh
./clickhouse client --host 127.0.0.1 --secure --password 123456 --port 9000 --query "insert into table format FormatName" < result.txt

```

### Reference links

| Name    | Description              | Link                                                                                                                                 |
| :------ | :----------------------- | :----------------------------------------------------------------------------------------------------------------------------------- |
| Formats | Input and output formats | [https://clickhouse.com/docs/en/interfaces/formats](https://clickhouse.com/docs/en/interfaces/formats)                               |
| Install | Installation             | [https://clickhouse.com/docs/en/install](https://clickhouse.com/docs/en/install)                                                     |
| Export  | Export data              | [https://clickhouse.com/docs/knowledgebase/file-export](https://clickhouse.com/docs/knowledgebase/file-export)                       |
| Import  | Import data              | [https://clickhouse.com/docs/en/integrations/data-formats/csv-tsv](https://clickhouse.com/docs/en/integrations/data-formats/csv-tsv) |
