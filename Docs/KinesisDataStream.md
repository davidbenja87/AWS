# Producer: put records to the KDS

cmd>aws kinesis put-record --stream-name kds-pv-benji  --partition-key user1 --data "isai" --cli-binary-format raw-in-base64-out

# Describe the stream
cmd> aws kinesis describe-stream --stream-name "kds-pv-benji"

# Get Shard Iterator ID
cmd>aws kinesis get-shard-iterator --stream-name "kds-pv-benji" --shard-id shardId-000000000000 --shard-iterator-type TRIM_HORIZON

# Get record from the first iterator
cmd>aws kinesis get-records --shard-iterator  "AAAAAAAAAAFj7BUH5pB/6LsJ6sx7J2pcQNelalRw/HKkcT8IC2AB1QQSWplHa32TMObm/OrvuObFacVuqPUGb4SR/JmyLQ6/72BEXTaefLkn+9hpPzJXAUx9u/qqiClodLLADco9Ln8pQnYqLHiDdmj95+vHL6GBH6qCgAltK54WA5kqHEEpMlakr2jJEV212DuSCBSd+Fohh6MsjJX4lm/Rc7jIU53UjcAI3SGFFAvI7QLO896uLQ=="

![image](https://user-images.githubusercontent.com/38088886/194479361-7808770c-18ae-4264-a488-0f766a9c1444.png)

# Loop next iterator until finds the record

![image](https://user-images.githubusercontent.com/38088886/194479462-ee6b68a5-4114-42e3-acd2-fbaf1ca76472.png)

