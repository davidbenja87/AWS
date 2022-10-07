# Producer: put records to the KDS

cmd>aws kinesis put-record --stream-name kds-pv-benji  --partition-key user1 --data "isai" --cli-binary-format raw-in-base64-out

# Describe the stream
cmd> aws kinesis describe-stream --stream-name "kds-pv-benji"

# Get Shard Iterator ID
cmd>aws kinesis get-shard-iterator --stream-name "kds-pv-benji" --shard-id shardId-000000000000 --shard-iterator-type TRIM_HORIZON
