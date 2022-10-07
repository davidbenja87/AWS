# Producer: put records to the KDS

aws kinesis put-record --stream-name kds-pv-benji  --partition-key user1 --data "isai" --cli-binary-format raw-in-base64-out
