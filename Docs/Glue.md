## Glue context

```pyspark 
import sys
from awsglue.transforms import *
from awsglue.utils import getResolvedOptions
from pyspark.context import SparkContext
from awsglue.context import GlueContext
from awsglue.job import Job
  
sc = SparkContext.getOrCreate()
glueContext = GlueContext(sc)
spark = glueContext.spark_session
job = Job(glueContext)
``` 
# Examine the schema for glue code
``` 
persons = glueContext.create_dynamic_frame.from_catalog(
             database="poc-benji",
             table_name="reciept")
print("Count: ", persons.count())
persons.printSchema()
``` 
